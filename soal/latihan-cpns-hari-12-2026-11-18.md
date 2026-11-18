# Latihan CPNS Hari 12 — Rabu, 18 November 2026
**Fokus: TIU Numerik — Deret & Soal Cerita (HARD) · 30 soal baru · Target: ≥24 benar (≈120 poin TIU) · Waktu: ~45 menit soal, total sesi ~2 jam**

*Sesuai rotasi mingguan: Rabu = TIU numerik. Semua soal di bawah ini BARU — tidak mengulang satu pun soal Hari 1–11 maupun simulasi (dicek terhadap file Hari 6, Hari 9, dan simulasi 14 Nov). Soal dibuat berpola sama dengan SKD 2023–2024, bukan soal resmi BKN — BKN tidak mempublikasikan soal SKD. Tingkat kesulitan HARD (di atas SKD asli, perintah Sandi 12 Nov) — deret dua operasi/dua lapis, analisis tabel, perbandingan kuantitatif, dan soal cerita multi-langkah. Kerjakan dulu tanpa melihat kunci, baru cek jawaban.*

---

## Pemanasan 60 detik — drill dari kesalahan Hari 6

Tulis jawabannya dari ingatan, tanpa menghitung panjang-panjang. Lalu cek langsung.

1. Deret kuadrat−1: 8, 15, 24, 35, 48, … → berikutnya?
2. Pekerja-hari: 9 pekerja menyelesaikan proyek dalam 16 hari. Berapa hari bila pekerjanya 12 orang?
3. Jumlah–selisih: jumlah dua bilangan 72, selisihnya 18. Bilangan yang lebih besar?

*Jawaban: 1) 63 (8²−1; polanya n²−1: 3²−1=8, 4²−1=15, 5²−1=24, 6²−1=35, 7²−1=48, 8²−1=63). 2) 12 hari (9×16=144 pekerja-hari; 144÷12=12). 3) 45 ((72+18)÷2). Tiga pola inilah yang menjatuhkanmu di Hari 6 (No. 15, 17, 26) — drill ini yang membuatmu tidak jatuh lagi.*

---

## Pelajaran fundamental: deret lanjutan (pola 11–14) + analisis tabel + perbandingan kuantitatif + soal cerita

Kamu sudah kuasai 10 pola deret (Hari 2b + Hari 6). Hari ini 4 pola baru — semuanya masih dipecahkan dengan urutan cek yang sama: **selisih dulu → rasio kedua → pisah ganjil-genap ketiga → tanya "apakah suku ini hasil dari DUA suku sebelumnya?"**

### Pola 11 — Dua lapis dengan operasi BERBEDA per lapis
Suku ganjil dan suku genap memakai aturan sendiri-sendiri — dan aturannya boleh beda jenis (satu dikali, satu ditambah).
Contoh: 2, 5, 6, 10, 18, 15, 54, 20, … → ganjil: 2, 6, 18, 54 (×3); genap: 5, 10, 15, 20 (+5) → suku berikutnya (ganjil) = 54 × 3 = **162**.
Cara mengenali: deret tampak acak, tapi begitu dipisah ganjil-genap, masing-masing lapis langsung teratur.

### Pola 12 — Deret mundur (selisih negatif yang membesar)
Deret tidak harus naik. Selisihnya bisa negatif dan membesar — jawabannya boleh negatif.
Contoh: 200, 190, 170, 130, 50, … → selisih −10, −20, −40, −80 (tiap selisih ×2) → selisih berikutnya −160 → 50 − 160 = **−110**.
Jebakan: yang takut angka negatif akan memaksakan jawaban positif — padahal di CAT, jawaban negatif itu sah.

### Pola 13 — Rekurensi dua suku (aₙ = 2·aₙ₋₁ + aₙ₋₂)
Bukan sekadar jumlah dua suku sebelumnya (Fibonacci), melainkan salah satunya dikali dulu.
Contoh: 1, 3, 7, 17, 41, … → 7 = 2×3+1; 17 = 2×7+3; 41 = 2×17+7 → berikutnya 2×41+17 = **99**.
Cara menemukan: kalau suku ketiga "terlalu besar" untuk jumlah biasa, coba kalikan suku sebelumnya dengan 2 lalu tambah suku sebelumnya lagi.

### Pola 14 — Pangkat ± n (n³−n dan n³+1)
Kubik yang digeser oleh n itu sendiri.
Contoh: 0, 6, 24, 60, 120, … → 1³−1, 2³−2, 3³−3, 4³−4, 5³−5 → berikutnya 6³−6 = **210**. Variasi: 2, 9, 28, 65, 126, … → n³+1 → berikutnya 6³+1 = **217**.
Jebakan: 216 (6³) selalu menggoda — ingat ± n-nya.

### Teknik analisis tabel — jumlahkan kolom dulu, pembagi = yang ditanyakan
1. Baca dulu apa yang ditanya: total? selisih? persen dari apa?
2. Jumlahkan per kolom/baris yang relevan SEBELUM menghitung — jangan bandingkan satu sel.
3. Persen "A dari B" → pembaginya B, bukan total keseluruhan. "Kenaikan dari X ke Y" → pembaginya X (nilai awal).
4. Kesimpulan dari tabel ("manakah pernyataan yang benar") → hitung rasionya (mis. kepadatan = penduduk ÷ luas), jangan tebak dari angka mentahnya.

### Teknik perbandingan kuantitatif — sederhanakan bentuk, jangan hitung penuh
1. Coret faktor yang sama di kedua sisi dulu (mis. 2/3 × 3/4 = 1/2 — angka 3-nya hilang).
2. Bandingkan bentuknya, bukan hasil akhirnya — sering kali jawabannya kelihatan tanpa kalkulator.
3. Kalau ada variabel bebas (mis. n bilangan asli tanpa batas), jawabannya "tidak dapat ditentukan" — uji dengan dua nilai n yang berbeda; kalau hasilnya berbalik, itulah jawabannya.

### Teknik soal cerita — TERJEMAH DULU KE PERSAMAAN (diagnosis Hari 6)
Kelemahanmu di Hari 6 bukan pola deret (13/15), melainkan penerjemahan soal cerita ke persamaan + kecerobohan satuan. Urutan kerja yang benar:
1. **Tulis "yang dicari = ?"** — satu baris, sebelum menghitung apa pun.
2. **Tulis persamaannya** (mis. total pekerja-hari = pekerja × hari; total nilai = rata-rata × jumlah).
3. **Cek satuan waktu** sebelum menghitung: 6 bulan = 0,5 tahun; 30 menit = 0,5 jam.
4. **"Maksimal"** = bulatkan ke BAWAH bila uang tidak cukup untuk satu unit lagi. **"Disisihkan dulu"** = kurangkan dari uang sebelum membagi.

---

## Soal (30 soal baru)

### TIU Numerik — deret (Soal 1–12)

**1.** 5, 13, 29, 61, 125, …
A. 249
B. 251
C. 253
D. 255

**2.** 2, 5, 6, 10, 18, 15, 54, 20, …
A. 25
B. 162
C. 108
D. 60

**3.** 1, 3, 7, 17, 41, …
A. 95
B. 97
C. 101
D. 99

**4.** 0, 6, 24, 60, 120, …
A. 210
B. 180
C. 200
D. 216

**5.** 200, 190, 170, 130, 50, …
A. −90
B. −110
C. −30
D. 10

**6.** 2, 3, 6, 15, 42, …
A. 120
B. 126
C. 123
D. 129

**7.** 5, 4, 12, 8, 19, 16, 26, 32, …
A. 40
B. 64
C. 36
D. 33

**8.** 2, 9, 28, 65, 126, …
A. 217
B. 215
C. 216
D. 218

**9.** 10, 20, 17, 34, 31, 62, …
A. 60
B. 59
C. 65
D. 124

**10.** 1, 2, 10, 37, 101, …
A. 222
B. 230
C. 226
D. 216

**11.** 96, 48, 52, 26, 30, 15, …
A. 17
B. 7
C. 30
D. 19

**12.** 6, 10, 20, 24, 48, 52, …
A. 104
B. 56
C. 100
D. 108

### TIU Numerik — analisis tabel (Soal 13–16)

**13.** Tabel penjualan Toko Maju (dalam unit). Kopi: Januari 120, Februari 150, Maret 180. Gula: Januari 80, Februari 100, Maret 90. Total penjualan gula selama tiga bulan adalah berapa persen dari total penjualan kopi?
A. 50%
B. 55%
C. 60%
D. 65%

**14.** Tabel produksi tiga mesin (unit per hari). Mesin A: hari ke-1 = 40, hari ke-2 = 50, hari ke-3 = 60, hari ke-4 = 70. Mesin B: 60, 60, 60, 60. Mesin C: 50, 60, 70, 80. Kenaikan total produksi dari hari pertama ke hari keempat adalah berapa persen?
A. 30%
B. 40%
C. 50%
D. 60%

**15.** Tabel empat kota. Kota P: penduduk 400 ribu jiwa, luas 200 km². Kota Q: penduduk 600 ribu jiwa, luas 300 km². Kota R: penduduk 450 ribu jiwa, luas 150 km². Kota S: penduduk 300 ribu jiwa, luas 100 km². Pernyataan yang BENAR berdasarkan tabel adalah…
A. Kota P paling padat penduduknya.
B. Kota R paling sedikit penduduknya.
C. Kota S paling rendah kepadatannya.
D. Kepadatan Kota Q sama dengan kepadatan Kota P.

**16.** Tabel kelulusan tiga kelas. Kelas A: 40 siswa, 3/4 di antaranya lulus. Kelas B: 50 siswa, 4/5 di antaranya lulus. Kelas C: 60 siswa, 5/6 di antaranya lulus. Berapa total siswa yang lulus dari ketiga kelas?
A. 120 siswa
B. 110 siswa
C. 125 siswa
D. 130 siswa

### TIU Numerik — perbandingan kuantitatif (Soal 17–20)

**17.** Diketahui X = 25% dari 160 dan Y = 30% dari 150. Hubungan X dan Y adalah…
A. X > Y
B. X < Y
C. X = Y
D. Tidak dapat ditentukan

**18.** Diketahui X = 2/3 × 3/4 × 120 dan Y = 1/2 × 100. Hubungan X dan Y adalah…
A. X > Y
B. X < Y
C. X = Y
D. Tidak dapat ditentukan

**19.** Diketahui X = jumlah semua bilangan ganjil dari 1 sampai 20 dan Y = 100. Hubungan X dan Y adalah…
A. X > Y
B. X < Y
C. X = Y
D. Tidak dapat ditentukan

**20.** Diketahui n bilangan asli. X = 2n dan Y = n + 10. Hubungan X dan Y adalah…
A. X > Y
B. X < Y
C. X = Y
D. Tidak dapat ditentukan

### TIU Numerik — soal cerita multi-langkah (Soal 21–30)

**21.** Sinta membawa uang Rp500.000 untuk membeli buku seharga Rp35.000 per buku. Ia harus menyisihkan Rp80.000 untuk ongkos kirim. Berapa buku MAKSIMAL yang dapat dibeli Sinta?
A. 12 buku
B. 13 buku
C. 14 buku
D. 11 buku

**22.** Pekerja A dapat menyelesaikan suatu pekerjaan dalam 12 hari, pekerja B dalam 18 hari, dan pekerja C dalam 36 hari. Jika ketiganya bekerja bersama, pekerjaan itu selesai dalam…
A. 5 hari
B. 7 hari
C. 6 hari
D. 8 hari

**23.** Harga sebuah jam tangan Rp800.000. Toko memberi diskon 20%, kemudian harga setelah diskon dinaikkan 25%. Harga akhir jam tangan itu adalah…
A. Rp780.000
B. Rp640.000
C. Rp820.000
D. Rp800.000

**24.** Mobil A berangkat pukul 08.00 dengan kecepatan 60 km/jam. Mobil B berangkat pukul 09.00 dari tempat yang sama, searah dengan A, dengan kecepatan 90 km/jam. Mobil B menyusul mobil A pukul…
A. 11.00
B. 10.30
C. 11.30
D. 12.00

**25.** Kelompok I terdiri dari 10 orang dengan nilai rata-rata 75. Kelompok II terdiri dari 20 orang dengan nilai rata-rata 85. Kelompok III terdiri dari 10 orang dengan nilai rata-rata 65. Nilai rata-rata gabungan ketiga kelompok adalah…
A. 75
B. 77,5
C. 78
D. 80

**26.** Umur Budi 3 kali umur Ani. Lima tahun lalu, umur Budi 5 kali umur Ani. Umur Ani sekarang adalah…
A. 8 tahun
B. 12 tahun
C. 10 tahun
D. 15 tahun

**27.** Seorang pedagang membeli 120 baju seharga Rp60.000 per baju. Sebanyak 80 baju terjual dengan harga Rp75.000 per baju, 30 baju terjual obral dengan harga Rp50.000 per baju, dan 10 baju rusak sehingga tidak terjual. Pedagang itu…
A. untung Rp200.000
B. rugi Rp100.000
C. untung Rp500.000
D. untung Rp300.000

**28.** Sebuah proyek dapat diselesaikan oleh 24 pekerja dalam 20 hari. Setelah 8 hari bekerja, 6 pekerja berhenti. Berapa hari LAGI proyek itu selesai (dengan pekerja yang tersisa)?
A. 16 hari
B. 14 hari
C. 18 hari
D. 20 hari

**29.** Seseorang menabung Rp1.200.000 dengan bunga sederhana 10% per tahun. Setelah 2,5 tahun, total uangnya (pokok + bunga) adalah…
A. Rp1.440.000
B. Rp1.560.000
C. Rp1.500.000
D. Rp1.452.000

**30.** Jarak dua kota 360 km. Sebuah mobil melaju dengan kecepatan 90 km/jam dan beristirahat 30 menit di tengah perjalanan. Jika mobil berangkat pukul 07.00, mobil tiba pukul…
A. 11.00
B. 11.30
C. 12.00
D. 12.30

---

## Kunci jawaban + pembahasan

**1. C — 253.** Pola ×2+3: 5×2+3=13, 13×2+3=29, 29×2+3=61, 61×2+3=125 → 125×2+3=253. Jebakan: B (251 = 125×2+1, lupa +3-nya); D (255 = 125×2+5).

**2. B — 162.** Pola 11 (dua lapis operasi berbeda): suku ganjil 2, 6, 18, 54 (×3); suku genap 5, 10, 15, 20 (+5). Suku berikutnya adalah suku ganjil ke-5: 54×3=162. Jebakan: A (25 — melanjutkan lapis genap +5); C (108 = 54×2, pengali tidak naik).

**3. D — 99.** Pola 13 (rekurensi dua suku): 7=2×3+1; 17=2×7+3; 41=2×17+7 → berikutnya 2×41+17=99. Jebakan: A (95 — hitungan 2×41+13, salah mengambil suku sebelumnya); C (101 — tebakan Fibonacci biasa 41+60? tidak ada polanya).

**4. A — 210.** Pola 14 (n³−n): 1³−1=0, 2³−2=6, 3³−3=24, 4³−4=60, 5³−5=120 → 6³−6=210. Jebakan: D (216 = 6³, lupa −6).

**5. B — −110.** Pola 12 (deret mundur): selisih −10, −20, −40, −80 (tiap selisih ×2) → selisih berikutnya −160 → 50−160=−110. Jebakan: C (−30 — mengulang selisih −80); D (10 — memaksakan jawaban positif).

**6. C — 123.** Selisih berlapis ×3: +1, +3, +9, +27 → selisih berikutnya +81 → 42+81=123. Jebakan: A (120 — membulatkan); B (126 — selisih +84, salah kelipatan).

**7. D — 33.** Pola 11: suku ganjil 5, 12, 19, 26 (+7); suku genap 4, 8, 16, 32 (×2). Suku berikutnya adalah suku ganjil ke-5: 26+7=33. Jebakan: B (64 — melanjutkan lapis genap ×2); A (40 — mengira lapis ganjilnya +14).

**8. A — 217.** Pola 14 (n³+1): 1³+1=2, 2³+1=9, 3³+1=28, 4³+1=65, 5³+1=126 → 6³+1=217. Jebakan: C (216 = 6³, lupa +1).

**9. B — 59.** Operasi ganda bergantian: ×2, −3, ×2, −3, ×2, −3 → 10×2=20, 20−3=17, 17×2=34, 34−3=31, 31×2=62, 62−3=59. Jebakan: D (124 — mengulang ×2); A (60 — mengira −2).

**10. C — 226.** Selisih kubik: +1, +8, +27, +64 (1³, 2³, 3³, 4³) → selisih berikutnya +125 → 101+125=226. Jebakan: D (216 = 6³, angka "bulat" yang menggoda); A (222 — selisih +121, salah pangkat).

**11. D — 19.** Operasi ganda bergantian: ÷2, +4 → 96÷2=48, 48+4=52, 52÷2=26, 26+4=30, 30÷2=15, 15+4=19. Jebakan: B (7 — membagi 15 dengan 2 lalu membulatkan ke bawah; padahal giliran +4).

**12. A — 104.** Operasi ganda bergantian: +4, ×2 → 6+4=10, 10×2=20, 20+4=24, 24×2=48, 48+4=52, 52×2=104. Jebakan: B (56 — mengulang +4); C (100 — mengira ×2 dari 50).

**13. C — 60%.** Total gula = 80+100+90 = 270. Total kopi = 120+150+180 = 450. 270 ÷ 450 × 100% = 60%. Jebakan: A (50% — memakai pembagi yang salah); D (65% — membagi dengan total keseluruhan 720? 270÷720≈37,5% — bukan; 65% muncul kalau salah menjumlah kopi menjadi 415).

**14. B — 40%.** Total hari pertama = 40+60+50 = 150. Total hari keempat = 70+60+80 = 210. Kenaikan = (210−150) ÷ 150 × 100% = 60 ÷ 150 = 40%. Jebakan: A (30% — pembagi 210: 60÷210≈28,6% dibulatkan 30%); D (60% — memakai selisihnya sebagai persen, lupa membagi).

**15. D — Kepadatan Kota Q sama dengan kepadatan Kota P.** Kepadatan = penduduk ÷ luas. P: 400.000÷200 = 2.000/km². Q: 600.000÷300 = 2.000/km². R: 450.000÷150 = 3.000/km². S: 300.000÷100 = 3.000/km². Jadi Q = P (paling rendah), R dan S paling padat. Jebakan: A (P tampak besar penduduknya, tapi luasnya juga besar); B (yang paling sedikit penduduknya adalah S, 300 ribu, bukan R); C (S justru paling padat bersama R).

**16. A — 120 siswa.** A: 3/4 × 40 = 30. B: 4/5 × 50 = 40. C: 5/6 × 60 = 50. Total = 30+40+50 = 120. Jebakan: B (110 — salah satu pecahan dihitung keliru, mis. 5/6 × 60 = 40); C (125 — menjumlahkan pembilangnya saja).

**17. B — X < Y.** X = 25% × 160 = 40. Y = 30% × 150 = 45. Jadi X < Y. Jebakan: A (25% < 30% tidak berarti X < Y — tapi di sini kebetulan memang X < Y; yang salah adalah menebak dari persennya saja tanpa menghitung, karena bilangan dasarnya berbeda).

**18. A — X > Y.** X = 2/3 × 3/4 × 120 = 1/2 × 120 = 60. Y = 1/2 × 100 = 50. Jadi X > Y. Jebakan: C (tertipu "sama-sama 1/2" — tapi yang dikalikan berbeda: 120 vs 100).

**19. C — X = Y.** Bilangan ganjil 1 sampai 20: 1, 3, 5, 7, 9, 11, 13, 15, 17, 19 — jumlahnya 100 (jumlah n bilangan ganjil pertama = n²; di sini 10² = 100). Jadi X = Y. Jebakan: A (mengira jumlah 10 bilangan ganjil pasti di atas 100).

**20. D — Tidak dapat ditentukan.** Uji dua nilai n: n = 5 → X = 10, Y = 15 (X < Y). n = 20 → X = 40, Y = 30 (X > Y). Hubungannya berbalik tergantung n, jadi tidak dapat ditentukan. Jebakan: A/B (mengambil satu nilai n lalu menggeneralisasi); C (benar hanya saat n = 10).

**21. A — 12 buku.** Uang yang boleh dipakai = Rp500.000 − Rp80.000 = Rp420.000. Rp420.000 ÷ Rp35.000 = 12 buku tepat. Jebakan: C (14 — Rp500.000 ÷ Rp35.000 = 14,28, lupa menyisihkan ongkir); B (13 — membulatkan 12,0 ke atas tanpa cek uang: 13 buku butuh Rp455.000 > Rp420.000).

**22. C — 6 hari.** Kerja bersama tiga orang: 1/T = 1/12 + 1/18 + 1/36 = 3/36 + 2/36 + 1/36 = 6/36 = 1/6 → T = 6 hari. Jebakan: D (8 — merata-rata waktu); A (5 — salah menjumlah pecahan).

**23. D — Rp800.000.** Setelah diskon: Rp800.000 × 0,8 = Rp640.000. Setelah naik 25%: Rp640.000 × 1,25 = Rp800.000 — kembali ke harga awal (0,8 × 1,25 = 1). Jebakan: B (Rp640.000 — lupa kenaikan setelah diskon); A (Rp780.000 — menghitung −20% +25% = +5% dari harga awal, padahal persen kedua dihitung dari harga setelah diskon).

**24. A — 11.00.** Saat B berangkat (09.00), A sudah jalan 1 jam × 60 km/jam = 60 km di depan. Kecepatan susul = 90 − 60 = 30 km/jam. Waktu susul = 60 ÷ 30 = 2 jam setelah 09.00 → 11.00. Cek: A menempuh 3 jam × 60 = 180 km; B menempuh 2 jam × 90 = 180 km ✓. Jebakan: B (10.30 — menghitung 60 ÷ 40, salah selisih kecepatan); C (11.30 — memakai jarak 360 km yang tidak ada di soal).

**25. B — 77,5.** Total nilai = 10×75 + 20×85 + 10×65 = 750 + 1.700 + 650 = 3.100. Jumlah orang = 40. Rata-rata gabungan = 3.100 ÷ 40 = 77,5. Jebakan: A (75 — rata-rata dari rata-rata (75+85+65)÷3 = 75; kelompoknya tidak sama besar, jadi harus ditimbang jumlah orangnya).

**26. C — 10 tahun.** Misal Ani = x, Budi = 3x. Lima tahun lalu: 3x − 5 = 5(x − 5) → 3x − 5 = 5x − 25 → 20 = 2x → x = 10. Cek: Budi sekarang 30; lima tahun lalu 25 dan 5 → 25 = 5 × 5 ✓. Jebakan: B (12 — salah menyusun persamaan, mis. 3x + 5 = 5(x + 5) yang menghasilkan x negatif lalu dibalik tandanya).

**27. D — untung Rp300.000.** Modal = 120 × Rp60.000 = Rp7.200.000. Pemasukan = 80 × Rp75.000 + 30 × Rp50.000 = Rp6.000.000 + Rp1.500.000 = Rp7.500.000. Untung = Rp7.500.000 − Rp7.200.000 = Rp300.000. Jebakan: C (Rp500.000 — menghitung 10 baju rusak seolah terjual obral juga: 40 × Rp50.000 = Rp2.000.000 → pemasukan Rp8.000.000); B (rugi — fokus pada 10 baju rusak dan lupa margin 80 baju yang terjual penuh menutupinya).

**28. A — 16 hari.** Total pekerjaan = 24 × 20 = 480 pekerja-hari. Setelah 8 hari: 24 × 8 = 192 selesai, sisa 480 − 192 = 288. Pekerja tersisa = 24 − 6 = 18. Waktu lagi = 288 ÷ 18 = 16 hari. Jebakan: D (20 — lupa 8 hari sudah berlalu dan pekerja berkurang); C (18 — memakai 16 pekerja tersisa, salah hitung 24−6).

**29. C — Rp1.500.000.** Bunga sederhana 2,5 tahun = Rp1.200.000 × 10% × 2,5 = Rp300.000. Total = Rp1.200.000 + Rp300.000 = Rp1.500.000. Jebakan: A (Rp1.440.000 — bunga 2 tahun saja, lupa 0,5 tahun); D (Rp1.452.000 — memakai bunga majemuk 2 tahun: Rp1.200.000 × 1,21; soal ini bunga SEDERHANA).

**30. B — 11.30.** Waktu berkendara = 360 ÷ 90 = 4 jam. Tambah istirahat 0,5 jam → total 4,5 jam. Berangkat 07.00 + 4,5 jam = 11.30. Jebakan: A (11.00 — lupa istirahat 30 menit); C (12.00 — menghitung istirahat 1 jam).

---

## Distribusi kunci (terverifikasi sebelum diterbitkan)

A: 8 (No. 4, 8, 12, 16, 18, 21, 24, 28) · B: 7 (No. 2, 5, 9, 14, 17, 25, 30) · C: 8 (No. 1, 6, 10, 13, 19, 22, 26, 29) · D: 7 (No. 3, 7, 11, 15, 20, 23, 27). Maks 26,7% — tidak ada posisi >40% (pelajaran cacat Hari 7 diterapkan). Semua kunci dihitung ulang dari nol oleh Mommy sebelum sesi diterbitkan.

## Setelah mengerjakan

- **Skor sesi ini:** ___ / 30. Target Hari 12: ≥24 benar (≈120 poin TIU — TIU 35 soal × 5 poin = 175; passing grade 80 = 16 benar; target aman 110+ = 22 benar).
- **Buku kesalahan:** soal yang salah diulang **Sabtu, 21 Nov 2026** (3 hari kemudian, sebagai bagian tryout mini + review kesalahan). Tulis nomor soal yang salah + polanya.
- **Status jawabanmu (cek aplikasi 18 Nov 09:55):** Hari 1 (10/10) dan Hari 2b (75/80) sudah kamu kerjakan kemarin — streak 1, XP 348. Yang masih menunggu: simulasi penuh, Hari 8, Hari 9, Hari 10, Hari 11. Kerjakan yang tertinggal saat ada waktu — terutama simulasi, karena prediksi skor jujur hanya bisa dibuat setelah ada data waktu nyata.
- **Besok (Kamis, 19 Nov):** TKP — studi kasus + ulangan soal salah Hari 10 (bila sudah kamu jawab; bila belum, ulangan digeser).
- **Jumat, 20 Nov:** TIU figural + ulangan soal salah Hari 11.
- **Sabtu, 21 Nov:** tryout mini 30 soal campuran + review kesalahan (ulangan soal salah Hari 12 ini).
