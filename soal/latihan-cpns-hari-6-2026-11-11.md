# Latihan CPNS Hari 6 — Rabu, 11 November 2026
**Fokus: TIU Numerik — Deret Lanjutan + Soal Cerita · 30 soal baru · Target: ≥24 benar · Waktu: ~45 menit soal, total sesi ~2 jam**

*Sesuai rotasi mingguan: Rabu = TIU numerik (deret & soal cerita). Semua soal di bawah ini BARU — tidak mengulang satu pun soal Hari 1–5 (dicek terhadap file Hari 1, 2, 2b, 3, 4, 5). Soal dibuat berpola sama dengan SKD 2023–2024, bukan soal resmi BKN — BKN tidak mempublikasikan soal SKD. Kerjakan dulu tanpa melihat kunci, baru cek jawaban.*

---

## Pemanasan 60 detik — drill pasal kembar (dari kesalahan Hari 4)

Sebelum materi baru, tulis SATU kalimat untuk tiap pasangan — dari ingatan, tanpa membuka kunci Hari 4. Lalu cek langsung.

1. Pasal 6 vs Pasal 6A: yang mana syarat calon Presiden, yang mana cara memilih Presiden & Wapres?
2. Pasal 21 vs Pasal 22: yang mana hak DPR mengajukan RUU, yang mana Perppu?
3. Pasal 24 vs Pasal 24A: yang mana kekuasaan kehakiman secara umum, yang mana kewenangan MA (kasasi + menguji peraturan di bawah UU)?

*Jawaban: 6 = syarat calon Presiden; 6A = Presiden & Wapres dipilih satu pasangan langsung oleh rakyat. 21 = DPR berhak mengajukan RUU; 22 = Perppu (hal ihwal kegentingan yang memaksa). 24 = kekuasaan kehakiman oleh MA & MK; 24A = MA berwenang mengadili kasasi + menguji peraturan di bawah UU terhadap UU. Tiga pasal kembar inilah yang menjatuhkanmu di Hari 4 — drill ini yang membuatmu tidak jatuh lagi.*

---

## Pelajaran fundamental: deret lanjutan — 5 pola baru + soal cerita

Kamu sudah kuasai 5 pola dasar Hari 2b (beda tetap, beda berubah, rasio tetap, dua lapis, operasi ganda). Hari ini 5 pola lanjutan yang paling sering muncul di TIU — semuanya masih bisa dipecahkan dengan urutan cek yang sama: **selisih dulu → rasio kedua → pisah ganjil-genap ketiga**, ditambah satu pertanyaan baru: **"apakah suku ini hasil dari suku sebelumnya, atau dari DUA suku sebelumnya?"**

### Pola 6 — Kuadrat & kubik (pangkat)
Suku ke-n adalah n², n³, atau variasinya (± angka tetap).
Contoh: 1, 8, 27, 64, 125, … → 1³, 2³, 3³, 4³, 5³ → berikutnya 6³ = **216**.
Variasi: 2, 5, 10, 17, 26, … → 1²+1, 2²+1, 3²+1, 4²+1, 5²+1 → berikutnya 6²+1 = **37**.
Cara mengenali: selisihnya membesar teratur (+3, +5, +7, +9 untuk kuadrat) dan angkanya "bulat" (1, 4, 9, 16, 25… atau 1, 8, 27, 64…).

### Pola 7 — Selisih berlapis dua (second difference)
Selisih antar suku membentuk deretnya sendiri.
Contoh: 3, 5, 9, 15, 23, … → selisih +2, +4, +6, +8 (naik 2 tiap langkah) → selisih berikutnya +10 → 23 + 10 = **33**.
Bedakan dari Pola 2 Hari 2b: di sana selisihnya naik dengan beda tetap juga — intinya sama, tapi di sini selisihnya bisa naik dengan pola lain (mis. ×2: +1, +2, +4, +8…).

### Pola 8 — Jumlah dua suku sebelumnya (Fibonacci)
Tiap suku = jumlah dua suku sebelumnya.
Contoh: 5, 6, 11, 17, 28, … → 5+6=11, 6+11=17, 11+17=28 → berikutnya 17+28 = **45**.
Cara mengenali: suku ketiga "terlalu besar" untuk dijelaskan selisih biasa, tapi pas sama dengan jumlah dua suku sebelumnya. Uji ke suku keempat sebelum percaya.

### Pola 9 — Pengali berubah (×n dengan n naik)
Pengalinya naik teratur: ×2, ×3, ×4… atau ×2, ×4, ×6…
Contoh: 3, 6, 24, 144, … → ×2, ×4, ×6 → berikutnya ×8 → 144 × 8 = **1152**.
Jebakan: yang hanya melihat "dikali" lalu menebak ×2 lagi akan menjawab 288 — padahal pengalinya ikut naik.

### Pola 10 — Operasi ganda naik (×n + m yang ikut berubah)
Tiap suku = suku sebelumnya × n, lalu ditambah m — dan m-nya naik tiap langkah.
Contoh: 3, 7, 16, 35, 74, … → ×2+1, ×2+2, ×2+3, ×2+4 → berikutnya ×2+5 → 74 × 2 + 5 = **153**.
Cara menemukan: coba ×2 dulu; kalau kelebihan/kekurangannya naik 1 tiap langkah, itulah m yang berubah.

### Soal cerita — 4 teknik cepat
1. **Perbandingan berbalik nilai** (pekerja × hari = tetap): total "pekerja-hari" dulu, baru bagi. Contoh: 12 pekerja × 20 hari = 240 pekerja-hari → 15 pekerja = 240 ÷ 15 = 16 hari.
2. **Kerja bersama:** 1/T = 1/T₁ + 1/T₂. Contoh: A 6 hari, B 12 hari → 1/T = 1/6 + 1/12 = 3/12 → T = 4 hari.
3. **Persen bertingkat:** kalikan faktornya, jangan dijumlah persennya. Naik 10% lalu 10% lagi = ×1,1 × 1,1 = ×1,21 (bukan +20%).
4. **Kecepatan bertemu / menyusul:** waktu bertemu = jarak ÷ (v₁ + v₂). Waktu menyusul = jarak awal ÷ (v₁ − v₂).

---

## Soal (30 soal baru)

### TIU Numerik — deret (Soal 1–15)

**1.** 2, 5, 10, 17, 26, …
A. 35
B. 36
C. 37
D. 38

**2.** 1, 8, 27, 64, 125, …
A. 196
B. 216
C. 225
D. 256

**3.** 3, 5, 9, 15, 23, …
A. 31
B. 32
C. 33
D. 35

**4.** 3, 6, 24, 144, …
A. 720
B. 864
C. 1152
D. 1728

**5.** 1, 10, 3, 12, 5, 14, 7, …
A. 9
B. 15
C. 16
D. 17

**6.** 4, 10, 28, 82, …
A. 240
B. 242
C. 244
D. 246

**7.** 1, 2, 6, 15, 31, …
A. 52
B. 54
C. 56
D. 58

**8.** 100, 90, 81, 73, 66, …
A. 58
B. 59
C. 60
D. 61

**9.** 5, 6, 11, 17, 28, …
A. 39
B. 43
C. 45
D. 47

**10.** 3, 7, 16, 35, 74, …
A. 149
B. 151
C. 153
D. 155

**11.** 2, 3, 5, 9, 17, 33, …
A. 63
B. 64
C. 65
D. 67

**12.** 2, 3, 5, 7, 11, 13, …
A. 15
B. 17
C. 19
D. 21

**13.** 729, 243, 81, 27, …
A. 3
B. 9
C. 12
D. 18

**14.** 20, 16, 19, 15, 18, 14, 17, …
A. 12
B. 13
C. 14
D. 16

**15.** 0, 3, 8, 15, 24, …
A. 33
B. 35
C. 36
D. 37

### TIU Numerik — soal cerita (Soal 16–30)

**16.** Sebuah kereta berangkat pukul 07.30 dengan kecepatan rata-rata 80 km/jam menuju kota yang berjarak 240 km. Kereta tiba pukul…
A. 10.00
B. 10.30
C. 11.00
D. 11.30

**17.** Sebuah proyek dikerjakan 12 pekerja selesai dalam 20 hari. Jika pekerja ditambah 3 orang, proyek selesai dalam…
A. 14 hari
B. 15 hari
C. 16 hari
D. 17 hari

**18.** Nilai rata-rata 8 siswa adalah 75. Dua siswa baru bergabung dengan nilai 80 dan 90. Nilai rata-rata 10 siswa sekarang adalah…
A. 76
B. 77
C. 78
D. 79

**19.** Sebuah barang dibeli seharga Rp400.000 lalu dijual dengan untung 15%. Harga jual barang itu adalah…
A. Rp440.000
B. Rp450.000
C. Rp460.000
D. Rp470.000

**20.** Umur ayah 4 kali umur anaknya. Enam tahun lagi, umur ayah 3 kali umur anaknya. Umur anak sekarang adalah…
A. 10 tahun
B. 11 tahun
C. 12 tahun
D. 13 tahun

**21.** Pekerja A dapat menyelesaikan suatu pekerjaan dalam 6 hari, pekerja B dalam 12 hari. Jika keduanya bekerja bersama, pekerjaan selesai dalam…
A. 3 hari
B. 4 hari
C. 5 hari
D. 6 hari

**22.** Gaji seorang karyawan Rp5.000.000. Gajinya naik 10%, lalu tahun berikutnya naik lagi 10%. Gaji akhirnya adalah…
A. Rp6.000.000
B. Rp6.050.000
C. Rp6.100.000
D. Rp6.500.000

**23.** Perbandingan uang Andi, Budi, dan Candra adalah 2 : 3 : 5. Jumlah uang mereka Rp500.000. Uang Candra adalah…
A. Rp200.000
B. Rp250.000
C. Rp300.000
D. Rp350.000

**24.** Dua mobil berangkat dari dua kota yang berjarak 300 km, saling mendekat dengan kecepatan 50 km/jam dan 70 km/jam. Keduanya berpapasan setelah…
A. 2 jam
B. 2,5 jam
C. 3 jam
D. 3,5 jam

**25.** Seseorang menabung Rp2.000.000 dengan bunga sederhana 12% per tahun. Setelah 6 bulan, total uangnya (pokok + bunga) adalah…
A. Rp2.060.000
B. Rp2.120.000
C. Rp2.240.000
D. Rp2.480.000

**26.** Jumlah dua bilangan adalah 48 dan selisihnya 12. Bilangan yang lebih besar adalah…
A. 28
B. 30
C. 32
D. 36

**27.** Sebuah mesin fotokopi mencetak 120 lembar dalam 4 menit. Waktu yang dibutuhkan untuk mencetak 900 lembar adalah…
A. 24 menit
B. 28 menit
C. 30 menit
D. 36 menit

**28.** Harga 3 kg apel dan 2 kg jeruk adalah Rp95.000. Harga 1 kg apel dan 1 kg jeruk adalah Rp35.000. Harga 1 kg jeruk adalah…
A. Rp10.000
B. Rp15.000
C. Rp20.000
D. Rp25.000

**29.** Sebuah jaket seharga Rp200.000 mendapat diskon 20%, lalu diskon tambahan 10% dari harga setelah diskon pertama. Harga akhir jaket adalah…
A. Rp136.000
B. Rp140.000
C. Rp144.000
D. Rp160.000

**30.** Seorang pekerja membuat 5 unit pada hari pertama, lalu setiap hari berikutnya ia membuat 3 unit lebih banyak dari hari sebelumnya. Total unit yang dibuat dalam 10 hari adalah…
A. 175 unit
B. 180 unit
C. 185 unit
D. 190 unit

---

## Kunci jawaban + pembahasan

**1. C — 37.** Pola 6 (kuadrat +1): 1²+1, 2²+1, 3²+1, 4²+1, 5²+1 → 6²+1 = 37. Jebakan: A (35) muncul kalau mengira selisihnya +3, +5, +7, +9 lalu +11 dari 26 — itu 37 juga, sebenarnya cara itu benar; yang salah adalah B (36 = 6², lupa +1).

**2. B — 216.** Pola 6 (kubik): 1³, 2³, 3³, 4³, 5³ → 6³ = 216. Jebakan: D (256 = 4⁴) dan C (225 = 15²) — angka "bulat" yang menggoda tapi bukan kubik.

**3. C — 33.** Pola 7 (selisih berlapis dua): selisih +2, +4, +6, +8 → selisih berikutnya +10 → 23 + 10 = 33.

**4. C — 1152.** Pola 9 (pengali berubah): ×2, ×4, ×6 → berikutnya ×8 → 144 × 8 = 1152. Jebakan: B (864 = 144 × 6) — pengali tidak naik.

**5. C — 16.** Pola 4 (dua lapis, dari Hari 2b): suku ganjil 1, 3, 5, 7 (+2); suku genap 10, 12, 14 (+2) → suku ke-8 (genap) = 16. Jebakan: B (15) — mengira deret genapnya +3.

**6. C — 244.** Pola 5 (operasi ganda, dari Hari 2b): ×3 − 2 → 82 × 3 − 2 = 244. Jebakan: A (240) — 82 × 3 = 246, lalu salah hitung.

**7. C — 56.** Pola 7 (selisih berlapis dua): selisih +1, +4, +9, +16 (kuadrat 1², 2², 3², 4²) → selisih berikutnya +25 → 31 + 25 = 56.

**8. C — 60.** Pola 2 (beda berubah, dari Hari 2b): selisih −10, −9, −8, −7 → selisih berikutnya −6 → 66 − 6 = 60. Jebakan: pengurangannya mengecil, bukan membesar — jangan otomatis menambah.

**9. C — 45.** Pola 8 (jumlah dua suku sebelumnya): 5+6=11, 6+11=17, 11+17=28 → 17+28 = 45.

**10. C — 153.** Pola 10 (operasi ganda naik): ×2+1, ×2+2, ×2+3, ×2+4 → berikutnya ×2+5 → 74 × 2 + 5 = 153.

**11. C — 65.** Pola 7 (selisih berlapis dua): selisih +1, +2, +4, +8, +16 (tiap selisih ×2) → selisih berikutnya +32 → 33 + 32 = 65.

**12. B — 17.** Bilangan prima berurutan: 2, 3, 5, 7, 11, 13 → berikutnya 17. Jebakan: A (15) — 15 bukan prima (3 × 5).

**13. B — 9.** Pola 3 (rasio tetap, dari Hari 2b): selalu ÷3 → 27 ÷ 3 = 9. Jebakan: A (3) — itu suku berikutnya setelah 9, bukan suku ini.

**14. B — 13.** Pola 4 (dua lapis menurun): suku ganjil 20, 19, 18, 17 (−1); suku genap 16, 15, 14 (−1) → suku ke-8 (genap) = 13.

**15. B — 35.** Pola 6 (kuadrat −1): 1²−1, 2²−1, 3²−1, 4²−1, 5²−1 → 6²−1 = 35. Jebakan: C (36 = 6², lupa −1).

**16. B — 10.30.** Waktu tempuh = 240 ÷ 80 = 3 jam → 07.30 + 3 jam = 10.30.

**17. C — 16 hari.** Perbandingan berbalik nilai: 12 × 20 = 240 pekerja-hari; pekerja baru 12 + 3 = 15 → 240 ÷ 15 = 16 hari. Jebakan: A (14) — hasil pengurangan asal-asalan (20 − 6).

**18. B — 77.** Total nilai awal = 8 × 75 = 600; tambah 80 + 90 = 770; rata-rata baru = 770 ÷ 10 = 77.

**19. C — Rp460.000.** Untung = 15% × Rp400.000 = Rp60.000 → jual Rp400.000 + Rp60.000 = Rp460.000. Atau langsung: 115% × Rp400.000 = Rp460.000.

**20. C — 12 tahun.** Misal anak = x, ayah = 4x. Enam tahun lagi: 4x + 6 = 3(x + 6) → 4x + 6 = 3x + 18 → x = 12. Ayah sekarang 48 tahun (cek: 48 + 6 = 54 = 3 × 18 ✓).

**21. B — 4 hari.** Kerja bersama: 1/T = 1/6 + 1/12 = 2/12 + 1/12 = 3/12 → T = 4 hari. Jebakan: C (5) — rata-rata 6 dan 12 dibagi 2 bukan cara kerja bersama; D (6) — itu waktu A sendiri.

**22. B — Rp6.050.000.** Persen bertingkat: Rp5.000.000 × 1,1 × 1,1 = Rp5.000.000 × 1,21 = Rp6.050.000. Jebakan: A (Rp6.000.000) — 10% + 10% = 20% adalah kesalahan klasik; persen kedua dihitung dari gaji yang sudah naik.

**23. B — Rp250.000.** Total bagian = 2 + 3 + 5 = 10 → Candra = 5/10 × Rp500.000 = Rp250.000.

**24. B — 2,5 jam.** Saling mendekat: kecepatan gabungan 50 + 70 = 120 km/jam → 300 ÷ 120 = 2,5 jam.

**25. B — Rp2.120.000.** Bunga 6 bulan = 12% × 6/12 × Rp2.000.000 = Rp120.000 → total Rp2.120.000. Jebakan: C (Rp2.240.000) — bunga 12% penuh setahun, lupa waktunya cuma 6 bulan.

**26. B — 30.** Bilangan besar = (jumlah + selisih) ÷ 2 = (48 + 12) ÷ 2 = 30. (Yang kecil = (48 − 12) ÷ 2 = 18; cek: 30 + 18 = 48, 30 − 18 = 12 ✓.)

**27. C — 30 menit.** Kecepatan mesin = 120 ÷ 4 = 30 lembar/menit → 900 ÷ 30 = 30 menit.

**28. A — Rp10.000.** Misal apel = A, jeruk = J: A + J = 35.000 dan 3A + 2J = 95.000. Kalikan persamaan pertama dengan 2: 2A + 2J = 70.000 → kurangkan: A = 25.000 → J = 35.000 − 25.000 = 10.000.

**29. C — Rp144.000.** Diskon bertingkat: Rp200.000 × 0,8 × 0,9 = Rp144.000. Jebakan: B (Rp140.000) — 20% + 10% = 30% langsung dari harga awal (Rp200.000 × 0,7); diskon kedua dihitung dari harga setelah diskon pertama, bukan dari harga awal.

**30. C — 185 unit.** Deret aritmetika: a = 5, d = 3, n = 10 → suku terakhir = 5 + 9 × 3 = 32 → total = 10/2 × (5 + 32) = 5 × 37 = 185. (Rumus: Sₙ = n/2 × (a + Uₙ).)

---

## Setelah mengerjakan

- **Skor sesi ini:** ___ / 30. Target Hari 6: ≥24 benar (≈120 poin TIU — TIU 35 soal × 5 poin = 175; passing grade 80 = 16 benar; target aman 110+ = 22 benar).
- **Buku kesalahan:** tulis nomor soal yang salah + polanya (mis. "Soal 10 — operasi ganda naik, lupa m ikut naik"). Soal yang salah diulang **3 hari kemudian (Sabtu, 14 Nov 2026)** — tapi ingat, Sabtu 14 Nov adalah **SIMULASI PENUH CAT SKD** (110 soal / 100 menit), jadi soal salah Hari 6 diulang sebagai bagian dari review pasca-simulasi, bukan sebagai sesi terpisah.
- **Jawaban Hari 1, 2, 2b masih belum dikirim.** Kirim sekali saja (format: "Hari 1: 1B 2A …") supaya buku kesalahan bisa jalan penuh — tanpa jawabanmu, spaced repetition tidak bisa bekerja.
- **Besok (Kamis, 12 Nov):** TKP — studi kasus + **ulang 3 soal salah Hari 4** (No. 7, 10, 15 — pasal kembar, versi soal bervariasi).
- **Jumat, 13 Nov:** TIU figural + **ulang 2 soal salah Hari 5** (No. 20, 29 — jebakan "tidak dapat disimpulkan" yang over-firing).
- **Sabtu, 14 Nov:** SIMULASI PENUH CAT SKD — 110 soal dalam 100 menit (TWK 30 → TIU 35 → TKP 45), target total ≥385/550. Siapkan jam, HP disingkirkan, dan mental play state.
