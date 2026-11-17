# Latihan CPNS Hari 3 — Minggu, 8 November 2026
**Fokus: Review Mingguan + SKB Ringan (ITIL — Incident Management) · 15 soal baru (Review 10 + SKB 5) · Target: Review ≥8/10, SKB ≥4/5 · Waktu: ~45–60 menit**

*Sesuai rotasi mingguan: Minggu = review mingguan + SKB ringan 1 topik Pranata Komputer. Semua soal di bawah ini BARU — menguji pola yang sama dengan Hari 1–2b, bukan mengulang soalnya. Kerjakan dulu tanpa melihat kunci, baru cek jawaban.*

---

## Review minggu ini — kilas balik pola Hari 1–2b

Total minggu ini: **41 soal** (Hari 1: 10, Hari 2: 15, Hari 2b: 16). Sebelum mengerjakan soal review, baca ulang ringkasan ini — inilah yang diuji hari ini:

| Materi | Pola kunci yang harus diingat |
|---|---|
| **Analogi TIU** (Hari 1) | Buat **kalimat penghubung** ("X digunakan untuk Y"), uji ke semua opsi. Pilih hubungan yang **paling spesifik dan identik**, bukan yang sekadar berhubungan. Arah hubungan tidak boleh terbalik. |
| **Silogisme TIU** (Hari 2, 2b) | "Semua A adalah B, X adalah A → X adalah B." Jangan balik arah (kesalahan paling umum). |
| **Deret angka** (Hari 2b) | Urutan cek: **selisih dulu → rasio kedua → pisah ganjil-genap ketiga**. 5 pola: beda tetap, beda berubah teratur, rasio tetap, dua lapis/loncat, operasi ganda (×n ± m). |
| **TWK** (Hari 2, 2b) | Pasal-pasal yang sudah muncul: Pasal 27 ayat (1) & (2), Pasal 28E ayat (3), Pasal 1 ayat (1) bentuk negara, Sutasoma, sila ke-3, 18 Agustus 1945. Hari ini diuji pasal lain. |
| **TKP** (Hari 2, 2b) | Empat prinsip penilai: **integritas** (lapor & kembalikan sesuai prosedur), **pelayanan prima** (empati + solusi konkret + tetap dalam prosedur), **kerja sama** (komunikasi dulu, cari akar masalah, bantu), **adaptabilitas** (belajar aktif, bertanya, menyesuaikan diri). |

> **Catatan:** Sandi belum mengirim jawaban Hari 1, 2, dan 2b — jadi **buku kesalahan masih kosong** dan belum ada soal yang dijadwalkan ulang 3 hari kemudian. Kirim jawabanmu (mis. "Hari 1: 8/10, salah no 4 dan 9") supaya spaced repetition bisa jalan: soal yang salah muncul lagi 3 hari kemudian.

---

## Soal Review (10 soal baru)

### TWK

**1.** Pembukaan UUD 1945 alinea keempat memuat rumusan…
A. Pancasila
B. Bhinneka Tunggal Ika
C. Teks Proklamasi
D. Sumpah Pemuda

**2.** UUD 1945 Pasal 34 ayat (1) menyatakan bahwa fakir miskin dan anak-anak terlantar…
A. Wajib bekerja
B. Dipelihara oleh negara
C. Mendapat bantuan asing
D. Diasuh oleh keluarga

### TIU Verbal

**3.** BULAN : BUMI = BUMI : …
A. Matahari
B. Mars
C. Bulan
D. Langit

**4.** PENULIS : BUKU = … : …
A. Pelukis : Lukisan
B. Koki : Restoran
C. Guru : Sekolah
D. Dokter : Pasien

### TIU Numerik

**5.** 1, 4, 9, 16, 25, …
A. 30
B. 32
C. 36
D. 49

**6.** 2, 4, 8, 16, 32, …
A. 48
B. 56
C. 64
D. 96

**7.** Harga sebuah laptop Rp6.000.000. Toko memberi diskon 10%, lalu dikenakan pajak 10% dari harga setelah diskon. Harga akhir yang harus dibayar adalah…
A. Rp6.000.000
B. Rp5.940.000
C. Rp5.400.000
D. Rp6.600.000

### TIU Figural

**8.** Sebuah anak panah menunjuk ke atas. Jika anak panah itu dicerminkan pada cermin vertikal (tegak) yang diletakkan di samping kanannya, anak panah akan menunjuk ke…
A. Atas
B. Bawah
C. Kiri
D. Kanan

### TKP

**9.** Kamu melihat rekan kerja memalsukan absensi kehadiran. Sikap terbaikmu adalah…
A. Ikut melakukannya agar tidak ketahuan sendiri
B. Menegurnya langsung di depan semua orang
C. Mengingatkannya secara pribadi dan, bila berlanjut, melaporkannya melalui jalur yang benar
D. Membiarkannya karena bukan urusanmu

**10.** Seorang warga lanjut usia kesulitan memahami prosedur layanan online. Tindakan terbaikmu adalah…
A. Menyuruhnya meminta bantuan keluarganya saja
B. Menjelaskan dengan sabar langkah demi langkah, membantunya mengisi, dan memastikan ia paham
C. Mengisikan semua datanya tanpa bertanya kepadanya
D. Memintanya datang lain hari

---

## Pelajaran fundamental SKB: ITIL — Incident Management

*SKB Pranata Komputer menguji teori dan kerangka kerja, bukan coding. ITIL adalah kerangka yang paling sering keluar. Mulai dari praktik yang paling dasar: Incident Management.*

### 1. Empat istilah yang wajib dibedakan

| Istilah | Arti | Contoh di instansi pemerintah |
|---|---|---|
| **Incident (insiden)** | Gangguan **tak terencana** pada layanan TI atau penurunan kualitas layanan | Aplikasi perizinan down di jam layanan; printer loket mati; jaringan kantor putus |
| **Service request** | Permintaan formal pengguna atas sesuatu yang **disediakan** (bukan gangguan) | Minta reset password; minta akses aplikasi baru; minta instalasi software |
| **Problem** | **Penyebab yang mendasari** satu atau lebih insiden | Server yang sama menyebabkan e-office down 3× seminggu |
| **Known error** | Problem yang akar penyebabnya **sudah diketahui** dan solusinya (workaround) sudah didokumentasikan | "Server X down tiap Jumat karena backup menumpuk — workaround: restart manual" |

### 2. Tujuan Incident Management

**Memulihkan layanan normal secepat mungkin dan meminimalkan dampaknya pada operasional.** Titik. Bukan mencari akar penyebab — itu tugas **Problem Management**. Ini jebakan paling klasik di soal SKB: opsi "mencari akar penyebab" selalu terlihat benar, padahal itu jawaban untuk problem, bukan incident.

### 3. Alur penanganan insiden (hafalkan urutannya)

**Identifikasi → Pencatatan (logging) → Kategorisasi → Prioritisasi → Diagnosis awal → Eskalasi (bila perlu) → Investigasi & diagnosis → Resolusi & pemulihan → Penutupan.**

### 4. Prioritas = Urgensi × Dampak

- **Urgensi:** seberapa cepat layanan harus pulih.
- **Dampak:** seberapa luas/besar kerugiannya.
- Keduanya digabung dalam matriks → prioritas: **kritis / tinggi / sedang / rendah**.
- Contoh: aplikasi layanan perizinan down di jam sibuk = dampak besar + urgensi tinggi → **prioritas kritis**. Satu printer rusak di ruangan yang punya printer cadangan = **prioritas rendah**.

### 5. Dua jenis eskalasi

- **Eskalasi fungsional:** dilempar ke tim/ahli yang lebih spesialis (mis. Service Desk → tim jaringan).
- **Eskalasi hierarkis:** dinaikkan ke manajemen karena butuh keputusan atau sumber daya lebih besar.

### 6. Service Desk

**Satu titik kontak** antara pengguna dan penyedia layanan TI. Service Desk menerima, mencatat, mengategorikan, dan mengarahkan insiden — bukan memperbaiki semuanya sendiri. Perbaikan teknis dilakukan tim terkait lewat eskalasi fungsional.

> **Kaitan dengan SKD:** prinsipnya sama dengan TKP — insiden ditangani dengan prosedur, prioritas, dan komunikasi yang jelas, bukan asal cepat atau asal diam.

---

## Soal SKB — ITIL Incident Management (5 soal baru)

**11.** Menurut ITIL, insiden (incident) adalah…
A. Permintaan pengguna atas layanan baru
B. Gangguan tak terencana pada layanan TI atau penurunan kualitas layanan
C. Penyebab yang mendasari satu atau lebih gangguan
D. Perubahan yang direncanakan pada sistem

**12.** Tujuan utama Incident Management adalah…
A. Mencari akar penyebab gangguan agar tidak terulang
B. Memulihkan layanan normal secepat mungkin dan meminimalkan dampaknya
C. Menyusun anggaran layanan TI tahunan
D. Mengganti seluruh perangkat yang bermasalah

**13.** Prioritas sebuah insiden ditentukan berdasarkan…
A. Jabatan pelapor
B. Waktu insiden dilaporkan
C. Urgensi × dampak
D. Jumlah pengguna yang menelepon service desk

**14.** Sistem e-office di instansimu down tiga kali dalam seminggu karena server yang sama. Tim membuka problem record untuk menelusuri penyebabnya. Alasan yang tepat membuka problem record adalah…
A. Agar insiden selesai lebih cepat
B. Untuk mencari akar penyebab dan mencegah insiden yang sama terulang
C. Karena pengguna meminta fitur baru
D. Untuk mencatat jumlah insiden

**15.** Fungsi utama Service Desk menurut ITIL adalah…
A. Memperbaiki sendiri semua insiden teknis
B. Menjadi satu titik kontak antara pengguna dan penyedia layanan TI
C. Mengawasi jaringan 24 jam
D. Menyetujui perubahan sistem

---

## Kunci jawaban + pembahasan

### Review

**1. A — Pancasila.** Alinea keempat Pembukaan UUD 1945 memuat rumusan dasar negara Pancasila. Bhinneka Tunggal Ika ada di lambang negara Garuda Pancasila; teks Proklamasi dan Sumpah Pemuda adalah dokumen terpisah.

**2. B — Dipelihara oleh negara.** Pasal 34 ayat (1): "Fakir miskin dan anak-anak yang terlantar dipelihara oleh negara." Jebakan: tertukar dengan Pasal 27 ayat (2) soal hak atas pekerjaan.

**3. A — Matahari.** Kalimat: "Bulan mengorbit Bumi." Bumi mengorbit Matahari — hubungan **satelit : benda yang diorbiti**. Mars juga planet tapi bukan yang diorbiti Bumi; langit hanya tempatnya.

**4. A — Pelukis : Lukisan.** Kalimat: "Penulis menghasilkan buku (karya)." Pelukis menghasilkan lukisan — **profesi : karya yang dihasilkan**. Koki : restoran, guru : sekolah, dokter : pasien adalah profesi : tempat/objek kerja.

**5. C — 36.** Pola kuadrat: 1², 2², 3², 4², 5², lalu 6² = **36**. Jebakan: 49 adalah 7² — loncat satu suku.

**6. C — 64.** Pola 3 (rasio tetap): selalu ×2 → 32 × 2 = **64**. Jebakan: 48 = 32 + 16, seolah-olah selisihnya naik — padahal rasionya yang tetap.

**7. B — Rp5.940.000.** Harga setelah diskon: Rp6.000.000 × 90% = Rp5.400.000. Pajak: 10% × Rp5.400.000 = Rp540.000. Total: Rp5.400.000 + Rp540.000 = **Rp5.940.000**. Jebakan: A (Rp6.000.000) muncul kalau pajak dihitung dari harga awal lalu dikurangi diskon — urutan hitungnya salah; C lupa pajak; D pajak ditambah ke harga awal.

**8. A — Atas.** Cermin **vertikal** membalik kiri-kanan saja, bukan atas-bawah — panah yang menunjuk ke atas tetap menunjuk ke atas. Ini kebalikan dari soal Hari 2b no. 13 (cermin horizontal membalik atas-bawah; panah ke kanan tetap ke kanan). Hafalkan: **cermin membalik sumbu yang tegak lurus dengannya**.

**9. C — skor 5.** Integritas + prosedur: ingatkan dulu secara pribadi, laporkan lewat jalur yang benar bila berlanjut. B mempermalukan (bukan cara profesional); A ikut melanggar; D menghindar.

**10. B — skor 5.** Pelayanan prima: empati + penjelasan sabar + bantuan konkret + pastikan paham. A mengusir; C mengambil alih tanpa persetujuan (melanggar prosedur dan privasi data); D mengabaikan kebutuhan.

### SKB — ITIL Incident Management

**11. B — Gangguan tak terencana pada layanan TI atau penurunan kualitas layanan.** A = service request; C = problem; D = change.

**12. B — Memulihkan layanan normal secepat mungkin dan meminimalkan dampaknya.** A adalah tujuan **Problem Management** — jebakan paling klasik. C dan D bukan tujuan praktik ini.

**13. C — Urgensi × dampak.** Prioritas lahir dari matriks urgensi dan dampak. Jabatan pelapor dan jumlah penelpon tidak menentukan prioritas — yang dinilai adalah seberapa cepat harus pulih dan seberapa besar kerugiannya.

**14. B — Untuk mencari akar penyebab dan mencegah insiden yang sama terulang.** Itulah fungsi problem record. A adalah tujuan incident; C adalah service request; D hanya pencatatan.

**15. B — Menjadi satu titik kontak antara pengguna dan penyedia layanan TI.** Service Desk menerima, mencatat, mengategorikan, dan mengarahkan insiden; perbaikan teknis dilakukan tim terkait lewat eskalasi fungsional (A salah), pengawasan jaringan (C) dan persetujuan perubahan (D) adalah fungsi lain.

---

## Setelah mengerjakan

- **Skor review:** ___ / 10. Target: ≥8 benar.
- **Skor SKB:** ___ / 5. Target: ≥4 benar.
- **Skor total Minggu:** ___ / 15.
- **Buku kesalahan:** tulis nomor soal yang salah + polanya (mis. "Soal 7 — diskon lalu pajak, urutan hitung"; "Soal 12 — incident vs problem"). Ulangi soal itu lagi **3 hari kemudian (Rabu, 11 Nov 2026)** — kalau masih salah, itulah kelemahan yang harus dilatih.
- **Kirim juga jawaban Hari 1, 2, dan 2b** kalau belum — tanpa itu, buku kesalahan dan spaced repetition tidak bisa jalan.
- **Besok (Senin, 9 Nov):** TWK — 1 topik + soal, sesuai rotasi. Materi berikutnya: Pasal-pasal UUD 1945 yang paling sering keluar + soal TWK.
