# Latihan CPNS Hari 19 — Rabu, 25 November 2026
**Fokus: TIU Numerik — Deret & Soal Cerita (HARD, Standar Brutal) · 30 soal baru · Target: ≥24 benar (≈120 poin TIU) · Waktu: ~50 menit soal, total sesi ~2 jam**

*Sesuai rotasi mingguan: Rabu = TIU numerik. Semua soal di bawah ini BARU — tidak mengulang satu pun soal Hari 1–18 maupun simulasi (dicek terhadap file Hari 2b, 6, 12, drill estimasi, simulasi 14 Nov, Hari 15, 16). Soal dibuat berpola sama dengan SKD 2023–2024, bukan soal resmi BKN — BKN tidak mempublikasikan soal SKD. Tingkat kesulitan Standar Brutal (setara/lebih berat dari tryout eksternal rekrutmencpns.id Batch #43, 24 Nov: 419/550): ≥60% soal multi-langkah; 1 soal pamungkas outlier (No. 12) gaya patokan kalibrasi; sisanya jebakan kecepatan 30–55 detik. Kerjakan dulu tanpa melihat kunci, baru cek jawaban.*

---

## Pemanasan 60 detik — drill dari kesalahan Hari 12 (kemarin, 26/30)

Tulis jawabannya dari ingatan, tanpa menghitung panjang-panjang. Lalu cek langsung.

1. Deret ÷2/+4: 96, 48, 52, 26, 30, 15, … → berikutnya?
2. Tabel persen "A dari B": total gula 270, total kopi 450 → gula berapa persen dari kopi?
3. Tabel pecahan: 3/4 × 40 + 4/5 × 50 + 5/6 × 60 = … lulus?
4. Diskon-naik: Rp800.000 didiskon 20% lalu dinaikkan 25% → harga akhir?

*Jawaban: 1) 19 (giliran +4 setelah 15 ÷ 2 — yang kemarin kamu jawab 7 karena langsung membagi lagi). 2) 60% (270 ÷ 450 — pembaginya kopi, bukan total gabungan). 3) 120 siswa (30 + 40 + 50 — tiap pecahan dikali jumlah kelasnya sendiri). 4) Rp800.000 (0,8 × 1,25 = 1 — kembali ke harga awal; hari ini No. 30 menghukum refleks "pasti kembali" itu). Empat pola inilah yang menjatuhkanmu kemarin — hari ini masing-masing muncul lagi sebagai variasi baru (No. 27–30).*

---

## Pelajaran fundamental: deret pola 15–18 + analisis tabel + soal cerita multi-langkah

Kamu sudah kuasai 14 pola deret (Hari 2b + Hari 6 + Hari 12). Hari ini 4 pola baru — semuanya masih dipecahkan dengan urutan cek yang sama: **selisih dulu → rasio kedua → pisah ganjil-genap ketiga → tanya "apakah suku ini hasil dari DUA/TIGA suku sebelumnya?"**

### Pola 15 — Selisih = kuadrat atau prima berurutan
Selisihnya sendiri punya pola: 1, 4, 9, 16, 25 (kuadrat) atau 2, 3, 5, 7, 11 (prima).
Contoh: 2, 3, 7, 16, 32, 57, … → selisih 1, 4, 9, 16, 25 → selisih berikutnya 36 → **93**.
Jebakan: mengulang selisih terakhir (57 + 25 = 82) — selalu tulis barisan selisihnya sampai polanya kelihatan.

### Pola 16 — Rekurensi tiga suku (tribonacci)
Tiap suku = jumlah TIGA suku sebelumnya (bukan dua).
Contoh: 1, 2, 3, 6, 11, 20, … → 1+2+3=6; 2+3+6=11; 3+6+11=20 → berikutnya 6+11+20 = **37**.
Cara menemukan: kalau suku ketiga "terlalu besar" untuk jumlah dua suku, uji jumlah tiga suku.

### Pola 17 — Deret pecahan: pisah pembilang & penyebut
Kerjakan sebagai dua deret terpisah.
Contoh: 1/2, 1/3, 2/5, 3/8, 5/13, … → pembilang 1, 1, 2, 3, 5 (Fibonacci); penyebut 2, 3, 5, 8, 13 (Fibonacci) → berikutnya **8/21**.
Jebakan: mengira penyebut naik tetap (+7) — cek kedua lapis, bukan satu.

### Pola 18 — ×k±c dengan k dan c naik berurutan
Pengali dan pengurang/kurangannya sama-sama naik 1 tiap langkah.
Contoh: 2, 3, 7, 25, 121, … → ×2−1, ×3−2, ×4−3, ×5−4 → berikutnya 121×6−5 = **721**.
Cara menemukan: bila hasil lompat besar, uji "kali lalu kurang" — catat pengali dan pengurang tiap langkah.

### Teknik analisis tabel — jumlahkan kolom dulu, pembagi = yang ditanyakan
1. Baca dulu apa yang ditanya: total? selisih? persen dari apa?
2. Jumlahkan per kolom/baris yang relevan SEBELUM menghitung — jangan bandingkan satu sel.
3. Persen "A dari B" → pembaginya B, bukan total keseluruhan. "Kenaikan dari X ke Y" → pembaginya X (nilai awal).
4. "Pernyataan yang BENAR" → hitung rasionya (mis. pengunjung ÷ hari buka), jangan tebak dari angka mentahnya. "Paling tinggi" gugur bila ada yang menyamai (seri ≠ paling).
5. Rata-rata tertimbang: tiap nilai dikali bobotnya dulu, baru dibagi total bobot — jangan merata-rata persen/nilai yang penyebutnya beda.

### Teknik soal cerita — TERJEMAH DULU KE PERSAMAAN
1. **Tulis "yang dicari = ?"** — satu baris, sebelum menghitung apa pun.
2. **Kerja bersama → jumlahkan kebalikan waktu** (1/T = 1/T₁ + 1/T₂ + …), lalu balik hasilnya.
3. **Campuran → timbang tiap bagian dengan volumenya** (jangan merata-rata kadar begitu saja).
4. **Diskon lalu naik → kalikan faktornya** (0,8 × 1,2 = 0,96 — TIDAK kembali ke harga awal; hanya kembali bila faktornya berpasangan, mis. 0,8 × 1,25 = 1).
5. **Rata-rata gabungan → lewat total nilai** (total = rata-rata × jumlah); bila yang dicari jumlah anggota, selisih total ÷ selisih rata-rata.
6. **"n tahun lalu" → kurangkan n dari TIAP orang** (total berkurang 3n untuk tiga orang).

### Hitung Cepat (toolkit Standar Brutal — pakai di semua soal cerita)
1. Bagi dulu baru kali (180 ÷ 9 = 20, lalu 4 × 20).
2. Jumlah 1 sampai n = n(n+1) ÷ 2.
3. 25% = seperempat (bagi 4 langsung); persen dari bilangan berbeda bisa sama nilainya.
4. Mesin vs hari = berbalik nilai: kalikan dulu (mesin × hari), baru bagi dengan mesin tersisa.
5. Pecah perjalanan per ruas (t = s ÷ v), jumlahkan semua jeda istirahatnya.

---

## Soal (30 soal baru)

### TIU Numerik — deret (Soal 1–11)

**1.** Perhatikan deret berikut: 2, 3, 7, 16, 32, 57, … Suku berikutnya adalah …
A. 93
B. 89
C. 97
D. 82
E. 101

**2.** Perhatikan deret berikut: 1, 2, 3, 6, 11, 20, … Suku berikutnya adalah …
A. 34
B. 37
C. 40
D. 31
E. 43

**3.** Perhatikan deret berikut: 3, 7, 6, 13, 12, 19, 24, 25, … Suku berikutnya adalah …
A. 36
B. 44
C. 48
D. 31
E. 52

**4.** Perhatikan deret pecahan berikut: 1/2, 1/3, 2/5, 3/8, 5/13, … Pecahan berikutnya adalah …
A. 5/12
B. 8/20
C. 6/17
D. 8/21
E. 7/18

**5.** Perhatikan deret berikut: 4, 6, 9, 14, 21, 32, … Suku berikutnya adalah …
A. 39
B. 41
C. 43
D. 44
E. 45

**6.** Perhatikan deret berikut: 120, 119, 115, 106, 90, 65, … Suku berikutnya adalah …
A. 35
B. 32
C. 29
D. 25
E. 40

**7.** Perhatikan deret berikut: 2, 3, 7, 25, 121, … Suku berikutnya adalah …
A. 601
B. 625
C. 726
D. 721
E. 731

**8.** Perhatikan deret berikut: 7, 18, 30, 43, 57, 72, … Suku berikutnya adalah …
A. 84
B. 85
C. 86
D. 87
E. 88

**9.** Perhatikan deret berikut: 0, 4, 18, 48, 100, … Suku berikutnya adalah …
A. 180
B. 176
C. 196
D. 150
E. 216

**10.** Perhatikan deret berikut: 2, 5, 16, 33, 100, 201, … Suku berikutnya adalah …
A. 403
B. 604
C. 402
D. 603
E. 606

**11.** Perhatikan deret berikut: 8, 11, 17, 29, 53, … Suku berikutnya adalah …
A. 96
B. 98
C. 100
D. 106
E. 101

### TIU Numerik — perbandingan kuantitatif (Soal 12–15)

**12.** Diketahui a dan b adalah bilangan real tak nol yang memenuhi a³ > b³ dan 1/a > 1/b. Jika P = a dan Q = −1, manakah hubungan yang benar antara kuantitas P dan Q?

A. P > Q
B. P < Q
C. P = Q
D. P = 2Q
E. Hubungan P dan Q tidak dapat ditentukan

**13.** Diketahui P = 3/8 × 160, Q = 45% dari 140, dan R = 0,62 × 100. Manakah hubungan yang benar antara kuantitas P, Q, dan R?

A. P > R > Q
B. Q > R > P
C. R > Q > P
D. Q = R > P
E. Hubungan P, Q, dan R tidak dapat ditentukan.

**14.** Diketahui P = 25% dari 240 dan Q = 40% dari 150. Manakah hubungan yang benar antara kuantitas P dan Q?

A. P > Q
B. P < Q
C. P = Q
D. P = 2Q
E. Hubungan P dan Q tidak dapat ditentukan

**15.** Diketahui P = 1 + 2 + 3 + … + 20 dan Q = 1 + 2 + 3 + … + 14. Manakah hubungan yang benar antara kuantitas P dan Q?

A. P > Q
B. P < Q
C. P = Q
D. P = 2Q
E. Hubungan P dan Q tidak dapat ditentukan

### TIU Numerik — soal cerita multi-langkah (Soal 16–22)

**16.** Empat keran mengisi sebuah bak air. Keran P mengisi bak itu dalam 10 menit, keran Q dalam 15 menit, keran R dalam 20 menit, dan keran S dalam 30 menit. Jika keempat keran dibuka bersamaan, bak itu penuh dalam …
A. 3 menit
B. 4 menit
C. 5 menit
D. 6 menit
E. 7,5 menit

**17.** Sebanyak 200 mL larutan garam berkadar 30% dicampur dengan 300 mL larutan garam berkadar 10%. Kadar garam campuran itu adalah …
A. 12%
B. 15%
C. 18%
D. 20%
E. 22%

**18.** Seorang kurir berangkat pukul 06.30 menempuh 220 km. Ia melaju 100 km pertama dengan kecepatan 50 km/jam, lalu beristirahat 20 menit, melanjutkan 120 km berikutnya dengan kecepatan 60 km/jam, lalu beristirahat 40 menit sebelum sampai di tujuan. Kurir itu tiba pukul …
A. 10.30
B. 10.50
C. 11.10
D. 11.30
E. 11.50

**19.** Sebuah pesanan dapat diselesaikan 12 mesin dalam 18 hari. Setelah 3 mesin rusak dan tidak dapat dipakai, pesanan yang sama diselesaikan mesin yang tersisa dalam …
A. 13,5 hari
B. 18 hari
C. 22,5 hari
D. 27 hari
E. 24 hari

**20.** Kelas A berisi 30 siswa dengan nilai rata-rata 84. Kelas B memiliki nilai rata-rata 72. Jika nilai rata-rata gabungan kedua kelas adalah 80, banyak siswa Kelas B adalah …
A. 15 siswa
B. 10 siswa
C. 20 siswa
D. 30 siswa
E. 60 siswa

**21.** Seorang pedagang membeli 200 kg mangga seharga Rp12.000 per kg. Sebanyak 20 kg mangga busuk sehingga tidak terjual. Sebanyak 100 kg terjual dengan harga Rp18.000 per kg dan sisanya dijual obral Rp10.000 per kg. Pedagang itu …
A. Untung Rp100.000
B. Rugi Rp100.000
C. Untung Rp400.000
D. Untung Rp200.000
E. Untung Rp600.000

**22.** Umur ayah 3 kali umur Budi. Umur ibu 2 tahun lebih muda dari ayah. Enam tahun lalu, jumlah umur ayah, ibu, dan Budi adalah 50 tahun. Umur ayah sekarang adalah …
A. 24 tahun
B. 26 tahun
C. 28 tahun
D. 34 tahun
E. 30 tahun

### TIU Numerik — analisis tabel (Soal 23–26)

**23.** Tabel panen padi tiga desa (ton):
Desa Mawar — Januari 120, Februari 150, Maret 180
Desa Melati — Januari 100, Februari 130, Maret 160
Desa Kenanga — Januari 80, Februari 110, Maret 140
Kenaikan total panen dari Januari ke Maret adalah berapa persen?
A. 60%
B. 50%
C. 37,5%
D. 75%
E. 30%

**24.** Tabel nilai rata-rata kelas (skala 100):
Matematika (bobot 4) — Semester 1: 72, Semester 2: 78
Bahasa Indonesia (bobot 3) — Semester 1: 80, Semester 2: 84
IPA (bobot 3) — Semester 1: 68, Semester 2: 76
Rata-rata tertimbang nilai Semester 2 adalah …
A. 78,0
B. 79,2
C. 79,3
D. 80,0
E. 79,0

**25.** Tabel anggaran tiga dinas (miliar rupiah):
Dinas Pendidikan — Pagu 200, Realisasi 150
Dinas Kesehatan — Pagu 100, Realisasi 90
Dinas PU — Pagu 300, Realisasi 180
Total realisasi ketiga dinas adalah berapa persen dari total pagu ketiga dinas?
A. 60%
B. 65%
C. 70%
D. 75%
E. 90%

**26.** Tabel kunjungan ke Taman Kota:
Januari — 12.000 pengunjung, 24 hari buka
Februari — 11.000 pengunjung, 22 hari buka
Maret — 15.000 pengunjung, 25 hari buka
April — 14.400 pengunjung, 24 hari buka
Pernyataan yang BENAR berdasarkan tabel adalah …
A. Rata-rata pengunjung harian Februari lebih tinggi daripada Januari.
B. Rata-rata pengunjung harian Maret paling tinggi di antara keempat bulan.
C. Total pengunjung April lebih banyak daripada total pengunjung Maret.
D. Rata-rata pengunjung harian Januari paling rendah di antara keempat bulan.
E. Rata-rata harian Maret sama dengan rata-rata harian April.

### TIU Numerik — ulangan variasi soal salah Hari 12 (Soal 27–30)

**27.** [Ulangan variasi Hari 12 No. 11 — deret ÷2/+4] 72, 36, 40, 20, 24, 12, …
Suku berikutnya adalah …
A. 16
B. 6
C. 12
D. 20
E. 8

**28.** [Ulangan variasi Hari 12 No. 13 — persen total dari total] Tabel produksi dua pabrik (unit):
Pabrik Jaya — Januari 280, Februari 300, Maret 320
Pabrik Makmur — Januari 200, Februari 260, Maret 260
Total produksi Pabrik Makmur selama tiga bulan adalah berapa persen dari total produksi Pabrik Jaya?
A. 71,4%
B. 80%
C. 81,3%
D. 86,7%
E. 44,4%

**29.** [Ulangan variasi Hari 12 No. 16 — total lulus dari pecahan tiap kelompok] Tiga batch pelatihan kerja: Batch I berisi 40 peserta dan 3/4 di antaranya lulus. Batch II berisi 50 peserta dan 7/10 di antaranya lulus. Batch III berisi 60 peserta dan 5/6 di antaranya lulus. Berapa total peserta yang lulus dari ketiga batch?
A. 105 peserta
B. 110 peserta
C. 115 peserta
D. 120 peserta
E. 125 peserta

**30.** [Ulangan variasi Hari 12 No. 23 — diskon lalu naik] Harga sebuah tas kulit Rp750.000. Toko memberi diskon 20%, kemudian harga setelah diskon dinaikkan 20%. Harga akhir tas kulit itu adalah …
A. Rp600.000
B. Rp750.000
C. Rp660.000
D. Rp720.000
E. Rp900.000

---

## Kunci jawaban + pembahasan

**1. A — 93.** Selisih kuadrat: 1, 4, 9, 16, 25 → 36 → 57+36=93. Jebakan: 82 (mengulang selisih 25); 89 (selisih dikira 32).
**2. B — 37.** Rekurensi tiga suku: 1+2+3=6; 2+3+6=11; 3+6+11=20 → 6+11+20=37. Jebakan: 31 (hanya jumlah dua suku, Fibonacci biasa).
**3. C — 48.** Dua lapis: ganjil 3, 6, 12, 24 (×2); genap 7, 13, 19, 25 (+6). Suku ke-9 ganjil: 24×2=48. Jebakan: 31 (melanjutkan lapis genap padahal giliran ganjil).
**4. D — 8/21.** Pembilang 1, 1, 2, 3, 5 → 8; penyebut 2, 3, 5, 8, 13 → 21. Jebakan: 8/20 (penyebut dikira +7).
**5. E — 45.** Selisih prima 2, 3, 5, 7, 11 → 13 → 32+13=45. Jebakan: 43 (mengulang selisih 11).
**6. C — 29.** Selisih −1, −4, −9, −16, −25 → −36 → 65−36=29. Jebakan: 40 (mengulang selisih −25).
**7. D — 721.** ×2−1, ×3−2, ×4−3, ×5−4 → 121×6−5=721. Jebakan: 726 (lupa mengurangi 5).
**8. E — 88.** Selisih 11, 12, 13, 14, 15 → 16 → 72+16=88. Jebakan: 87 (mengulang selisih 15).
**9. A — 180.** n³−n²: 1−1=0; 8−4=4; 27−9=18; 64−16=48; 125−25=100 → 216−36=180. Jebakan: 216 (6³, lupa −36).
**10. B — 604.** Operasi bergantian ×2+1, ×3+1: 2→5→16→33→100→201 → 201×3+1=604. Jebakan: 403 (mengulang ×2+1 padahal giliran ×3+1).
**11. E — 101.** ×2−5: 8→11→17→29→53 → 53×2−5=101. Jebakan: 106 (lupa mengurangi 5).
**12. A — P > Q.** a³ > b³ setara a > b. Uji tanda: sama-sama positif → 1/a > 1/b berarti b > a (bertentangan); sama-sama negatif → sama (bertentangan); a negatif & b positif → 1/a < 0 < 1/b (bertentangan). Tersisa a positif & b negatif → P = a > 0 > −1 = Q. Jebakan: E (menebak "tidak dapat ditentukan" karena a, b tampak bebas).
**13. B — Q > R > P.** P = 3/8 × 160 = 60; Q = 45% × 140 = 63; R = 0,62 × 100 = 62. Jebakan: menebak dari persennya saja (62% > 45% lalu menyimpulkan R > Q — lupa pengalinya beda, 100 vs 140); mengira P terbesar karena 160 terbesar; membulatkan 62 ≈ 63 lalu memilih Q = R > P (opsi D).

**14. C — P = Q.** P = 25% × 240 = 60; Q = 40% × 150 = 60. Jebakan: melihat 40% > 25% langsung menebak P < Q.
**15. D — P = 2Q.** P = 20×21÷2 = 210; Q = 14×15÷2 = 105; 210 = 2 × 105. Jebakan: menjumlah satu per satu; salah rumus n(n−1)÷2.
**16. B — 4 menit.** 1/10+1/15+1/20+1/30 = 15/60 = 1/4 → 1 ÷ 1/4 = 4 menit. Jebakan: merata-rata waktu (18,75 menit).
**17. C — 18%.** Garam 200×30% = 60; 300×10% = 30; total 90 ÷ 500 = 18%. Jebakan: rata-rata sederhana (30%+10%)÷2 = 20%.
**18. D — 11.30.** Ruas 1: 100÷50 = 2 jam → 08.30; istirahat 20 mnt → 08.50; ruas 2: 120÷60 = 2 jam → 10.50; istirahat 40 mnt → 11.30. Jebakan: 10.30 (kedua istirahat dilewatkan).
**19. E — 24 hari.** Total 12×18 = 216 mesin-hari; mesin tersisa 9 → 216÷9 = 24 hari. Jebakan: arah senilai (13,5 hari — makin sedikit mesin kok makin cepat).
**20. A — 15 siswa.** (2.520+72n)÷(30+n) = 80 → 120 = 8n → n = 15. Jebakan: 10 (membagi 120 dengan 12, selisih 84−72 — pembagi benar 80−72 = 8).
**21. D — untung Rp200.000.** Modal 200×12.000 = 2.400.000; pemasukan 100×18.000 + 80×10.000 = 2.600.000; selisih 200.000. Jebakan: 400.000 (lupa 20 kg busuk, sisa obral dihitung 100 kg).
**22. E — 30 tahun.** Ayah 3x, ibu 3x−2, Budi x; 6 thn lalu (3x−6)+(3x−8)+(x−6) = 50 → 7x = 70 → x = 10 → ayah 30. Jebakan: 24 (umur ayah 6 tahun lalu); 28 (umur ibu sekarang).
**23. A — 60%.** Total Jan 300 ton; total Mar 480 ton; (480−300)÷300 = 60%. Jebakan: satu desa saja (Mawar 50%, Kenanga 75%); pembagi nilai akhir (37,5%).
**24. B — 79,2.** (78×4 + 84×3 + 76×3) ÷ 10 = 792 ÷ 10 = 79,2. Jebakan: rata-rata sederhana 79,3 (mengabaikan bobot).
**25. C — 70%.** Total pagu 600; total realisasi 420; 420÷600 = 70%. Jebakan: rata-rata persen tiap dinas (75%+90%+60%)÷3 = 75%.
**26. E — Maret = April.** Harian: Jan 500; Feb 500; Mar 600; Apr 600. Jebakan: B (total Maret tertinggi tapi hari bukanya juga paling banyak — hariannya seri dengan April).
**27. A — 16.** ÷2, +4 bergantian: 72→36→40→20→24→12 → +4 = 16. Jebakan: 6 (langsung ÷2 lagi padahal giliran +4).
**28. B — 80%.** Jaya 900; Makmur 720; 720÷900 = 80%. Jebakan: rasio satu bulan saja (Januari 71,4%).
**29. C — 115 peserta.** 3/4×40 = 30; 7/10×50 = 35; 5/6×60 = 50; total 115. Jebakan: salah baca satu pecahan (105/110).
**30. D — Rp720.000.** 750.000×0,8 = 600.000; ×1,2 = 720.000 (faktor gabungan 0,96 — TIDAK kembali ke harga awal). Jebakan: Rp750.000 (refleks "diskon lalu naik pasti kembali").

## Distribusi kunci (terverifikasi sebelum diterbitkan)

A: 6 (No. 1, 9, 12, 20, 23, 27) · B: 6 (No. 2, 10, 13, 16, 24, 28) · C: 6 (No. 3, 6, 14, 17, 25, 29) · D: 6 (No. 4, 7, 15, 18, 21, 30) · E: 6 (No. 5, 8, 11, 19, 22, 26). Maks 20% per posisi — tidak ada posisi >40%. Tidak ada tiga kunci berurutan yang sama. Semua kunci dihitung ulang dari nol oleh Mommy (audit buta 30/30) sebelum sesi diterbitkan; 2 cacat draf diperbaiki sebelum submit: No. 29 batang soal menyebut total peserta 129 padahal 40+50+60=150 (angka total dihapus), No. 26 opsi kunci dipadatkan agar bukan opsi terpanjang unik.

## Setelah mengerjakan

- **Skor sesi ini:** ___ / 30. Target Hari 19: ≥24 benar (≈120 poin TIU — TIU 35 soal × 5 poin = 175; passing grade 80 = 16 benar; target aman 110+ = 22 benar).
- **Buku kesalahan:** soal yang salah diulang **Sabtu, 28 Nov 2026** (3 hari kemudian). Tulis nomor soal yang salah + polanya. Buku Kesalahan saat ini: 26 kartu aktif jatuh tempo hari ini — kerjakan mode FSRS di tab Buku.
- **Status jawabanmu (cek aplikasi 25 Nov 09:57):** XP 1.630, Elo 1.862 (TWK 1.876, TIU 1.797, TKP 1.879), streak 2 (23–24 Nov). Terakhir dikerjakan: Hari 12 (24 Nov, 26/30). Yang masih menunggu: Hari 9, 13, 14, 15, 16, 17, 18. Pola lemah terkonfirmasi: analisis tabel (3× belum nilai penuh) — sesi ini memuat 6 soal tabel (No. 23–26 + ulangan 28–29).
- **Besok (Kamis, 26 Nov):** TKP — studi kasus + ulangan soal salah Hari 17 (bila sudah kamu jawab; bila belum, ulangan digeser).
- **Jumat, 27 Nov:** TIU figural + ulangan soal salah Hari 18.
- **Sabtu, 28 Nov:** tryout mini 30 soal campuran + review kesalahan (ulangan soal salah Hari 19 ini).
