# Latihan CPNS Hari 21 — Jumat, 27 November 2026
**Fokus: TIU Figural HARD + penalaran matriks 3×3 multi-perspektif · 30 soal BARU · Target: ≥24/30 benar (~120 poin TIU) · Waktu soal: ~50 menit, total sesi ~2 jam termasuk pelajaran & koreksi**

*Sesuai rotasi mingguan: Jumat = TIU figural. Semua 30 soal di bawah ini BARU — tidak satu pun mendaur ulang soal figural Hari 2, Hari 2b, Hari 3, Hari 8, Hari 14, Hari 15, Hari 16, maupun Simulasi Penuh 14 Nov dan paket kalibrasi 26 Nov (Q2-rev). Soal dibuat dari pola yang sama dengan soal SKD 2023–2024 (bukan soal resmi BKN — BKN tidak mempublikasikan soal SKD). Di aplikasi web, soal-soal ini dikerjakan dengan klik dan tampil sebagai GAMBAR (diagram SVG); file ini adalah arsip + sumber transkripsi aplikasi.*

## Pelajaran fundamental: TIU figural HARD

### 0. Pemanasan 60 detik — tiga pola lemah dari buku kesalahan
- **Simulasi No. 56 (matriks XOR):** ○△ + △□ → ○□. Aturannya: bentuk yang muncul di KEDUA kotak pertama DIHAPUS, sisanya dipertahankan. Uji di baris 1 dan 2 sebelum menebak baris 3.
- **Bedah HOTS No. 5 (matriks kombinasi kolom + rotasi):** dua atribut berjalan bersamaan — lacak rotasi dan isi sebagai dua pola terpisah, jangan dicampur.
- **Hari 2b No. 13 (pencerminan):** cermin kiri-kanan hanya mengubah arah HORIZONTAL — panah vertikal (↑/↓) tidak berubah saat dicerminkan kiri-kanan; cermin atas-bawah hanya mengubah arah VERTIKAL.
- Ketiga soal ini ada di buku kesalahanmu (26 kartu jatuh tempo hari ini) — ulangi lewat mode FSRS di tab Buku.

### 1. Penalaran matriks 3×3 (2026): dua aturan independen, multi-perspektif
Di KepmenPANRB 674/2026, slot ketidaksamaan digantikan penalaran matriks: grid 3×3 dengan 1 sel kosong yang menuntut analisis pola multi-perspektif — DILARANG menghitung odd-one-out sebagai matriks. Soal HARD memakai DUA atribut yang berubah bersamaan: (a) **rotasi per baris + pergeseran/superposisi per kolom** (pelajaran Q2-rev paket kalibrasi 26 Nov: pisahkan keduanya sejak awal); (b) **bentuk ikut kotak 1 + isi ikut kotak 2** (superposisi atribut); (c) **jumlah/selisih** (jumlah sisi tetap, selisih antarkolom, jumlah titik = jumlah dua kotak sebelumnya); (d) **bujur sangkar Latin** (tiap baris/kolom memuat tiap nilai tepat sekali). Cara kerja: selesaikan SATU atribut sampai tuntas (tulis angkanya: sisi 3-4-5, titik 1-2-3), baru atribut kedua. Jangan menebak keduanya sekaligus.
- **XOR (yang kembar hilang):** kotak ketiga = bentuk yang muncul di tepat SATU kotak sebelumnya. Bentuk yang muncul di kedua kotak DIHAPUS. Hitung kemunculan tiap bentuk: 2 kali → hilang, 1 kali → lolos.
- **Jumlah tetap:** jumlah sisi / jumlah elemen tiap baris atau kolom selalu sama. Tulis angkanya di samping tiap bangun sebelum menjumlah — mata mudah tertipu, angka tidak.

### 2. Serial HARD: satu daftar per pola
Satu panel bisa membawa dua atau tiga pola sekaligus: arah berputar + jumlah berselisih + isi bersiklus. Cara kerja: buat SATU daftar per pola (daftar arah, daftar jumlah, daftar isi) dan selesaikan masing-masing. Jawaban yang hanya benar satu polanya adalah jebakan yang sengaja dipasang.
- **Putaran 45° punya 8 arah** — tuliskan derajatnya (0, 45, 90, … 315) agar ↙ (225°) tidak tertukar dengan ↖ (315°).
- **Isi bersiklus** (penuh → setengah → kosong, atau penuh–kosong bergantian) dan **titik bersiklus** (0–1–2) — kelompokkan panel berpasangan sebelum menyimpulkan; jangan kira siklusnya kembali ke awal tiap 4 langkah.

### 3. Analogi gambar: transformasi GANDA (pola lemah simulasi!)
Soal HARD memakai transformasi DUA lapis sekaligus (tiga lapis untuk satu soal brutal): putar + balik isi, sisi +/−1/2 + balik isi, ganda + cermin, sisi + putar. Cara kerja: baca A → B, tulis KEDUA lapisnya, lalu terapkan KEDUA-DUANYA ke C. Bangun simetris menyembunyikan putaran: lingkaran diputar tetap lingkaran, belah ketupat diputar 180° tetap belah ketupat, persegi diputar 90° tetap persegi — di situlah jebakannya. Cermin kiri-kanan membalik → menjadi ← (bukan ↘); cermin atas-bawah membalik ↑ menjadi ↓.

### 4. Aturan main sesi ini
- Kerjakan di aplikasi (klik). Tandai soal yang ragu dan lewati — kembali di akhir. Jangan kosongkan soal.
- Soal yang salah masuk buku kesalahan (diulang 3 hari kemudian, Senin 30 Nov).
- **Ulangan:** Hari 18 dan Hari 19 belum dijawab Sandi, jadi tidak ada soal ulangan hari ini. 26 kartu buku kesalahan jatuh tempo — kerjakan lewat mode FSRS di tab Buku.

---

## Soal — Bagian A: Penalaran matriks 3×3 (Soal 1–12)

**1.** Perhatikan matriks 3×3 berikut. Bentuk yang tepat untuk mengisi kotak bertanda ? adalah…

*■● | ◆▲ | ■▲
◆● | ■▲ | ◆▲
■◆ | ◆■ | ?*

A. ◆▲
B. ■◆
C. ●◆
D. ■▲
E. ◆●

**Kunci: B — ■◆.** (1) B karena per kolom berlaku XOR: bentuk yang muncul di kedua kotak atas dihapus, sisanya dipertahankan; kolom 3: ■▲ dan ◆▲ — ▲ muncul dua kali (dihapus), tersisa ■◆. (2) Uji kolom 1: ■● dan ◆● — ● terhapus, tersisa ■◆, cocok dengan kotak baris 3 kolom 1; kolom 2 pun cocok: ◆▲ dan ■▲ → ◆■. (3) Trik: pada matriks XOR, hitung kemunculan tiap bentuk per kolom — muncul 2 kali berarti hilang, muncul 1 kali berarti lolos ke kotak ketiga.
**Jebakan:** Menjawab ◆▲ karena menyalin kotak baris 2 kolom 3 — XOR menghapus bentuk yang muncul di kedua kotak (▲ muncul dua kali di kolom 3), jadi jawaban harus hasil penghapusan, bukan salinan.

**2.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu panah dan satu lingkaran kecil. Panah dan lingkaran yang tepat untuk mengisi kotak bertanda ? adalah…

*▶● | ▲○ | ◀●
▼● | ▶○ | ▲●
◀● | ▼○ | ?*

A. ◀ + ○
B. ▲ + ●
C. ▶ + ○
D. ▼ + ●
E. ▶ + ●

**Kunci: E — ▶ + ●.** (1) E karena dua aturan berjalan bersamaan: panah berputar 90° berlawanan arah jarum jam tiap langkah ke kanan (◀ → ▼ → ▶) dan isi lingkaran kecil mengikuti kolom (kolom 1 penuh, kolom 2 kosong, kolom 3 penuh), jadi kotak terakhir adalah ▶ dengan lingkaran penuh. (2) Uji baris 1: ▶ → ▲ → ◀ (putaran berlawanan arah jarum jam konsisten) dengan lingkaran penuh–kosong–penuh; baris 2 pun sama: ▼ → ▶ → ▲ dengan isi yang sama. (3) Trik: matriks dua atribut — lacak arah putaran dan isi sebagai dua pola terpisah, dan periksa arah putaran dari baris yang sudah lengkap sebelum menebak.
**Jebakan:** Menjawab ▶ + ○ karena panahnya benar tetapi lingkarannya dikira kosong — kolom 3 selalu penuh, dibuktikan baris 1 dan 2.

**3.** Perhatikan matriks 3×3 berikut. Bangun yang tepat untuk mengisi kotak bertanda ? adalah…

*△(3) | ⬟(7) | ⬢(8)
⬠(5) | ⬡(6) | ⬟(7)
□(4) | ⬢(8) | ?*

A. ⬡ (6 sisi)
B. ⬟ (7 sisi)
C. ⬠ (5 sisi)
D. □ (4 sisi)
E. △ (3 sisi)

**Kunci: A — ⬡ (6 sisi).** (1) A karena jumlah sisi tiap baris selalu 18: baris 3 sudah bersisi 4 + 8 = 12, jadi kotak yang hilang harus bersisi 6, yaitu segienam. (2) Uji baris 1: 3 + 7 + 8 = 18; baris 2: 5 + 6 + 7 = 18 — aturannya terbukti di dua baris lengkap. (3) Trik: soal 'jumlah sisi' selalu minta dihitung, bukan ditebak dari posisi — tulis angkanya di samping tiap bangun sebelum menjumlah.
**Jebakan:** Menjawab ⬟ (7 sisi) karena 7 adalah sisi yang paling sering muncul — frekuensi kemunculan bukan aturan; yang dijaga tetap adalah jumlah sisi per baris (18).

**4.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu bangun dengan isi penuh atau kosong. Bangun yang tepat untuk mengisi kotak bertanda ? adalah…

*▲(penuh) | □(kosong) | △(kosong)
○(kosong) | ◆(penuh) | ●(penuh)
◆(penuh) | △(kosong) | ?*

A. ◆ (penuh)
B. △ (kosong)
C. ◇ (kosong)
D. ▲ (penuh)
E. ○ (kosong)

**Kunci: C — ◇ (kosong).** (1) C karena kotak ketiga mengambil bentuk dari kotak pertama dan isi dari kotak kedua: baris 3 mengambil bentuk ◆ dari kotak pertama dan isi kosong dari kotak kedua, jadi ◇ (belah ketupat kosong). (2) Uji baris 1: bentuk ▲ dari kotak pertama + isi kosong dari kotak kedua = △ kosong, cocok; baris 2: bentuk ● dari kotak pertama + isi penuh dari kotak kedua = ● penuh, cocok. (3) Trik: bila bentuk dan isi berubah tidak sejalan, pisahkan keduanya — tanyakan 'bentuknya ikut kotak mana?' dan 'isinya ikut kotak mana?' secara terpisah.
**Jebakan:** Menjawab ◆ (penuh) karena menyalin bentuk sekaligus isi kotak pertama baris 3 — isi kotak ketiga mengikuti kotak kedua (kosong), bukan kotak pertama.

**5.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu panah dan sejumlah titik. Isi yang tepat untuk kotak bertanda ? adalah…

*↑•• | →• | ↓•••
←• | ↑••• | →••
↓••• | ←•• | ?*

A. ↑ + 2 titik
B. ↑ + 1 titik
C. → + 1 titik
D. ← + 1 titik
E. ↑ + 3 titik

**Kunci: B — ↑ + 1 titik.** (1) B karena dua aturan berjalan bersamaan: panah berputar 90° berlawanan arah jarum jam tiap langkah ke bawah (kolom 3: ↓ → → → ↑) dan jumlah titik tiap kolom selalu 6 (kolom 3 sudah membawa 3 + 2 = 5, jadi tersisa 1). (2) Uji kolom 1 ke bawah: ↑ → ← → ↓ (putaran berlawanan arah jarum jam konsisten) dengan titik 2 + 1 + 3 = 6; kolom 2 pun cocok: → → ↑ → ← dengan titik 1 + 3 + 2 = 6. (3) Trik: matriks dua atribut — selesaikan satu atribut sampai tuntas (mis. panahnya dulu), baru atribut kedua; jangan menebak keduanya sekaligus.
**Jebakan:** Menjawab ↑ + 2 titik karena titiknya dikira mengikuti baris dari kiri — jumlah titik dijaga tetap 6 per kolom; kolom 3 sudah membawa 5 titik, jadi yang tersisa adalah 1, bukan 2.

**6.** Perhatikan matriks 3×3 berikut. Bangun yang tepat untuk mengisi kotak bertanda ? adalah…

*⬢(8) | ⬠(5) | △(3)
⬟(7) | △(3) | □(4)
⬢(8) | △(3) | ?*

A. △ (3 sisi)
B. □ (4 sisi)
C. ⬡ (6 sisi)
D. ⬠ (5 sisi)
E. ⬟ (7 sisi)

**Kunci: D — ⬠ (5 sisi).** (1) D karena jumlah sisi kotak ketiga adalah selisih jumlah sisi dua kotak sebelumnya: baris 3 adalah 8 − 3 = 5, yaitu segilima. (2) Uji baris 1: 8 − 5 = 3 (segitiga), cocok; baris 2: 7 − 3 = 4 (persegi), cocok — aturannya terbukti di dua baris lengkap. (3) Trik: bila angka sisinya tidak dijumlahkan menjadi total tetap, curigai operasi selisih — hitung kolom 1 dikurangi kolom 2 di tiap baris sebelum menebak.
**Jebakan:** Menjawab □ (4 sisi) karena mengira selisihnya tetap 4 — selisih dihitung per baris dari angka baris itu sendiri (8 − 3 = 5), bukan nilai tetap dari baris lain.

**7.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu segitiga dan sejumlah titik. Isi yang tepat untuk kotak bertanda ? adalah…

*▲• | ▶••• | ▼••
▶•• | ▼• | ◀•••
▼••• | ◀•• | ?*

A. ▲ + 2 titik
B. ▶ + 1 titik
C. ▼ + 1 titik
D. ▲ + 3 titik
E. ▲ + 1 titik

**Kunci: E — ▲ + 1 titik.** (1) E karena dua aturan independen berjalan bersamaan: segitiga berputar 90° searah jarum jam tiap langkah ke kanan (baris 3: ▼ → ◀ → ▲) dan jumlah titik membentuk bujur sangkar Latin per kolom (kolom 3: 2, 3, → 1). (2) Uji baris 1: ▲ → ▶ → ▼ (putaran konsisten) dengan titik 1, 3, 2; kolom 1: titik 1, 2, 3 lengkap — kedua pola terbukti di baris dan kolom yang sudah lengkap. (3) Trik: soal brutal dua aturan — pisahkan keduanya sejak awal (daftar arah, daftar jumlah) dan jawab hanya bila KEDUA daftar menunjuk opsi yang sama.
**Jebakan:** Menjawab ▶ + 1 titik karena memutar segitiga ke bawah mengikuti kolom — putaran segitiga berjalan per baris (ke kanan), sedangkan titik berjalan per kolom (ke bawah); keduanya harus dicek terpisah.

**8.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi beberapa bangun yang sama. Isi yang tepat untuk kotak bertanda ? adalah…

*◆◆ | ○ | □□□
□ | ◆◆◆ | ○○
○○○ | □□ | ?*

A. ◆ (1 buah)
B. ○ (1 buah)
C. ◆◆ (2 buah)
D. □ (1 buah)
E. ○○ (2 buah)

**Kunci: A — ◆ (1 buah).** (1) A karena tiap baris jumlah elemennya selalu 6 dan tiap baris memuat ketiga bentuk tepat sekali: baris 3 sudah membawa ○○○ (3) dan □□ (2), jadi yang hilang adalah 1 belah ketupat. (2) Uji baris 1: 2 + 1 + 3 = 6 dengan bentuk ◆, ○, □; baris 2 pun cocok: 1 + 3 + 2 = 6 dengan ketiga bentuk yang sama. (3) Trik: bila kotaknya berisi banyak bangun yang sama, hitung JUMLAHNYA dulu dan periksa bentuknya — jawaban harus lolos kedua pemeriksaan itu.
**Jebakan:** Menjawab ○ (1 buah) karena menyalin bentuk kolom 3 baris 2 — tiap baris harus memuat ketiga bentuk tepat sekali; baris 3 sudah punya ○ dan □, jadi yang hilang adalah ◆.

**9.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu bangun dengan isi penuh, kosong, atau setengah. Bangun yang tepat untuk mengisi kotak bertanda ? adalah…

*▲(penuh) | □(kosong) | ◐(setengah)
□(kosong) | ◐(setengah) | ▲(penuh)
◐(setengah) | ▲(penuh) | ?*

A. ■ (penuh)
B. ○ (kosong)
C. □ (kosong)
D. △ (kosong)
E. ○ (setengah)

**Kunci: C — □ (kosong).** (1) C karena dua aturan berjalan berlawanan arah: bentuk membentuk bujur sangkar Latin per kolom (kolom 3: ○ → ▲ → □) dan isi berotasi per baris ke kanan (baris 3: setengah → penuh → kosong), jadi kotak terakhir adalah persegi kosong. (2) Uji kolom 1 ke bawah: ▲ → □ → ○ (ketiga bentuk lengkap); baris 1 ke kanan: penuh → kosong → setengah (ketiga isi lengkap) — kedua pola terbukti di jalur yang sudah lengkap. (3) Trik: bila dua atribut bergerak ke arah berbeda, lacak masing-masing pada jalurnya sendiri — bentuk ikut kolom, isi ikut baris, jangan dicampur.
**Jebakan:** Menjawab ■ (penuh) karena bentuknya benar tapi isinya mengikuti kolom — isi berotasi per baris, bukan per kolom; baris 3 menuntut isi kosong.

**10.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu bangun dan sejumlah titik. Isi yang tepat untuk kotak bertanda ? adalah…

*▲• | ▲•• | ▲•••
■•• | ■• | ■•••
●••• | ●•• | ?*

A. ● + 4 titik
B. ● + 5 titik
C. ● + 3 titik
D. ● + 2 titik
E. ▲ + 5 titik

**Kunci: B — ● + 5 titik.** (1) B karena jumlah titik kotak ketiga adalah jumlah titik dua kotak sebelumnya: baris 3 adalah 3 + 2 = 5, dan bentuknya mengikuti baris (lingkaran), jadi ● + 5 titik. (2) Uji baris 1: 1 + 2 = 3 titik, cocok; baris 2: 2 + 1 = 3 titik, cocok — aturannya terbukti di dua baris lengkap. (3) Trik: bila tiap baris memakai satu bentuk yang sama, bentuknya bukan pola — polanya ada pada angkanya; jumlahkan titik dua kotak pertama sebelum menebak.
**Jebakan:** Menjawab ● + 4 titik karena mengira titiknya naik 1 tiap baris — titik kolom 3 adalah jumlah dua kolom sebelumnya (3 + 2 = 5), bukan kelanjutan barisan.

**11.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu bangun dan satu lingkaran kecil. Bangun dan lingkaran yang tepat untuk mengisi kotak bertanda ? adalah…

*△● | □◐ | ⬠○
□◐ | ⬠○ | ⬡●
⬠○ | ⬡● | ?*

A. ⬟ (7 sisi) + ●
B. ⬡ (6 sisi) + ◐
C. ⬟ (7 sisi) + ○
D. ⬢ (8 sisi) + ◐
E. ⬟ (7 sisi) + ◐

**Kunci: E — ⬟ (7 sisi) + ◐.** (1) E karena dua aturan independen berjalan bersamaan: jumlah sisi naik 1 tiap langkah ke kanan (baris 3: 5, 6, → 7 = segitujuh) dan isi lingkaran kecil berotasi tiap langkah ke bawah (kolom 3: kosong → penuh → setengah). (2) Uji baris 1: sisi 3, 4, 5 naik 1; kolom 1 ke bawah: penuh → setengah → kosong (siklus isi konsisten) — kedua pola terbukti di jalur yang sudah lengkap. (3) Trik: soal brutal dua aturan — pisahkan keduanya sejak awal (daftar sisi, daftar isi) dan jawab hanya bila KEDUA daftar menunjuk opsi yang sama.
**Jebakan:** Menjawab ⬟ + ● karena sisinya benar tetapi isinya mengikuti baris — isi lingkaran berubah per kolom (ke bawah), bukan per baris; kolom 3 menuntut isi setengah.

**12.** Perhatikan matriks 3×3 berikut. Tiap kotak berisi satu bangun dan sejumlah titik. Isi yang tepat untuk kotak bertanda ? adalah…

*△• | ⬡•• | ⬟•
⬠•• | □• | ⬠•••
⬢•• | ⬡•• | ?*

A. □ + 2 titik
B. ⬠ + 1 titik
C. △ + 1 titik
D. □ + 1 titik
E. □ + 3 titik

**Kunci: D — □ + 1 titik.** (1) D karena dua total dijaga tetap per kolom: jumlah sisi kolom 3 sudah 7 + 5 = 12 (butuh 4 → persegi) dan jumlah titik kolom 3 sudah 1 + 3 = 4 (butuh 1), jadi □ + 1 titik. (2) Uji kolom 1: sisi 3 + 5 + 8 = 16 dan titik 1 + 2 + 2 = 5; kolom 2: sisi 6 + 4 + 6 = 16 dan titik 2 + 1 + 2 = 5 — kedua total terbukti di dua kolom lengkap. (3) Trik: bila dua angka dijaga tetap sekaligus, hitung keduanya sebagai total kolom — jawaban harus lolos KEDUA total, bukan salah satu.
**Jebakan:** Menjawab □ + 2 titik karena sisinya benar tapi titiknya tidak dihitung — total titik per kolom adalah 5; kolom 3 sudah membawa 4 titik, jadi yang tersisa adalah 1, bukan 2.

## Soal — Bagian B: Serial gambar (Soal 13–21)

**13.** Perhatikan urutan gambar berikut. Gambar berikutnya yang tepat adalah…

*↑ | ↗• | →•• | ↘ | ?*

A. ↓
B. ↓ + 1 titik
C. ↓ + 2 titik
D. ↘ + 1 titik
E. ↑ + 1 titik

**Kunci: B — ↓ + 1 titik.** (1) B karena dua pola berjalan bersamaan: panah berputar 45° searah jarum jam (↘ → ↓) dan jumlah titik bersiklus 0–1–2 (0, 1, 2, 0 → 1), jadi gambar kelima adalah ↓ dengan 1 titik. (2) Uji putaran: 0°, 45°, 90°, 135° → 180°; uji titik: 0, 1, 2, 0 → 1 — kedua pola konsisten di keempat panel. (3) Trik: putaran 45° punya 8 arah — tuliskan derajatnya agar ↘ tidak tertukar dengan ↙; titik yang bersiklus dilacak sebagai daftar terpisah.
**Jebakan:** Menjawab ↓ karena arahnya benar tetapi titiknya dikira tetap 0 — titik bersiklus 0–1–2, jadi langkah kelima membawa 1 titik.

**14.** Perhatikan urutan gambar berikut. Gambar berikutnya yang tepat adalah…

*△ (3 sisi) | ⬠ (5 sisi) | □ (4 sisi) | ⬡ (6 sisi) | ?*

A. ⬟ (7 sisi)
B. ⬢ (8 sisi)
C. □ (4 sisi)
D. ⬠ (5 sisi)
E. ⬡ (6 sisi)

**Kunci: D — ⬠ (5 sisi).** (1) D karena jumlah sisi mengikuti selisih +2 lalu −1 berulang: 3, 5, 4, 6, → 5, jadi bangun kelima adalah segilima. (2) Uji selisih: 3→5 (+2), 5→4 (−1), 4→6 (+2) — selisih berikutnya −1 sehingga 6−1=5. (3) Trik: bila jumlahnya naik-turun, tulis SELISIH antar langkah — selisih yang berulang adalah polanya.
**Jebakan:** Menjawab ⬟ karena mengira sisinya naik 1 tiap dua langkah (3, 4, 5, …) — selisih sebenarnya +2 lalu −1, bukan +1.

**15.** Perhatikan urutan gambar berikut. Gambar berikutnya yang tepat adalah…

*▲▲ | ●●● | ■■■■■ | ▲▲▲▲▲▲▲ | ?*

A. 11 buah ●
B. 11 buah ▲
C. 13 buah ●
D. 7 buah ●
E. 11 buah ■

**Kunci: A — 11 buah ●.** (1) A karena dua pola berjalan bersamaan: bentuk bergantian tiga macam (▲, ●, ■, ▲, → ●) dan jumlah mengikuti bilangan prima (2, 3, 5, 7, → 11), jadi gambar kelima adalah 11 buah ●. (2) Uji bentuk: langkah 1 ▲, 2 ●, 3 ■, 4 ▲ — siklus tiga bentuk kembali ke ● di langkah 5; uji jumlah: 2, 3, 5, 7 adalah empat prima pertama berurutan, prima berikutnya 11. (3) Trik: bila jumlahnya melompat tidak tetap, curigai bilangan prima — tulis daftar primanya (2, 3, 5, 7, 11, 13) sebelum memilih.
**Jebakan:** Menjawab 11 buah ▲ karena jumlahnya benar tetapi bentuknya salah — bentuk bersiklus tiga (▲●■), jadi langkah kelima kembali ke ●, bukan ▲.

**16.** Perhatikan urutan gambar berikut. Tiap gambar berisi dua panah. Gambar berikutnya yang tepat adalah…

*↑→ | →↑ | ↓← | ←↓ | ?*

A. ↓←
B. ←↓
C. ↑→
D. →↑
E. ↓→

**Kunci: C — ↑→.** (1) C karena dua panah berputar berlawanan arah: panah pertama berputar 90° searah jarum jam (← → ↑) dan panah kedua berputar 90° berlawanan arah jarum jam (↓ → →), jadi gambar kelima adalah ↑→. (2) Uji panah pertama: ↑, →, ↓, ← → ↑; uji panah kedua: →, ↑, ←, ↓ → → — kedua putaran konsisten di keempat panel. (3) Trik: bila ada dua elemen yang bergerak, lacak SATU elemen sampai tuntas, baru elemen kedua — jangan menebak keduanya sekaligus.
**Jebakan:** Menjawab →↑ karena kedua panahnya tertukar posisinya — yang berputar searah jarum jam adalah panah PERTAMA (kiri); panah kedua bergerak berlawanan arah.

**17.** Perhatikan urutan gambar berikut. Tiap gambar berisi satu bangun dengan satu titik kecil di sudutnya. Gambar berikutnya yang tepat adalah…

*▲ (titik kiri atas) | ▼ (titik kanan atas) | ▲ (titik kanan bawah) | ▼ (titik kiri bawah) | ?*

A. ▲ + titik kanan atas
B. ▼ + titik kiri atas
C. ▲ + titik kanan bawah
D. ▼ + titik kanan bawah
E. ▲ + titik kiri atas

**Kunci: E — ▲ + titik kiri atas.** (1) E karena dua pola berjalan bersamaan: segitiga berputar 180° tiap langkah (▼ → ▲) dan titik sudut bergerak searah jarum jam (kiri bawah → kiri atas), jadi gambar kelima adalah ▲ dengan titik di kiri atas. (2) Uji segitiga: ▲, ▼, ▲, ▼ → ▲; uji titik: kiri atas, kanan atas, kanan bawah, kiri bawah → kiri atas — kedua pola konsisten di keempat panel. (3) Trik: serial dua elemen — buat dua daftar terpisah (daftar bentuk, daftar posisi) dan selesaikan masing-masing.
**Jebakan:** Menjawab ▼ + titik kiri atas karena titiknya benar tetapi segitiganya dikira tetap ▼ — segitiga berputar 180° tiap langkah, jadi langkah kelima kembali ke ▲.

**18.** Perhatikan urutan gambar berikut. Tiap gambar berisi dua bangun yang sama. Gambar berikutnya yang tepat adalah…

*△△ (kosong) | □□ (penuh) | ⬠⬠ (kosong) | ⬡⬡ (penuh) | ?*

A. ⬟⬟ (penuh)
B. ⬟⬟ (kosong)
C. ⬡⬡ (penuh)
D. ⬡⬡ (kosong)
E. ⬠⬠ (kosong)

**Kunci: B — ⬟⬟ (kosong).** (1) B karena tiga pola berjalan bersamaan: tiap panel berisi dua bangun kembar, jumlah sisinya naik 1 (6 → 7), dan isinya bergantian kosong–penuh (kosong, penuh, kosong, penuh → kosong), jadi gambar kelima adalah dua segitujuh kosong. (2) Uji sisi: 3, 4, 5, 6 → 7; uji isi: kosong, penuh, kosong, penuh → kosong; uji kekembaran: tiap panel selalu dua bangun yang sama. (3) Trik: bila tiga atribut berubah sekaligus, tulis ketiganya sebagai daftar kecil (sisi, isi, jumlah bangun) — jawaban harus lolos KETIGA daftar, bukan salah satu.
**Jebakan:** Menjawab ⬟⬟ penuh karena sisi dan kekembarannya benar tetapi isinya dikira bergantian mulai penuh — isi di sini bergantian mulai kosong, jadi langkah kelima kembali kosong.

**19.** Perhatikan urutan gambar berikut. Gambar berikutnya yang tepat adalah…

*↑• | →•• | ↓•••• | ←••••• | ?*

A. ↑ + 6 titik
B. → + 7 titik
C. ↑ + 5 titik
D. ↑ + 7 titik
E. ← + 7 titik

**Kunci: D — ↑ + 7 titik.** (1) D karena dua pola berjalan bersamaan: panah berputar 90° searah jarum jam (← → ↑) dan jumlah titik berselisih +1 lalu +2 berulang (5 → 7), jadi gambar kelima adalah ↑ dengan 7 titik. (2) Uji panah: ↑, →, ↓, ← → ↑; uji titik: 1, 2, 4, 5 → 7 dengan selisih +1, +2, +1, +2. (3) Trik: bila angkanya naik tidak tetap, tulis SELISIH antar langkah — selisih berlapis +1 lalu +2 adalah polanya.
**Jebakan:** Menjawab ↑ + 6 titik karena arahnya benar tetapi titiknya dikira naik 1 tiap langkah — titiknya berselisih +1 lalu +2 berulang, jadi langkah kelima membawa 7 titik, bukan 6.

**20.** Perhatikan urutan gambar berikut. Gambar berikutnya yang tepat adalah…

*▲••••• | ▶•••• | ▼••• | ◀•• | ?*

A. ▲ + 1 titik
B. ▶ + 1 titik
C. ▲ + 2 titik
D. ▼ + 1 titik
E. ◀ + 1 titik

**Kunci: A — ▲ + 1 titik.** (1) A karena dua pola berjalan bersamaan: segitiga berputar 90° searah jarum jam (◀ → ▲) dan jumlah titik berkurang 1 tiap langkah (2 → 1), jadi gambar kelima adalah ▲ dengan 1 titik. (2) Uji putaran: 0°, 90°, 180°, 270° → 0°; uji titik: 5, 4, 3, 2 → 1 — kedua pola konsisten di keempat panel. (3) Trik: serial dua pola — lacak tiap pola sampai langkah terakhir sebelum memilih; jawaban yang hanya benar satu polanya adalah jebakan.
**Jebakan:** Menjawab ▲ + 2 titik karena arahnya benar tetapi titiknya dikira tetap — titiknya berkurang 1 tiap langkah, jadi langkah kelima hanya membawa 1 titik.

**21.** Perhatikan urutan gambar berikut. Tiap gambar berisi satu persegi dengan satu titik kecil di sudutnya. Gambar berikutnya yang tepat adalah…

*■ (titik kiri atas) | ■ (titik kiri bawah) | □ (titik kanan bawah) | □ (titik kanan atas) | ?*

A. ■ + titik kanan atas
B. □ + titik kiri atas
C. ■ + titik kiri atas
D. ■ + titik kiri bawah
E. □ + titik kanan bawah

**Kunci: C — ■ + titik kiri atas.** (1) C karena dua pola berjalan bersamaan: isi persegi berubah tiap dua langkah (kosong, kosong, → penuh) dan titik sudut bergerak berlawanan arah jarum jam (kanan atas → kiri atas), jadi gambar kelima adalah ■ dengan titik di kiri atas. (2) Uji isi: penuh, penuh, kosong, kosong → penuh; uji titik: kiri atas, kiri bawah, kanan bawah, kanan atas → kiri atas — kedua pola konsisten di keempat panel. (3) Trik: bila isi tidak bergantian tiap langkah, curigai pola 'berubah tiap dua langkah' — kelompokkan panel berpasangan sebelum menyimpulkan.
**Jebakan:** Menjawab □ + titik kiri atas karena titiknya benar tetapi isinya dikira tetap kosong — isi berubah tiap DUA langkah, jadi langkah kelima kembali penuh.

## Soal — Bagian C: Analogi gambar (Soal 22–30)

**22.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*▶(penuh) : ◀(kosong)  =  ◆(penuh) : ?*

A. ◇
B. ◆
C. □
D. ■
E. ◐

**Kunci: A — ◇.** (1) A karena transformasinya dua lapis: diputar 180° dan isinya dibalik. (2) Periksa pada A → B: ▶ penuh menjadi ◀ kosong — putaran 180° (90° menjadi 270°) dan isi penuh menjadi kosong sama-sama terjadi. (3) Trik: analogi dua lapis — tulis kedua lapisnya dari A → B sebelum menyentuh C; jawaban harus lolos kedua lapis sekaligus.
**Jebakan:** Menjawab ◆ karena putaran 180° pada belah ketupat tidak terlihat sehingga isinya dikira tetap penuh — padahal isi dibalik juga: penuh menjadi kosong.

**23.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*⬟(7 sisi) + → : ⬠(5 sisi) + ←  =  ⬡(6 sisi) + → : ?*

A. □ + →
B. □ + ←
C. ⬡ + ←
D. ⬠ + ←
E. ⬟ + ←

**Kunci: B — □ + ←.** (1) B karena transformasinya dua lapis: jumlah sisi berkurang 2 dan dicerminkan kiri-kanan. (2) Periksa pada A → B: segitujuh 7 sisi + → menjadi segilima 5 sisi + ← — sisi berkurang 2 dan panah berbalik arah oleh cermin kiri-kanan. (3) Trik: analogi dengan dua elemen — selesaikan elemen pertama (bangun) lalu elemen kedua (panah); jangan mencampur keduanya.
**Jebakan:** Menjawab □ + → karena hanya mengurangi sisi dan lupa mencerminkan panah — cermin kiri-kanan membalik → menjadi ←.

**24.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*▲(penuh) : ▼▼(penuh)  =  ↑(penuh) : ?*

A. ↑↑
B. ↓
C. ↓↓
D. ↑
E. →→

**Kunci: C — ↓↓.** (1) C karena transformasinya dua lapis: bangun digandakan dan dicerminkan atas-bawah. (2) Periksa pada A → B: ▲ menjadi ▼▼ — bangun digandakan dan salinannya dicerminkan atas-bawah menjadi ▼. (3) Trik: bila transformasinya melibatkan cermin, tanyakan dulu arah cerminnya — cermin atas-bawah membalik ↑ menjadi ↓, sedangkan cermin kiri-kanan tidak mengubahnya.
**Jebakan:** Menjawab ↑↑ karena hanya menggandakan dan lupa mencerminkan — cermin atas-bawah membalik ↑ menjadi ↓.

**25.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*▲(penuh) : ⬠(kosong)  =  □(penuh) : ?*

A. ⬡ (penuh)
B. ⬠ (kosong)
C. □ (kosong)
D. ⬡ (kosong)
E. ⬟ (kosong)

**Kunci: D — ⬡ (kosong).** (1) D karena transformasinya dua lapis: bangun bertambah 2 sisi dan isinya dibalik (penuh menjadi kosong). (2) Periksa pada A → B: ▲ 3 sisi penuh menjadi ⬠ 5 sisi kosong — sisi bertambah 2 dan isi dibalik sama-sama terjadi. (3) Trik: hitung SISI sebagai angka (3→5, 4→6) dan isi sebagai dua keadaan — dua daftar kecil, satu jawaban.
**Jebakan:** Menjawab ⬡ penuh karena hanya menambah sisi dan lupa membalik isi — isi dibalik juga: penuh menjadi kosong.

**26.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*▲(penuh) : ▶(kosong)  =  ▼(penuh) : ?*

A. ▶ (kosong)
B. ▼ (kosong)
C. ◀ (penuh)
D. ◐ (setengah)
E. ◀ (kosong)

**Kunci: E — ◀ (kosong).** (1) E karena transformasinya dua lapis: diputar 90° searah jarum jam dan isinya dibalik (penuh menjadi kosong). (2) Periksa pada A → B: ▲ penuh menjadi ▶ kosong — putaran 90° dan isi penuh menjadi kosong sama-sama terjadi. (3) Trik: analogi dua lapis — tulis kedua lapisnya dari A → B sebelum menyentuh C; jawaban harus lolos kedua lapis sekaligus.
**Jebakan:** Menjawab C (◀ penuh) karena putarannya benar tetapi isinya tidak dibalik — isi dibalik di kedua pasangan; menjawab A (▶ kosong) karena putarannya tertukar arah (berlawanan jarum jam).

**27.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*⬡(6 sisi) : ⬠⬠(5 sisi)  =  □(4 sisi) : ?*

A. △△
B. △
C. □□
D. ⬠⬠
E. △△△

**Kunci: A — △△.** (1) A karena transformasinya dua lapis: jumlah sisi berkurang 1 dan bangun digandakan. (2) Periksa pada A → B: ⬡ 6 sisi menjadi ⬠⬠ 5 sisi — sisi berkurang 1 dan jumlahnya menjadi dua. (3) Trik: analogi dua lapis — hitung JUMLAHNYA sebagai angka (1→2) dan sisinya sebagai angka (6→5); jawaban harus lolos keduanya.
**Jebakan:** Menjawab □□ karena hanya menggandakan dan lupa mengurangi sisi — transformasi −1 sisi berlaku juga pada C.

**28.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*▲(penuh) : ▽(kosong)  =  ▼(penuh) : ?*

A. ▼ (penuh)
B. ▽ (kosong)
C. △ (kosong)
D. ▲ (penuh)
E. ◀ (kosong)

**Kunci: C — △ (kosong).** (1) C karena transformasinya dua lapis: dicerminkan atas-bawah dan isinya dibalik. (2) Periksa pada A → B: ▲ penuh menjadi ▽ kosong — cermin atas-bawah membalik ▲ menjadi ▼ dan isi penuh menjadi kosong. (3) Trik: cermin atas-bawah hanya membalik arah VERTIKAL — segitiga menghadap atas menjadi menghadap bawah, sedangkan segitiga menghadap kanan tetap menghadap kanan.
**Jebakan:** Menjawab ▽ karena hanya membalik isi dan lupa mencerminkan — cermin atas-bawah membalik ▼ menjadi ▲.

**29.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*⬠(5 sisi) + ↑ : □(4 sisi) + →  =  ⬡(6 sisi) + ← : ?*

A. ⬠ + ←
B. ⬡ + ↑
C. ⬟ + ↑
D. ⬠ + ↑
E. ⬠ + →

**Kunci: D — ⬠ + ↑.** (1) D karena transformasinya dua lapis: bangun berkurang 1 sisi dan panah berputar 90° searah jarum jam. (2) Periksa pada A → B: ⬠ 5 sisi + ↑ menjadi □ 4 sisi + → — sisi berkurang 1 dan panah berputar 90° sama-sama terjadi. (3) Trik: analogi dengan dua elemen — selesaikan elemen pertama (bangun) lalu elemen kedua (panah); jangan mencampur keduanya.
**Jebakan:** Menjawab ⬠ + ← karena hanya mengurangi sisi dan lupa memutar panah — putaran 90° mengubah ← menjadi ↑.

**30.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…

*▲(penuh) : ▶▶(kosong)  =  ●●(penuh) : ?*

A. ●●●●
B. ○○
C. ●●
D. ◐◐◐◐
E. ○○○○

**Kunci: E — ○○○○.** (1) E karena transformasinya tiga lapis: jumlah bangun digandakan, diputar 90° searah jarum jam, dan isinya dibalik. (2) Periksa pada A → B: 1 segitiga penuh menjadi 2 segitiga kosong yang menghadap kanan — jumlah ×2, putaran 90°, dan isi penuh menjadi kosong sama-sama terjadi. (3) Trik: soal tiga lapis — kerjakan lapis demi lapis (jumlah, lalu putaran, lalu isi) dan coret opsi yang gagal di lapis mana pun.
**Jebakan:** Menjawab ●●●● karena jumlahnya benar tetapi isinya tidak dibalik — balik isi berlaku di kedua pasangan; putaran 90° pada lingkaran memang tidak terlihat, jadi periksa jumlah dan isinya.

---

## Setelah mengerjakan

- **Skor figural (Soal 1–30):** ___ / 30. Target: ≥24 (~120 poin TIU). Passing-grade konteks: TIU 35 soal, target aman 110/175.
- **Buku kesalahan:** soal yang salah masuk buku kesalahan dengan polanya (mis. "Soal 1 — matriks XOR, lupa hapus yang kembar"; "Soal 29 — analogi −1 sisi, lupa kurangi"). Soal salah diulang Senin, 30 Nov 2026.
- **Besok (Sabtu, 28 Nov, 10:00): tryout mini 30 soal campuran + review kesalahan** — ulangan soal salah Hari 19 (bila sudah dijawab).
- **Hari ini juga: pendaftaran CPNS 2026 DIBUKA (27 Nov 2026)** — daftar formasi per instansi belum terbit per cek 09:32 WIB; cek ulang 13:00 WIB terjadwal. Portal resmi satu-satunya: sscasn.bkn.go.id.

## Catatan verifikasi (untuk Mommy, sebelum sesi diterbitkan di aplikasi)

- **Distribusi kunci final (30 soal): A 6, B 6, C 6, D 6, E 6** (maks 20% per posisi). Tidak ada dua soal berurutan dengan kunci di posisi yang sama.
- **Verifikasi kunci:** Mommy memeriksa SEMUA 30 kunci sendiri dari spesifikasi gambar (figureJson), bukan dari klaim penyusun — 30/30 cocok; tiap aturan terbukti di minimal dua baris/kolom/panel lengkap; hanya satu opsi yang memenuhi aturan penuh per soal.
- **Perbaikan saat verifikasi (7 soal):** No. 2, 9, 11, 13, 18, 25, 26 ditulis ulang total oleh Mommy karena draf awal memakai kombinasi figure yang BELUM PERNAH terverifikasi tampil di aplikasi (isi pada panah; setengah pada persegi/poligon/segitiga; putaran pada poligon). Acuan keamanan: hanya kombinasi yang sudah tampil live di Hari 14 yang dipakai — isi hanya pada lingkaran (setengah), segitiga/persegi/belah ketupat/poligon (penuh/kosong), putaran hanya pada panah/segitiga. Kunci huruf ketujuh soal dipertahankan agar distribusi tetap A6/B6/C6/D6/E6.
- **Tidak mengulang soal:** dicek terhadap file Hari 1–20 + simulasi + set HOTS + paket kalibrasi 26 Nov — pola XOR, rotasi 45° matriks, jumlah sisi, analogi cermin, dan serial dua pola semuanya susunan BARU (aturan yang sama dengan Sim 56/59/62 dan HOTS No. 5 dipakai sebagai variasi, bukan soal identik).
- **Semua 30 soal figural memakai figureJson** (diagram SVG di aplikasi): matriks 12, serial 9, analogi 9 — tanpa satu pun soal figural tanpa gambar.
- **Kata terlarang:** 0× "tanpa", 0× "melewatkan" di seluruh teks soal/opsi/pembahasan (dicek otomatis).
- **Sesi live:** aplikasi slug `hari-21` (addSession 27 Nov 2026) — verifikasi via getSession setelah terbit.