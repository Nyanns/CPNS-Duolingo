# Riset: Skill GitHub + Desain Mobbin untuk Aplikasi Duolingo CPNS
Tanggal: 13 Nov 2026 (pagi). Permintaan Sandi (verbatim): "coba cari skill di github atau dimana dan desainnya cari di mobbin oke, agar ai mommy lebih canggih oke da coba teraapkan di web app kita".
Aplikasi: artifact `duolingo-cpns-latihan-soal-interaktif` (goal lolos-cpns). Status saat riset: v2 sudah diserahkan 12 Nov 21:08 (palet Duolingo slate-teal + amber, mode terang/gelap, mode "nilai langsung", bug buku kesalahan diperbaiki, sesi Bedah HOTS 10 soal LIVE, kotak Info CPNS Terbaru LIVE, updater harian 10:00 + cron cpns-daily-practice).

## A. SKILL GITHUB — yang membuat aplikasi lebih "pintar"

### A1. FSRS — Free Spaced Repetition Scheduler (PRIORITAS UTAMA)
- Proyek: open-spaced-repetition (open source). Versi terkini FSRS-6. Implementasi referensi: `ts-fsrs` (TypeScript).
- Model: DSR — Difficulty, Stability, Retrievability per kartu/soal. Setiap review diberi 1 dari 4 rating: Again / Hard / Good / Easy. Algoritma memprediksi kapan soal akan dilupakan lalu menjadwalkan review berikutnya di sekitar target retensi (default 0.90).
- Bukti: butuh 20–30% lebih sedikit review daripada SM-2/Leitner untuk retensi yang sama (data ratusan juta review log). Encode app: akurasi prediksi recall FSRS 89,6% vs SM-2 47,1%.
- Dipakai oleh: Anki (FSRS bawaan), Nibomo (FSRS-6 via ts-fsrs 5.2.3), OpenTutor (FSRS 4.5), KnowledgeForge (FSRS-6), Encode (menggantikan SM-2), GxP-Training-Bot (`attempts/fsrs.py`).
- **Yang diambil untuk aplikasi kita:** GANTI jadwal tetap buku kesalahan 1-3-7-14-30 hari dengan FSRS per soal. Aplikasi sudah menyimpan riwayat percobaan per soal — itu semua data yang FSRS butuhkan. Tambah UI rating 4 tombol (Lupa / Sulit / Lumayan / Mudah) di mode ulangan + antrean "jatuh tempo hari ini" di beranda. Ini satu-satunya upgrade yang benar-benar membuat aplikasi "lebih canggih" secara ilmiah, bukan kosmetik.

### A2. Elo rating untuk kesulitan soal + kemampuan murid (GxP-Training-Bot)
- Repo: https://github.com/kurapati-sai-suhas/gxp-training-bot (README terverifikasi).
- Ide: rating Elo seperti catur — setiap soal punya rating kesulitan hidup, setiap murid punya rating kemampuan hidup. Keduanya bergerak dari jawaban nyata, bukan tebakan AI sekali jadi. Dijalankan di dua granularitas: per keseluruhan materi DAN per bagian (satu bagian lemah tidak mereset bagian lain yang sudah dikuasai).
- **Yang diambil:** tiap soal CPNS punya rating Elo kesulitan yang bergerak; dashboard menampilkan kemampuan Sandi vs kesulitan soal; set HOTS harian memilih soal yang ratingnya dekat dengan kemampuan (tantangan ≈ kemampuan = flow state — ini tujuan yang dia minta sendiri 12 Nov).

### A3. OpenTutor — adaptive learning workspace (MIT)
- Repo: https://github.com/zijinz456/OpenTutor
- Fitur: AI-generated quizzes (7 tipe soal), wrong-answer tracking dengan diagnostic feedback, kesulitan beradaptasi dari performa, FSRS 4.5, knowledge graphs, cognitive load detection, BKT (Bayesian Knowledge Tracing), LOOM, LECTOR. Local-first, 10+ LLM provider.
- **Yang diambil:** (a) diagnostic feedback per jawaban salah — bukan sekadar pembahasan, tapi diagnosis pola ("3x salah silogisme rantai-putus — ini polanya"); (b) kesulitan sesi berikutnya beradaptasi dari skor sesi sebelumnya.

### A4. KnowledgeForge — adaptive study agent (FSRS-6 + mastery states)
- Repo: https://github.com/paulina-grunwald/knowledgeforge (README terverifikasi).
- Fitur: RAG-generated quiz dari materi sendiri, tracking state per konsep dengan FSRS-6, sesi multi-turn dengan hints, follow-up, dan teach-back exercises. Mastery states: UNSEEN → EXPOSED → SHAKY → SOLID → STALE.
- **Yang diambil:** (a) mastery state per topik di dashboard (TWK pasal / TIU deret / figural / TKP per aspek) dengan bar progres; (b) tombol "petunjuk" di mode nilai-langsung sebelum menjawab + soal variasi lanjutan setelah salah (teach-back).

### A5. Universal Exam Cram Coach — Claude Agent Skill (ZeKaiNie)
- Repo: https://github.com/ZeKaiNie/universal-examprep-skill (MIT, instal via `npx skills add`).
- Fitur: mengubah slide/catatan/past paper jadi knowledge base ber-bab + bank soal, hanya mengajar dari materi yang ada, tidak mengarang (terukur 100% out-of-scope abstention). Bilingual EN/中文.
- **Yang diambil (untuk Mommy, bukan aplikasi):** pola anti-hallucination-nya — soal latihan HANYA dari bank soal standar; soal AI sementara tidak pernah disajikan sebagai soal kursus. Ini sudah menjadi aturan kita (soal bimbel ≠ soal resmi BKN); skill ini memberi template formalnya. Catatan: instalasi skill ini untuk Mommy sendiri adalah keputusan terpisah — JANGAN instal tanpa persetujuan Sandi.

### A6. Ekosistem skill (konteks format)
- Anthropic official Agent Skills: https://github.com/anthropics/skills (186,2 ribu stars) — format SKILL.md.
- awesome-claude-code (57.668 stars) — direktori skill/plugin; mattpocock/skills (307,2 ribu stars, 27 skill); awesome-agentic-atlas (252 entri). Skill relevan lain yang disebut: `learn-faster-kit` (framework edukasi), `Bloom` (taksonomi Bloom untuk soal).

## B. DESAIN MOBBIN — pola yang terbukti dari aplikasi nyata

Mobbin = perpustakaan referensi UI dengan 600.000+ layar nyata dari produk yang sudah rilis. Akses penuh butuh akun Mobbin berbayar (Pro/Team) + MCP resmi (https://api.mobbin.com/mcp); ada pula skill CLI `thesved/epic-skills` (.claude/skills/mobbin) yang membungkus MCP itu. Untuk edit ini pola-pola di bawah sudah cukup terdokumentasi — TIDAK perlu akun Mobbin.

### B1. Studi streak Mobbin — 859 desain streak (Sep 2026)
- Sumber: https://mobbin.com/blog/streaks-are-about-losing-a-study-of-859-streak-designs
- Aturan yang terbukti:
  - Streak menghitung HARI berturut-turut, bukan progres belajar.
  - Layar angka besar HANYA muncul setelah aksi selesai (layar pasca-pelajaran) atau saat milestone — TIDAK PERNAH saat membuka aplikasi.
  - Permukaan streak sehari-hari = satu baris di header beranda (contoh Peloton: "3 days Streak" + tujuh titik; Streaks: angka di dalam cincin).
  - Strip 7 hari bersifat universal dengan 3 keadaan: sudah dikerjakan (centang terisi), hari ini (garis tepi/warna), hari mendatang (redup).
  - Streak freeze itu norma: Duolingo mengizinkan 2 freeze sekaligus → 200.000 orang lebih kembali setiap hari. Finch: palu perbaikan saat sehari terlewat. Alma: jeda hingga 14 hari.
  - Copy perayaan = satu kalimat pendek orang kedua + angka + satuan ("3 day streak") + satu tombol utama.
- Layar Mobbin spesifik (dari repo GuidedChildhood yang mengutip Mobbin):
  - Daily Quests panel: https://mobbin.com/screens/0b1b367c-1d8c-493f-8d77-d1d895ae613d — 3–4 baris, masing-masing SATU baris teks, progress bar tipis sendiri, peti hadiah di kanan, countdown di header.
  - Quest point earned: https://mobbin.com/screens/60b2c7e0-b3c5-4ebe-ae99-976f7cb8ece6 — takeover kecil dengan daftar + bar yang baru bergerak.
  - Streak day one: https://mobbin.com/screens/e319cd42-df5e-4862-ad4a-9cffdc5234d2 ; day five: https://mobbin.com/screens/84ec5a7b-37ce-4c38-808d-7c3c91c3c0aa ; day six: https://mobbin.com/screens/f6675d16-c6b5-4847-aa9f-fb66a2d61e88 — takeover layar penuh, angka besar, "N day streak", strip minggu Sen–Min dengan centang.
- **Relevansi pribadi:** streak Duolingo Sandi sendiri PUTUS 11 Nov 2026 (jadi 0). Mekanik freeze/repair bukan hiasan — itu yang dia butuhkan.

### B2. Studi onboarding — 35 flow + 18 layar via Mobbin (Agu 2026)
- Sumber: https://sciencebasedsoftware.com/topics/onboarding/ (juga dirangkum di https://github.com/chrispiz/apple-app-ui-design/blob/HEAD/references/onboarding-flows.md — sintesis 1.460+ flow).
- Duolingo memberikan SATU PELAJARAN PENUH sebelum meminta apa pun; signup dipindah ke setelah pelajaran pertama → +20% DAU; melunakkan dinding signup ("LATER" alih-alih tombol buang merah) → +8,2% DAU.
- Layar payoff (hasil akhir) adalah artefak penyelesaian, bukan dekorasi: tampilkan XP total, akurasi, waktu.
- 63% flow kuis punya 3+ layar pertanyaan; progress bar di layar pertanyaan adalah standar.

### B3. Template Duolingo 15 layar (Whimsical, digambar dari screenshot Mobbin)
- Sumber: https://whimsical.com/templates/language-learning-app-wireframe
- Pola yang bisa dicuri: lesson path (Section 1, Unit 1, pelajaran kafe di jalur, popover menawarkan review demi XP atau ronde Legendary yang lebih sulit); tiga tipe latihan; layar hasil ("Nicely done!" + XP total, akurasi, waktu); streak + quest (streak 6 hari, minggu ditandai, daily quest "Earn 70 XP", weekend + monthly quest); profil (XP, liga, streak teman, toko gem).
- Template ini dibuat dengan skill open-source "App Wireframe" (mengubah layar aplikasi jadi wireframe Whimsical).

## C. RENCANA PENERAPAN KE APLIKASI KITA (prioritas)

### P0 — wajib di edit ini
1. **Buku kesalahan FSRS (A1):** ganti jadwal tetap 1-3-7-14-30 dengan model FSRS-6 per soal (Difficulty/Stability/Retrievability, target retensi 0.90). UI review: 4 rating (Lupa/Sulit/Lumayan/Mudah). Beranda: antrean "jatuh tempo hari ini" (jumlah soal + perkiraan menit). Migrasi: soal yang sudah ada di buku kesalahan masuk FSRS dengan state awal dari riwayatnya (salah 1x = Stability rendah). JANGAN hapus data lama.
2. **Panel Daily Quests ala Mobbin (B1):** di beranda, 3–4 baris satu-baris-teks, masing-masing progress bar tipis + hadiah (peti/XP) di kanan, countdown ke reset 10:00. Quest harian yang masuk akal untuk Sandi: (a) kerjakan 1 sesi latihan, (b) ulangi 5 soal buku kesalahan, (c) 1 set Bedah HOTS, (d) skor TKP ≥ 4,5/soal. Quest selesai → animasi kecil + bar bergerak (pola "Quest point earned").
3. **Lesson path sebagai beranda (B3):** ganti daftar sesi biasa menjadi jalur (path) bernode: Hari 1 → Hari 8 → Bedah HOTS → Simulasi. Node selesai = centang, node aktif = menonjol, node mendatang = terkunci/redup. Popover pada node aktif: "Review demi XP" atau "Ronde Legendary" (varian lebih sulit dari sesi itu).

### P1 — penting, kerjakan bila muat di edit ini
4. **Streak yang benar (B1):** header beranda satu baris streak + strip 7 hari (3 keadaan). Layar angka besar HANYA di layar selesai-pelajaran (payoff), bukan saat buka aplikasi. Tambah 1 streak freeze (beku otomatis bila sehari terlewat, maks 1 aktif) — relevan karena streak Duolingo-nya pernah putus.
5. **Elo kesulitan + sesi adaptif (A2 + A3):** rating Elo per soal (bergerak dari jawaban nyata); dashboard "kemampuanmu vs kesulitan soal"; set HOTS harian memilih soal di dekat rating kemampuan (flow).
6. **Layar payoff selesai-pelajaran (B2 + B3):** setelah submit, layar hasil: XP total, akurasi, waktu, update streak, dan tombol lanjut. Ini artefak penyelesaian — bukan dekorasi.

### P2 — bila masih muat
7. **Mastery state per topik (A4):** dashboard per topik (TWK pasal / TIU deret / figural / TKP per aspek): UNSEEN → EXPOSED → SHAKY → SOLID → STALE + bar progres.
8. **Diagnosis pola salah (A3):** panel "titik lemahmu minggu ini" dari jawaban salah (contoh: "silogisme rantai-putus 3x — ini polanya").
9. **Tombol petunjuk (A4):** di mode nilai-langsung, tombol petunjuk sebelum menjawab (biaya sedikit skor) + soal variasi lanjutan setelah salah.

## D. BATASAN (jangan dilanggar)
- Data yang ada TIDAK BOLEH hilang: 251 soal bank + 10 HOTS, 12 sesi, riwayat skor (termasuk attempt verifikasi Mommy Hari 8: 155/160 — itu BUKAN skor Sandi, jangan tampilkan sebagai skornya), buku kesalahan, briefing CPNS 12 Nov.
- Tetap: target TWK 90 / TIU 110 / TKP 185; passing grade TWK 65 / TIU 80 / TKP 166; bahasa Indonesia; soal HOTS tetap sulit; cron cpns-daily-practice + updater harian aplikasi (applyDailyUpdate) + aksi addSession tetap berfungsi.
- Verifikasi seperti edit sebelumnya: audit lulus tanpa error konsol, probe HP + desktop, dan periksa sendiri logika FSRS (jadwal berikutnya berubah sesuai rating) sebelum diserahkan.
- Instalasi skill untuk Mommy sendiri (mis. universal-examprep-skill, mobbin CLI) TIDAK termasuk dalam edit ini — itu keputusan terpisah yang butuh persetujuan Sandi.
