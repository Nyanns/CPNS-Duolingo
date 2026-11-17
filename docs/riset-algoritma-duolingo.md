# Riset Algoritma Duolingo → Pemetaan ke Aplikasi Duolingo CPNS

**Tanggal:** 13 November 2026
**Sifat:** riset dan laporan saja — TIDAK ada perubahan artifact.
**Membangun di atas:** `~/workspace/research_notes/duolingo-ui-algoritma-20261113/report.md`
(token Duolingo, pola lesson path, aturan streak, ringkasan HLR vs FSRS, arsitektur clone).
Laporan ini mendalami bagian algoritmanya: HLR, Birdbrain, penjadwalan review,
adaptasi kesulitan, dan mekanik streak/XP/liga/quest/daily goal.

## 0. Cara membaca laporan ini — kejujuran sumber

- **[PRIMER]** = dibaca langsung dari sumber primer (blog/paper resmi Duolingo,
  paper peer-review, repo benchmark).
- **[SEKUNDER]** = dirangkum dari kajian pihak ketiga yang mengutip sumber primer;
  angkanya dikutip apa adanya dengan nama sumbernya.
- **[PERKIRAAN]** = inferensi/hipotesis penulis laporan, ditandai jelas; bukan fakta.
- Angka benchmark Anki **bukan** angka CPNS: benchmark mengukur prediksi recall
  kosakata Anki. Yang penting adalah **ranking antar-algoritma**, bukan angka absolutnya.
- Duolingo berhenti memublikasikan algoritma intinya setelah 2021 (berdasarkan
  penelusuran riset loxelingo, Agu 2026: daftar publikasi research.duolingo.com
  berjalan 2015–2021, tidak ditemukan paper algoritma adaptif 2024–2026).
  Apa pun tentang "Birdbrain saat ini" di luar blog 2020 + wawancara Bicknell
  adalah inferensi sekunder — ditandai sebagai [SEKUNDER].

## 1. Ringkasan algoritma Duolingo

### 1.1 HLR — Half-Life Regression (Settles & Meeder, ACL 2016) [PRIMER]

Model memori sebagai **half-life** `h`: waktu sampai probabilitas recall turun ke 50%.

- `p = 2^(-Δ/h)` — probabilitas recall setelah lag `Δ` sejak latihan terakhir.
- `ĥ(x) = 2^(Θ·x)` — half-life diduga dari fitur riwayat belajar (jumlah paparan,
  benar/salah sebelumnya, waktu sejak paparan terakhir, fitur lexeme).
- Loss (dari blog Duolingo):
  `ℓ(⟨p,∆,x⟩ ; Θ) = (p − 2^(−∆/2^(Θ·x)))^2 + α(−∆/log2(p) − 2^(Θ·x))^2 + λ‖Θ‖²`.
- Data: eksperimen perbandingan memakai 12 jt+ sesi latihan Duolingo; dataset
  publik ~13 jt traces, 200 rb+ pengguna, 8 bahasa [SEKUNDER — loxelingo].
  Kode + data: `github.com/duolingo/halflife-regression`.
- Hasil [PRIMER — blog Duolingo, dibaca langsung 13 Nov 2026]: error prediksi
  **hampir setengah** dari sistem Leitner; A/B live: retensi harian **+9,5%**
  untuk practice session, **+1,7%** untuk lesson, **+12%** untuk aktivitas
  keseluruhan. (Catatan: A/B 6 minggu, ~1 jt learner, error turun 7,3% pada
  awalnya, lalu naik menjadi +9,5% setelah fitur lexeme yang overfit dihapus —
  [SEKUNDER — pracha.me, mengutip Tabel 4 paper].)
- Sejarah: Leitner (2012) → HLR (2016).

**Revisi 2026** — Ilídio et al., "Revisiting Half-Life Regression for Explainable
and Personalized Spaced Repetition in Duolingo", PMLR 339:217–227, IRAISE 2026
[PRIMER — abstrak + hasil dibaca dari PDF PMLR]:
- HLR diperluas menjadi **mixed-effects HLR (HLR+LMM)**: random effects bersilang
  untuk learner dan lexeme — artinya model ini secara eksplisit memulihkan
  parameter ability learner dan difficulty lexeme yang interpretable.
- Random effects hasil estimasi dipakai sebagai input **Random Forest (RF+EF)**.
- Hasil: HLR+LMM mengalahkan HLR di semua metrik; RF+EF terbaik di AUC dan
  korelasi Spearman; analisis SHAP menunjukkan fitur kontekstual + fitur
  random-effects (yang mencerminkan difficulty lexeme dan ability learner) paling
  penting.
- Penting: ini riset akademik (KU Leuven) atas data/model Duolingo, **bukan**
  pengumuman bahwa Duolingo production memakai model ini.

### 1.2 Birdbrain (2020 → V2) [PRIMER blog Duolingo via kutipan + wawancara Bicknell]

- **V1 (2020):** regresi logistik beraroma IRT (Item Response Theory) —
  `P(correct)` sebagai fungsi dari ability learner minus difficulty soal.
  Mengestimasi **keduanya** (ability learner + difficulty soal) dan meng-update
  keduanya setelah setiap interaksi. Dikembangkan bersama Carnegie Mellon.
- **Session Generator** memakai prediksi Birdbrain untuk merakit pelajaran pada
  "Goldilocks difficulty" — zona tantangan optimal (Zone of Proximal Development
  Vygotsky): tidak terlalu mudah (membosankan) dan tidak terlalu sulit
  (mematahkan semangat). Per Okt 2020, >20% pelajaran sudah terpersonalisasi
  [SEKUNDER — loxelingo, mengutip blog Duolingo].
- **V2:** LSTM/RNN yang memampatkan seluruh riwayat interaksi learner menjadi
  **vektor laten 40-dimensi**, di-update setiap exercise (profil teknis IEEE
  Spectrum via Settles; dikonfirmasi Bicknell: "formally, the current version
  of Birdbrain is implemented with artificial neural networks, specifically a
  version of a recurrent network").
- **Unified (saat ini)** [SEKUNDER]: satu model deep learning memprediksi
  half-life DAN seleksi konten sekaligus — HLR ("kapan") dan Birdbrain ("apa")
  dilebur.
- **Yang TIDAK dipublikasikan:** angka akurasi Birdbrain, band P(correct) target
  yang dipakai Session Generator, detail arsitektur V2 selain "RNN 40-dim".
  Jangan mengutip angka-angka itu — tidak ada sumbernya.

### 1.3 Strength meter & skill decay [PRIMER — blog Duolingo "How we learn how you learn"]

- Setiap skill punya **strength meter**: penuh + ikon emas saat selesai; turun
  ke setengah = waktunya latihan; kata terlemah dipilih untuk sesi latihan khusus.
- Skill **"crack" (retak)** saat kekuatannya jatuh — harus diperbaiki (repair).
- Ini adalah UX di atas HLR: rata-rata prediksi recall per kata dalam skill.
  Perilaku yang sama berlaku untuk soal: makin lama tidak disentuh, makin lemah.

### 1.4 Streak, XP, daily goal, liga, quest [SEKUNDER — konsisten di banyak kajian]

- **Streak:** naik maks **1× per hari kalender** saat lesson selesai; hari yang
  sama = no-op; jeda >1 hari = reset ke 1. **Freeze** = asuransi untuk 1 hari
  terlewat (dibeli dengan mata uang in-app / perk). Milestone 7/30/100/365 hari
  membuka reward. Klaim Trophy (2026): freeze menghasilkan streak rata-rata
  4,5× lebih panjang pada hari ke-21 — angka Trophy, **bukan** angka Duolingo;
  jangan dikutip sebagai fakta Duolingo.
- **XP:** mata uang bersama yang mengikat lesson + liga + achievement; feedback
  langsung (XP tampil sebelum layar lesson ditutup); reward variabel (10/20/bonus).
- **Daily goal:** target XP yang **diatur pengguna** (5–20 menit konten); cincin
  goal berubah emas saat tercapai; streak dikalibrasi ke target itu, bukan angka
  absolut.
- **Liga:** mingguan, ~30 peserta, **10 tier sampai Diamond**, promosi/degradasi
  di akhir minggu; matchmaking berdasarkan level aktivitas sejenis (supaya
  kompetisi terasa bisa dimenangkan, bukan mustahil). Bisa opt-out.
- **Quest:** harian (Earn 10 XP, 5 benar beruntun, 5 menit belajar) + bulanan
  (selesaikan 30 quest) + badge.
- **Hearts:** kesalahan menghabiskan hati di tier gratis — friksi monetisasi,
  bukan mekanisme belajar.
- **Notifikasi:** contextual bandit yang belajar reminder mana yang efektif
  (menurut satu kajian dilatih pada ~200 jt reminder — [SEKUNDER]).

### 1.5 FSRS — pembanding modern [PRIMER — repo open-spaced-repetition/srs-benchmark]

- FSRS-6: model **DSR (Difficulty, Stability, Retrievability)**, kurva lupa
  **power-law** (bukan eksponensial), **21 parameter**, dilatih dengan BPTT +
  maximum likelihood pada log review.
- Benchmark terbuka (9.999 koleksi Anki, ~350 jt review untuk evaluasi,
  TimeSeriesSplit — model hanya melihat masa lalu):

  | Algoritma | Log loss ↓ | RMSE (bins) ↓ | AUC ↑ |
  |---|---|---|---|
  | RWKV-Instant (neural, 2,76 jt param) | 0,2773 | — | 0,8329 |
  | FSRS-7 recency (34 param) | 0,3370 | — | 0,7220 |
  | **FSRS-6 (21 param)** | **0,3460** | **0,0653** | **0,7034** |
  | FSRS-6 default (tanpa optimasi per-user) | 0,3661 | 0,0927 | 0,6956 |
  | HLR (Duolingo, 3 param) | 0,4694 | 0,1275 | 0,6369 |
  | Anki SM-2 (default) | 0,616 | 0,1724 | 0,6133 |
  | SM-2 (original 1987) | 0,722 | 0,2031 | 0,6026 |

  (Angka direproduksi identik oleh tiga kajian independen dari repo yang sama;
  variasi 0,3456 vs 0,3460 di beberapa sumber = perbedaan pembulatan/tabel.)
- FSRS-6 mengalahkan SM-2 untuk **~99,5–99,7%** koleksi; klaim dok FSRS:
  20–30% lebih sedikit review pada retensi setara [SEKUNDER].
- Anki 23.10+ memakai FSRS sebagai default; **desired retention default 90%**.
- FSRS-7 (34 parameter, interval fraksional, kurva lupa 8 parameter) sedikit
  lebih baik dan satu-satunya versi dengan prediksi same-day recall yang realistis.
- Caveat: data Anki (kosakata, pengguna self-selected); SM-2 tidak mengeluarkan
  probabilitas sehingga perlu konversi untuk benchmark — tetapi AUC (yang tidak
  bergantung pada konversi itu) menunjukkan ranking yang sama.

### 1.6 Elo / IRT — keluarga model yang sama (pengetahuan standar)

- **Elo** (Arpad Elo, catur): ekspektasi `E = 1 / (1 + 10^(-ΔR/400))`;
  update `R' = R + K·(S − E)`, dengan `S` hasil aktual (1/0) dan `E` ekspektasi.
  Besarnya update proporsional dengan "kejutan" (`S − E`): hasil yang sudah
  diduga hampir tidak menggerakkan rating; hasil mengejutkan menggerakkannya jauh.
- **IRT 2PL:** `P(correct|θ) = 1 / (1 + exp(−a(θ − b)))`; `b` = difficulty,
  `a` = discrimination.
- **Birdbrain V1 ≈ IRT/Elo**: fungsi logistik dari (ability − difficulty) dengan
  update kedua sisi. Jadi Elo dan Birdbrain V1 adalah satu keluarga — bedanya
  adalah cara pakai, bukan rumus dasar.

## 2. Keadaan aplikasi kami saat ini (fakta dari konteks tugas)

- **FSRS-6** di buku kesalahan: 4 rating (1 Lupa, 2 Sulit, 3 Lumayan, 4 Mudah),
  D/S/R, **target retensi 0,90**, antrean due-today (2 item jatuh tempo),
  2 item aktif.
- **Elo:** ability pengguna baseline **1500**; Elo per soal; delta per subtes
  dari dashboard — TWK +96 (soal rata-rata 1404), TIU +30 (soal 1470),
  TKP +0 (soal 1500); label flow: "kesulitan HOTS (1500) dekat dengan
  kemampuanmu (1500)".
- **Streak 7**, freeze **1 tersedia**, maks +1/hari, freeze menutup tepat 1 hari
  terlewat, server-side; week strip.
- **XP total 155**; 4 Daily Quests (sesi 20, FSRS 15, HOTS 30, TKP 25 XP),
  reset harian; cincin daily goal ada.
- **Lesson path:** node 70×70, zigzag ±64px; state selesai (hijau + mahkota emas
  bila sempurna), saat ini (hijau + bintang + denyut + gelembung MULAI),
  terkunci (abu-abu), terlewat (merah #E05252); banner "Bagian SKD, Unit N";
  popover node.
- **Mastery per topik:** akurasi, progressPct, state SOLID/EXPOSED.
- 29 sesi / 714 soal; simulasi Sabtu 110 soal/100 menit (slot 0 soal).
- **Gap verifikasi (jangan membangun di atas asumsi ini sebelum dicek):**
  (1) apakah Elo soal ikut bergerak setelah attempt, dan berapa K-factor-nya;
  (2) apakah target daily goal sudah bisa diatur pengguna;
  (3) apa yang dilakukan tombol "Ronde Legendary" di popover node;
  (4) apakah XP tampil langsung di layar payoff;
  (5) apakah FSRS-6 memakai parameter default atau sudah dioptimasi per-user.

## 3. Tabel pemetaan + rekomendasi

| # | Algoritma Duolingo | Mekanisme kami | Rekomendasi | Alasan |
|---|---|---|---|---|
| 1 | HLR (spaced repetition) | FSRS-6 | **KEEP** | Benchmark: FSRS-6 log loss 0,3460 vs HLR 0,4694 (≈26% lebih rendah); AUC 0,7034 vs 0,6369. Bahkan FSRS-6 default (0,3661) mengalahkan HLR. HLR = model 2016, 3 parameter, kurva eksponensial; FSRS-6 = 21 parameter, power-law. Tidak ada alasan perilaku Duolingo yang membenarkan downgrade — Duolingo sendiri sudah bergerak ke model unified, dan revisi HLR 2026 bersifat akademik. |
| 2 | Birdbrain V1 — P(correct), Elo/IRT | Elo 1500 + Elo soal | **ADAPT** (Birdbrain-lite) | Elo sudah satu keluarga dengan Birdbrain V1 (logistik ability−difficulty). Yang kurang: (a) update **dua sisi** (ability pengguna + difficulty soal) — verifikasi dulu apakah Elo soal sudah bergerak; bila belum, tambahkan update item dengan K lebih kecil; (b) gunakan P(correct) untuk sequencing — lihat #3. JANGAN bangun LSTM 40-dim (Birdbrain V2): 1 user, 714 soal — tidak ada skala data dan tidak ada infra untuk itu. |
| 3 | Session Generator — Goldilocks / ZPD | Sesi harian tetap + antrean FSRS | **ADAPT** | Jangan ubah sesi harian jadi adaptif (sesi harian melayani cakupan materi + simulasi ujian — nilainya justru pada keteraturan). ADAPT: (a) urutkan soal di dalam sesi memakai P(correct) Elo — mudah dulu untuk momentum (sudah menjadi strategi flow kami), lalu sulit; (b) mode "latihan adaptif" terpisah yang merakit soal dari bank berdasarkan band P(correct) target; (c) antrean error-book sudah adaptif via FSRS — tambahkan pengurutan P(correct) di dalamnya. Band target **[PERKIRAAN]**: P(correct) ~0,70–0,85 untuk sesi belajar (zona flow); Duolingo tidak memublikasikan band-nya — perlakukan sebagai hipotesis awal, bukan fakta. |
| 4 | Strength meter + cracked skill | Mastery per topik (SOLID/EXPOSED) + buku kesalahan | **ADAPT** (prioritas tertinggi) | FSRS sudah menghitung Retrievability per item — rata-ratakan per topik menjadi "strength meter" (batang kekuatan yang meluruh) dan tandai topik "retak" bila R jatuh di bawah ambang (mis. R<0,70 — ambang [PERKIRAAN], sesuaikan dari data). Ini memakai data yang sudah ada, tanpa model baru, dan langsung memberi isi pada node mastery di path. |
| 5 | Streak (+freeze, repair, milestone) | Streak 7, freeze 1, maks +1/hari, server-side | **KEEP** inti; **ADAPT** kecil | Inti sudah sama dengan Duolingo (maks +1/hari, freeze 1 hari, server-side). Tambah: perayaan milestone 7/30/100 hari (murah, motivasi tinggi). Tunda: streak repair berbayar XP (Duolingo punya) — freeze sudah menutup 1 hari; tambah hanya bila streak putus menjadi masalah nyata. |
| 6 | XP (mata uang bersama, feedback langsung) | XP 155, quest reward, payoff | **KEEP**; **ADAPT** kecil | Ekonomi XP sudah ada. Tambah: bonus XP variabel (perfect session, runtun benar) — reinforcement variabel ala Duolingo; verifikasi XP tampil langsung di layar payoff. XP dari review FSRS sudah dihitung ke daily goal (seperti Duolingo yang menghitung review). |
| 7 | Daily goal (target XP pilihan pengguna, cincin emas) | Cincin daily goal (target belum terverifikasi) | **ADOPT** (verifikasi dulu) | Verifikasi apakah target cincin sudah bisa diatur pengguna. Bila tetap: jadikan pilihan (mis. 20/50/100 XP) + cincin jadi emas saat tercapai — persis mekanik Duolingo, murah. |
| 8 | Liga mingguan (~30 orang, 10 tier, promosi/degradasi) | Label "Liga Emas Elo 1500" (solo) | **ADAPT** (solo ladder) | Liga multiplayer tidak mungkin (1 user) — dan JANGAN mengarang lawan palsu. ADAPT: tangga solo — pita Elo dipetakan ke tier liga (Bronze→Diamond); promosi/degradasi mingguan berdasarkan XP minggu itu vs riwayat minggu-minggu sendiri ("liga melawan diri sendiri"). Mempertahankan psikologi tangga tanpa kebohongan. |
| 9 | Quest harian + bulanan + badge | 4 Daily Quest, reset harian | **KEEP**; **ADOPT** kecil | Quest harian sudah ala Duolingo. Tambah: quest bulanan + badge ("selesaikan 30 quest dalam sebulan") dan quest "5 benar beruntun" (Duolingo punya; kami punya akurasi per sesi tapi belum quest runtun). Murah (counter + badge). |
| 10 | Hearts (biaya kesalahan) | Tidak ada | **KEEP OUT** | Hearts adalah friksi monetisasi, bukan mekanisme belajar. Aplikasi tanpa pembayaran, 1 user. Jangan diadopsi. |
| 11 | Notifikasi contextual bandit | Cron 10:00 + 09:41 | **KEEP OUT** | Bandit butuh volume data yang tidak ada (1 user). Cron yang ada sudah cukup. Tunda tanpa batas. |
| 12 | Placement test (diagnostik awal) | Elo 1500 baseline + delta dari attempt nyata | **KEEP** (lewati) | Elo sudah terkalibrasi oleh 8 hari attempt nyata (TWK +96, TIU +30, TKP +0). Placement test hanya berguna di awal; nilainya sekarang kecil. Lewati. |
| 13 | Lesson path + node mastery | Node 70px, 4 state, mastery topik | **ADAPT** (via #4) | Node sudah mengikuti pola Duolingo. Yang ditambah adalah isi mastery-nya: strength meter per topik (#4) + review "Legendary" untuk sesi selesai (mahkota sudah ada; tombol "Ronde Legendary" perlu diverifikasi dulu apa yang dilakukannya sebelum diperluas). |
| 14 | FSRS-7 (penerus FSRS-6) | FSRS-6 | **Tunda** (ADAPT nanti) | FSRS-7 (34 param, interval fraksional, log loss 0,3370) sedikit lebih baik dan satu-satunya versi dengan prediksi same-day recall yang realistis. Tunda sampai ada cukup banyak data review; migrasi kecil, bukan prioritas. |

## 4. Dua pertanyaan wajib — jawaban tegas

### 4.1 FSRS-6 vs HLR: KEEP FSRS-6

- **Bukti benchmark** (repo terbuka, 9.999 koleksi, ~350 jt review): FSRS-6
  log loss 0,3460 vs HLR 0,4694; AUC 0,7034 vs 0,6369; RMSE 0,0653 vs 0,1275.
  Selisih ≈26% — bukan margin tipis.
- Bahkan FSRS-6 **tanpa optimasi per-user (0,3661)** masih mengalahkan HLR.
- HLR adalah model 2016 (3 parameter, eksponensial); FSRS-6 adalah 21 parameter
  dengan power-law forgetting curve yang secara empiris lebih cocok dengan log
  review besar.
- Revisi HLR 2026 (Ilídio et al.) memperbaiki HLR dengan mixed-effects +
  Random Forest — tapi itu riset akademik, bukan sistem produksi Duolingo, dan
  paper itu tidak membandingkan HLR+LMM+RF dengan FSRS — jangan klaim ada
  perbandingan itu.
- Satu-satunya argumen untuk HLR adalah "sama seperti Duolingo" — itu argumen
  branding, bukan argumen belajar. Duolingo sendiri tidak lagi memakai HLR murni
  (model unified Birdbrain).
- **Caveat jujur:** benchmark memakai data Anki (kosakata bahasa). Ranking-nya
  robust (selisih besar, 9.999 koleksi), tapi angka absolut tidak transfer ke
  soal CPNS. Tidak ada benchmark HLR-vs-FSRS pada data CPNS — dan tidak perlu
  ada untuk keputusan ini.

### 4.2 Birdbrain vs Elo: Elo sudah setara perannya (V1) — ADAPT, bukan ganti

- Birdbrain V1 = model logistik gaya IRT/Elo: `P(correct)` dari
  (ability − difficulty), update kedua sisi setiap jawaban. Elo kami = keluarga
  yang sama, dengan ability 1500 + Elo per soal.
- Yang membuat Birdbrain "Birdbrain" bukan rumusnya, melainkan **cara pakainya**:
  (a) memprediksi P(correct) untuk SETIAP soal yang mungkin disajikan,
  (b) Session Generator memilih soal pada band kesulitan Goldilocks,
  (c) update kedua sisi (learner + item).
- Jadi: jangan ganti Elo dengan "Birdbrain" — Elo kami **adalah** Birdbrain-lite.
  Yang perlu dibangun:
  1. Pastikan Elo soal ikut bergerak (verifikasi implementasi; bila belum,
     tambahkan update item dengan K lebih kecil dari K pengguna).
  2. Hitung `P(correct) = 1 / (1 + 10^(-(ability − difficulty)/400))` dan pakai
     untuk sequencing (urutan soal dalam sesi, antrean error-book, mode adaptif).
  3. Log response time sebagai sinyal kepercayaan (Duolingo menggunakannya
     [SEKUNDER]) — murah dicatat, berharga nanti.
- Birdbrain V2 (LSTM 40-dim): **JANGAN**. Membutuhkan data skala besar + infra
  training; untuk 1 user dan 714 soal, modelnya akan overfit/noise. Keuntungan
  marjinal, biaya besar.

## 5. Urutan pengerjaan yang disarankan

**Fase 1 — murah, nilai langsung (kerjakan dulu):**
1. Birdbrain-lite: verifikasi + lengkapi update Elo dua sisi; hitung P(correct)
   per soal; pakai untuk mengurutkan soal dalam sesi (mudah → sulit) dan antrean
   error-book.
2. Strength meter per topik dari FSRS Retrievability + status "retak" + ajakan
   perbaikan (ini yang paling Duolingo).
3. Daily goal bisa diatur pengguna (target XP) + cincin emas saat tercapai —
   verifikasi dulu konfigurabilitas saat ini.
4. Milestone streak 7/30/100 + perayaan.
5. Monthly quest + badge + quest "5 benar beruntun".

**Fase 2 — setelah simulasi Sabtu / bila ada waktu:**
6. Solo league ladder (pita Elo → tier; promosi/degradasi mingguan vs diri sendiri).
7. Mode latihan adaptif (session builder dari bank via band P(correct)).
8. Log response time per jawaban (sinyal kepercayaan untuk Elo/FSRS).
9. Evaluasi migrasi FSRS-6 → FSRS-7 (bila data review sudah cukup).

**Jangan pernah:** pindah ke HLR; hearts; liga multiplayer palsu; notifikasi
bandit; LSTM Birdbrain V2.

## 6. Hal yang harus diverifikasi sebelum membangun (gap)

1. Apakah Elo soal ikut bergerak setelah attempt (K-factor item)? — dari implementasi.
2. Apakah target daily goal sudah bisa diatur pengguna?
3. Apa yang dilakukan tombol "Ronde Legendary" di popover node?
4. Apakah XP tampil langsung di layar payoff?
5. Apakah FSRS-6 memakai parameter default atau sudah dioptimasi per-user?

## 7. Sumber

- Settles, B. & Meeder, B. (2016). *A Trainable Spaced Repetition Model for
  Language Learning.* ACL 2016, pp. 1848–1858. + Duolingo blog, "How we learn
  how you learn" (blog.duolingo.com/how-we-learn-how-you-learn/) — dibaca
  langsung 13 Nov 2026. + kode/data: github.com/duolingo/halflife-regression.
- Ilídio, P. et al. (2026). *Revisiting Half-Life Regression for Explainable and
  Personalized Spaced Repetition in Duolingo.* PMLR 339:217–227, IRAISE 2026 —
  abstrak + hasil dibaca dari PDF PMLR.
- Duolingo blog (2020), "Learning how to help you learn: introducing Birdbrain"
  — dikutip via riset loxelingo + wawancara Bicknell; >20% pelajaran
  terpersonalisasi per Okt 2020.
- Bicknell, K. (Head of AI, Duolingo), wawancara — IndiaAI: Birdbrain = RNN,
  memprediksi P(correct), menjaga soal di "intermediate difficulty range".
- IEEE Spectrum (profil teknis Birdbrain, via Settles): LSTM 40-dim, update
  setiap exercise — dikutip via kajian sekunder.
- McCarthy et al. (2021). *Jump-Starting Item Parameters for Adaptive Language
  Tests.* EMNLP 2021 (research.duolingo.com) — publikasi algoritma Duolingo
  terakhir yang terlacak.
- Open Spaced Repetition, **srs-benchmark** (GitHub): tabel log loss / RMSE /
  AUC (9.999 koleksi, ~350 jt review evaluasi) — angka dikutip dari repo +
  tiga kajian independen yang mereproduksinya.
- Anki Manual / FSRS docs: FSRS default di Anki 23.10+, desired retention
  default 90%.
- Loxelingo research doc 02-ml-and-naming.md (2026-08-05): publikasi algoritma
  Duolingo berhenti setelah 2021; angka benchmark HLR 0,4694 vs FSRS-6 0,3460.
- Trophy.so, "Duolingo Gamification Strategy: A Full Case Study (2026)":
  liga ~30 orang, 10 tier; angka freeze 4,5× adalah angka Trophy, bukan Duolingo.
- Uladshauchenka, "Duolingo Case Study: The Gamification of Learning":
  10 tier liga sampai Diamond; contextual bandit ~200 jt reminder.
- Laporan sebelumnya: `~/workspace/research_notes/duolingo-ui-algoritma-20261113/report.md`.
