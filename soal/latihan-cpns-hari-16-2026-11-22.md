# Latihan CPNS Hari 16 — Minggu, 22 November 2026
**Fokus: Review Mingguan + SKB Ringan Topik #3 (Normalisasi Database) · 20 soal BARU · 5 opsi (A–E) · Target: review ≥8/10 benar · SKB ≥4/5 benar · Ulangan variasi 5/5 · Waktu soal: ~40 menit, total sesi ~2 jam termasuk pelajaran**

*Sesuai rotasi mingguan: Minggu = review mingguan + SKB ringan 1 topik Pranata Komputer. Semua soal memakai 5 opsi (A–E) seperti CAT BKN asli (format baru sejak Hari 15). Semua 20 soal di bawah ini BARU — tidak satu pun mendaur ulang soal Hari 1–15, simulasi, maupun Bedah HOTS; 5 soal ulangan adalah VARIASI BARU dari soal simulasi yang salah (skenario/angka/nama berbeda, pola yang sama). Soal dibuat berpola sama dengan SKD 2023–2024 (bukan soal resmi BKN — BKN tidak mempublikasikan soal SKD). Di aplikasi web, soal-soal ini dikerjakan dengan klik; file ini adalah arsip.*

## Pelajaran fundamental: kilas balik minggu ini + Normalisasi Database

### 0. Pemanasan 60 detik — tiga pola lemah dari dasbor
- **Silogisme:** "sebagian" di tengah rantai = rantai PUTUS → "tidak dapat disimpulkan" (Sim No. 32). TAPI "sebagian" di AWAL rantai + "semua" sesudahnya = kesimpulan "sebagian" yang VALID (soal 4 hari ini). Bedakan posisi "sebagian"-nya.
- **Analogi gambar:** tulis KEDUA lapis transformasi (jumlah + isi) sebelum memilih — Hari 15 No. 20: ×2 + balik isi. Hari ini: ×3 + balik isi (soal 9).
- **Pencerminan (Hari 2b No. 13):** cermin vertikal membalik kiri-kanan; bangun yang simetris kiri-kanan tidak berubah.

### 1. Kilas balik 7 pola minggu ini (Hari 10–15)
1. **TWK Bahasa Indonesia:** ide pokok = gagasan yang mencakup SELURUH teks, bukan satu contoh; coret opsi yang hanya mengambil satu kalimat.
2. **TWK narasi panjang:** tentukan prinsipnya dulu (netralitas, integritas, kerahasiaan data), lalu pilih opsi PALING LENGKAP (tolak + sopan + laporkan).
3. **Implementasi pasal dalam kasus:** hafalkan frasa kunci tiap pasal — pasal berdekatan sengaja dipakai sebagai pengecoh (33 ayat 1 vs 2 vs 3 vs 4).
4. **Silogisme 3 premis:** gambar rantainya; "sebagian" di tengah memutus, "sebagian" di awal + "semua" sesudahnya memberi kesimpulan "sebagian" yang valid.
5. **Deret dua lapis:** bila satu operasi tidak konsisten, pisah ganjil-genap atau uji dua operasi bergantian.
6. **Soal cerita → persamaan:** terjemah dulu ke persamaan, baru hitung; tulis totalnya dulu (pekerja-hari, total nilai, total uang) sebelum membagi.
7. **TKP HOTS:** rumus 5 poin v2 — AKTIF + KONKRET + PROSEDURAL + LIBATKAN PIHAK TEPAT + JEJAK TERTULIS. Panjang opsi bukan petunjuk.

### 2. SKB ringan — Normalisasi Database (topik #3)
- **Kenapa dinormalisasi:** menghilangkan redundansi (data yang sama disimpan berulang) dan tiga anomali: **penyisipan** (tidak bisa menambah data karena kunci belum ada), **pembaruan** (ubah satu fakta harus ubah di banyak baris), **penghapusan** (hapus satu baris ikut menghapus fakta lain).
- **Dependensi fungsional:** X → Y artinya nilai X menentukan nilai Y (contoh: NIM → NamaMahasiswa). **Determinan** = sisi kiri (X). **Candidate key** = atribut/kombinasi minimal yang menentukan semua atribut lain.
- **1NF:** tiap sel bernilai ATOMIK (satu nilai, bukan daftar) dan tidak ada repeating group. "Hobi: Membaca, Memancing" dalam satu sel = melanggar 1NF.
- **2NF:** sudah 1NF + TIDAK ADA dependensi parsial — tidak ada atribut non-kunci yang hanya bergantung pada SEBAGIAN kunci primer gabungan. Kunci primer tunggal = otomatis lolos 2NF.
- **3NF:** sudah 2NF + TIDAK ADA dependensi transitif — atribut non-kunci tidak boleh bergantung pada atribut non-kunci lain (NIP → KodeDept → NamaDept = melanggar 3NF).
- **BCNF:** bentuk 3NF yang lebih ketat — SETIAP determinan harus merupakan candidate key. Semua relasi BCNF pasti 3NF; tidak semua 3NF adalah BCNF.
- **Cara kerja:** temukan dependensi fungsionalnya → pisahkan tabel di sepanjang dependensi yang melanggar → kunci asing (foreign key) menjaga hubungannya.

### 3. Review kesalahan
- **Ulangan hari ini (soal 16–20):** variasi baru dari 5 soal simulasi yang salah — Sim No. 21 (sila Pancasila), No. 31 (duduk melingkar), No. 32 (silogisme "sebagian"), No. 50 (analisis tabel), No. 56 (matriks XOR).
- **Tidak ada ulangan Hari 13:** Hari 13 (TKP HOTS) belum dijawab Sandi — ulangannya digeser ke hari setelah Hari 13 dikerjakan. Ulangan Hari 15 jatuh Selasa, 24 Nov 2026.
- **Buku kesalahan:** 16 kartu aktif, semua jatuh tempo hari ini — kerjakan lewat mode FSRS di tab Buku.
- Soal yang salah di sesi ini diulang Rabu, 25 Nov 2026 (3 hari kemudian).

### 4. Aturan main sesi ini
- Kerjakan di aplikasi (klik). Tandai soal yang ragu dan lewati — kembali di akhir. Jangan kosongkan soal.
- Soal yang salah masuk buku kesalahan (diulang 3 hari kemudian, Rabu 25 Nov).

---

## Soal — Bagian A: Review Mingguan (Soal 1–10)

**1.** Bacalah teks berikut.

Pasar tradisional di banyak kota mulai ditinggalkan pembeli karena bangunannya kumuh, becek saat hujan, dan tidak ada area parkir yang memadai. Pemerintah daerah lalu merenovasi pasar: atap diperbaiki, lantai dikeringkan, los pedagang ditata, dan area parkir ditambah. Namun, renovasi saja tidak cukup. Tanpa penataan pedagang kaki lima di sekitar pasar dan tanpa promosi agar pembeli kembali, pasar yang sudah bagus akan kembali sepi. Pasar yang hidup membutuhkan bangunan yang layak dan pembeli yang kembali datang.

Ide pokok teks di atas adalah …

A. Keberhasilan revitalisasi pasar tradisional bergantung pada bangunan layak dan kembalinya pembeli.
B. Pasar tradisional mulai ditinggalkan pembeli karena bangunannya yang kumuh dan becek saat hujan deras.
C. Pemerintah daerah merenovasi pasar dengan memperbaiki atap dan lantai serta menata los pedagang.
D. Pedagang kaki lima di sekitar pasar harus ditata agar tidak mengganggu kenyamanan pembeli.
E. Area parkir yang memadai membuat pembeli nyaman berbelanja di pasar tradisional itu setiap hari.

**Kunci: A.** (1) Prinsip: ide pokok merangkum seluruh teks. Kalimat penutup menegaskan dua hal sekaligus: bangunan yang layak DAN pembeli yang kembali datang. Karena itu kunci A. B hanya mengambil penyebab awal (bangunan kumuh); C hanya satu bagian renovasi (atap dan lantai); D hanya satu syarat tambahan (kaki lima); E hanya satu fasilitas (parkir). (2) Langkah: 1. Cari gagasan yang mencakup seluruh paragraf, bukan satu contoh. 2. Coret opsi yang hanya mengambil satu kalimat. 3. Pilih opsi yang memuat kedua penentu dari kalimat penutup: bangunan layak dan pembeli kembali. (3) Trik: Opsi yang menyebut satu contoh (atap, parkir, kaki lima) hampir selalu bukan ide pokok — ide pokok merangkum semuanya. (4) Jebakan: B terdengar benar karena teks dibuka dengan pasar yang ditinggalkan — padahal itu hanya latar masalah, bukan gagasan yang dirangkum seluruh teks.

**Jebakan:** B terdengar benar karena teks dibuka dengan pasar yang ditinggalkan — padahal itu hanya latar masalah, bukan gagasan yang dirangkum seluruh teks.

**2.** Seorang ASN diminta tim sukses seorang calon kepala daerah untuk membagikan konten kampanye calon itu di grup WhatsApp keluarganya. ASN itu sebaiknya …

A. Membagikan konten kampanye itu karena grup keluarga bukan forum resmi dan tidak ada yang mengawasi isinya di sana.
B. Membagikan konten kampanye itu tetapi menghapusnya setelah beberapa jam agar tidak meninggalkan jejak di grup itu.
C. Menolak membagikan konten itu tetapi tidak melaporkannya karena takut dianggap tidak sopan kepada tim sukses.
D. Menolak membagikan konten kampanye dan menjaga netralitas serta melaporkan permintaan itu kepada atasan atau pengawas.
E. Membagikan konten itu dengan catatan hanya meneruskan bukan mendukung agar tidak dianggap berpihak kepada calon itu sendiri.

**Kunci: D.** (1) Prinsip: netralitas ASN berlaku juga di media sosial dan grup pribadi — 'grup keluarga' bukan pengecualian. Kunci D menolak membagikan, menjaga netralitas, dan melaporkan permintaan itu. A dan B membagikan konten dengan dalih grup keluarga dan menghapus jejak; C menolak tetapi tidak melapor karena takut dianggap tidak sopan; E membagikan dengan catatan 'hanya meneruskan' — dalih yang tidak menghapus keberpihakan. (2) Langkah: 1. Tentukan prinsipnya: netralitas ASN. 2. Coret semua opsi yang membagikan, apa pun dalihnya. 3. Pilih opsi yang menolak, menjaga netralitas, dan melaporkan. (3) Trik: Dalih 'grup keluarga' atau 'hanya meneruskan' tidak menghapus keberpihakan — yang dinilai adalah perbuatannya. (4) Jebakan: C adalah jebakan utama: menolak saja terasa sudah cukup, padahal permintaan dari tim sukses harus dilaporkan agar tercatat dan tidak terulang.

**Jebakan:** C adalah jebakan utama: menolak saja terasa sudah cukup, padahal permintaan dari tim sukses harus dilaporkan agar tercatat dan tidak terulang.

**3.** Pemerintah menetapkan bahwa distribusi listrik ke seluruh pelosok negeri tetap dikuasai oleh negara, karena listrik merupakan cabang produksi yang penting dan menguasai hajat hidup orang banyak. Ketetapan tersebut didasarkan pada UUD 1945 Pasal …

A. 33 ayat (1)
B. 33 ayat (2)
C. 33 ayat (3)
D. 33 ayat (4)
E. 34 ayat (1)

**Kunci: B.** (1) B karena Pasal 33 ayat (2) berbunyi cabang-cabang produksi yang penting bagi negara dan yang menguasai hajat hidup orang banyak dikuasai oleh negara. (2) Langkah: 1. Cari frasa kunci soal: cabang produksi penting + menguasai hajat hidup orang banyak. 2. Cocokkan dengan bunyi tiap ayat Pasal 33. 3. Coret ayat yang frasanya berbeda walau pasalnya sama. (3) Trik: hafalkan keempat ayat Pasal 33 berpasangan — (1) usaha bersama, (2) cabang produksi penting, (3) bumi/air/kekayaan alam, (4) demokrasi ekonomi.

**Jebakan:** Opsi C (33 ayat 3) menggoda karena sama-sama soal penguasaan negara, tetapi ayat (3) mengatur bumi, air, dan kekayaan alam yang terkandung di dalamnya — bukan cabang produksi.

**4.** Premis 1: Sebagian mahasiswa penerima beasiswa adalah mahasiswa berprestasi. Premis 2: Semua mahasiswa berprestasi mendapat prioritas magang. Kesimpulan yang PASTI benar adalah …

A. Semua mahasiswa penerima beasiswa mendapat prioritas magang.
B. Tidak dapat disimpulkan.
C. Sebagian mahasiswa penerima beasiswa mendapat prioritas magang.
D. Semua mahasiswa berprestasi adalah penerima beasiswa.
E. Sebagian mahasiswa berprestasi bukan penerima beasiswa.

**Kunci: C.** (1) C karena 'sebagian' di AWAL rantai + 'semua' sesudahnya memberi kesimpulan 'sebagian' yang sah: ada penerima beasiswa yang berprestasi, dan semua yang berprestasi mendapat prioritas magang. (2) Langkah: 1. Tulis dengan simbol: B = penerima beasiswa, P = mahasiswa berprestasi, M = mendapat prioritas magang. Premis 1: sebagian penerima beasiswa adalah mahasiswa berprestasi (B ∩ P ≠ ∅) — irisan ini pasti ada isinya. Premis 2: semua mahasiswa berprestasi mendapat prioritas magang (P ⊆ M). 2. Terapkan premis 2 pada irisan premis 1: seluruh irisan (B ∩ P) berada di dalam P, jadi seluruhnya mendapat prioritas magang. 3. Kesimpulan mengikuti kuantor terlemah yang dijamin premis, yaitu 'sebagian': sebagian penerima beasiswa mendapat prioritas magang (B ∩ M ≠ ∅). 4. Opsi A ('semua penerima beasiswa') terlalu luas — premis 1 hanya menjamin sebagian. (3) Trik: 'sebagian' di awal rantai TIDAK memutus rantai — yang memutus adalah 'sebagian' di TENGAH rantai.

**Jebakan:** Opsi B menggoda karena 'sebagian' terasa seperti rantai putus, padahal di sini 'sebagian' berada di awal rantai dan premis kedua berlaku untuk seluruh kelompok kedua — jadi kesimpulan parsialnya valid.

**5.** Sebagaimana kunci membuka gembok agar pintu dapat dibuka, maka …

A. payung dipakai agar tubuh tidak basah saat hujan
B. peta dibaca agar perjalanan tidak tersesat
C. kacamata dipakai agar penglihatan menjadi jelas
D. obat diminum agar penyakit sembuh
E. kata sandi dimasukkan agar akun dapat diakses

**Kunci: E.** (1) E karena kunci adalah alat yang membuka penghalang (gembok) agar akses (pintu) terbuka — kata sandi adalah alat yang membuka penghalang (kunci akun) agar akses (akun) terbuka. (2) Langkah: 1. Cari kata kerja penghubung soal: alat membuka penghalang agar akses terbuka. 2. Uji tiap opsi: hanya E yang alatnya berfungsi membuka penghalang akses. 3. Opsi lain adalah alat pelindung, penuntun, pembantu, atau penyembuh. (3) Trik: samakan FUNGSI kata kerjanya (membuka penghalang), bukan sekadar bentuk kalimatnya.

**Jebakan:** Opsi A tampak mirip karena sama-sama alat yang dipakai, padahal payung berfungsi melindungi dari hujan, bukan membuka penghalang agar akses terbuka.

**6.** 3, 9, 8, 24, 23, 69, 68, …

A. 204
B. 207
C. 203
D. 205
E. 201

**Kunci: A.** (1) A karena operasinya bergantian ×3 lalu −1. (2) Langkah: 1. 3 × 3 = 9. 2. 9 − 1 = 8. 3. 8 × 3 = 24, 24 − 1 = 23, 23 × 3 = 69, 69 − 1 = 68, jadi berikutnya 68 × 3 = 204. (3) Trik: bila satu operasi tidak konsisten, uji dua operasi yang bergantian — dan perhatikan gilirannya, jangan lanjutkan lapis yang salah.

**Jebakan:** Opsi B (207) muncul bila menghitung 69 × 3 — padahal giliran berikutnya adalah lapis ×3 dari 68, bukan dari 69.

**7.** Sebuah proyek dapat diselesaikan oleh 24 pekerja dalam 30 hari. Setelah 12 hari bekerja, 8 pekerja dipindahkan ke proyek lain. Berapa hari LAGI proyek itu selesai (dengan pekerja yang tersisa)?

A. 18 hari
B. 24 hari
C. 27 hari
D. 30 hari
E. 36 hari

**Kunci: C.** (1) C karena sisa pekerjaan dibagi pekerja yang tersisa, bukan pekerja awal. (2) Langkah: 1. Total pekerjaan = 24 × 30 = 720 pekerja-hari. 2. Sudah dikerjakan 12 hari: 24 × 12 = 288, sisa 720 − 288 = 432. 3. Pekerja tersisa 24 − 8 = 16 → 432 ÷ 16 = 27 hari lagi. (3) Trik: hitung total pekerja-hari dulu, kurangkan yang sudah dikerjakan, baru bagi dengan pekerja yang tersisa.

**Jebakan:** Opsi A (18 hari) muncul bila membagi sisa pekerjaan dengan 24 pekerja awal (432 ÷ 24) — lupa 8 pekerja sudah dipindahkan.

**8.** Perhatikan tabel penjualan empat cabang (dalam juta rupiah) berikut.

| Cabang | Januari | Februari | Maret |
| A | 120 | 150 | 180 |
| B | 140 | 130 | 160 |
| C | 110 | 170 | 150 |
| D | 160 | 140 | 130 |

Rata-rata penjualan bulan Maret keempat cabang adalah …

A. 150 juta
B. 155 juta
C. 160 juta
D. 145 juta
E. 165 juta

**Kunci: B.** (1) B karena rata-rata Maret = (180 + 160 + 150 + 130) ÷ 4 = 620 ÷ 4 = 155. (2) Langkah: 1. Ambil hanya kolom Maret, jangan campur kolom lain. 2. Jumlahkan keempat angka itu. 3. Bagi dengan banyak cabang (4), bukan banyak bulan. (3) Trik: pada soal tabel, garis bawahi dulu kolom dan baris yang ditanya sebelum menghitung apa pun.

**Jebakan:** Opsi A (150 juta) menggoda karena angka 150 muncul di tabel (Februari cabang A dan Maret cabang C) — tetapi yang ditanya adalah rata-rata kolom Maret; jumlahkan keempat angka Maret (620) lalu bagi dengan banyak cabang (4).

**9.** Perhatikan analogi gambar berikut. Gambar yang tepat untuk melengkapi analogi itu adalah…


*▲(penuh) : △△△(kosong)  =  ●(penuh) : ?*

A. ●●●● (4 penuh)
B. ○○ (2 kosong)
C. ●●● (3 penuh)
D. ○ (1 kosong)
E. ○○○ (3 kosong)

**Kunci: E.** (1) E karena transformasinya dua lapis: jumlah bangun dikalikan tiga (×3) DAN isi dibalik (penuh → kosong); 1 lingkaran penuh menjadi 3 lingkaran kosong. (2) Langkah: 1. Periksa A → B: 1 segitiga penuh menjadi 3 segitiga kosong — jumlah ×3 dan isi berbalik. 2. Terapkan ke C: 1 × 3 = 3 lingkaran, isi penuh → kosong. (3) Trik: analogi dua lapis — hitung JUMLAHNYA sebagai angka (1→3) dan isinya sebagai dua keadaan; jawaban harus lolos keduanya.

**Jebakan:** Menjawab ●●● karena jumlahnya benar tapi isinya tidak dibalik — transformasi balik isi berlaku di kedua pasangan, bukan hanya di A → B.

**10.** Anda sedang mengevaluasi produk seorang vendor untuk pengadaan di unit Anda, dan laporan evaluasi itu harus selesai minggu ini. Sebuah parsel hadiah bernilai besar dari vendor itu tiba di alamat rumah Anda disertai catatan bahwa hadiah itu sekadar tanda terima kasih. Atasan Anda sedang berada di luar kota sampai akhir minggu. Sikap Anda adalah…

A. Menyimpan parsel itu sementara dan melanjutkan evaluasi seperti biasa, karena hadiah itu sekadar tanda terima kasih. *(skor 1)*
B. Mengembalikan parsel itu kepada vendor lewat kurir dan melanjutkan evaluasi seperti biasa sambil menunggu atasan kembali. *(skor 3)*
C. Mengembalikan parsel itu kepada vendor dan memberitahu atasan soal kiriman itu serta mencatatnya dalam laporan evaluasi. *(skor 5)*
D. Memberitahu atasan tentang kiriman itu dan segera meminta arahan beliau sebelum memutuskan nasib parsel itu minggu ini. *(skor 4)*
E. Menyimpan parsel itu di kantor dan baru melaporkannya kepada atasan setelah laporan evaluasi selesai minggu ini. *(skor 2)*

**Kunci: C.** (1) C skor 5 karena aktif mengembalikan parsel, konkret memberitahu atasan, prosedural lewat pencatatan dalam laporan evaluasi, dan melibatkan pihak yang tepat sebelum laporan selesai minggu ini. (2) Skor tiap opsi: A=1 (parsel gratifikasi disimpan dan evaluasi dilanjutkan seolah tidak terjadi apa-apa), B=3 (parsel dikembalikan sehingga konflik kepentingan hilang, tetapi upaya gratifikasi itu disembunyikan sehingga vendor bisa mencoba lagi), C=5 (lengkap), D=4 (melaporkan dan meminta arahan dengan benar, tetapi parsel belum dikembalikan dan belum ada catatan dalam laporan), E=2 (parsel diamankan di kantor, tetapi laporan kepada atasan ditunda sampai evaluasi selesai — selama evaluasi berjalan, penilai masih memegang hadiah vendor). (3) Trik: gratifikasi menjelang tenggat dijawab dengan mengembalikan + memberitahu atasan + mencatat dalam dokumen resmi — mengembalikan saja dan melompati pencatatan resmi belum cukup.

**Jebakan:** D terdengar paling hati-hati karena atasan dilibatkan sebelum keputusan — padahal parsel yang masih berada di tangan Anda selama evaluasi berjalan tetap menjadi celah integritas, dan belum ada catatan resminya.

---

## Soal — Bagian B: SKB Ringan — Normalisasi Database (Soal 11–15)

**11.** Sebuah tabel Anggota menyimpan kolom Hobi dengan isi 'Membaca, Memancing' dalam satu sel untuk satu anggota. Kondisi ini melanggar bentuk normal …

A. 3NF — karena ada dependensi transitif
B. 1NF — karena nilai sel tidak atomik
C. 2NF — karena ada dependensi parsial
D. BCNF — karena determinan bukan candidate key
E. 4NF — karena ada dependensi multivalued

**Kunci: B.** (1) B karena 1NF mensyaratkan tiap sel bernilai atomik — satu nilai saja; sel berisi dua hobi sekaligus berarti nilainya tidak atomik. (2) Langkah: 1. Periksa apakah tiap sel hanya berisi satu nilai. 2. 'Membaca, Memancing' adalah dua nilai dalam satu sel. 3. Itu pelanggaran 1NF, bentuk paling dasar. (3) Trik: bila soal menyebut satu sel berisi daftar dipisah koma, jawabannya hampir selalu 1NF — periksa bentuk paling dasar dulu sebelum naik ke 2NF/3NF.

**Jebakan:** Opsi C (2NF) menggoda karena sama-sama soal dependensi, tetapi 2NF baru relevan bila kunci primernya gabungan dan ada dependensi parsial — soal ini bahkan belum lolos 1NF.

**12.** Tabel Nilai (NIM, KodeMK, NamaMahasiswa, Nilai) dengan kunci primer gabungan (NIM, KodeMK). Kolom NamaMahasiswa hanya bergantung pada NIM, bukan pada seluruh kunci. Untuk mencapai 2NF, langkah yang benar adalah …

A. Menghapus kolom NamaMahasiswa dari tabel.
B. Menjadikan NamaMahasiswa sebagai kunci primer baru.
C. Memindahkan kolom Nilai ke tabel terpisah.
D. Memisahkan NamaMahasiswa ke tabel Mahasiswa dengan kunci NIM.
E. Menambahkan kolom baru KodeJurusan ke tabel Nilai.

**Kunci: D.** (1) D karena NamaMahasiswa bergantung parsial — hanya pada sebagian kunci (NIM); cara memperbaikinya adalah memisahkan atribut itu ke tabel sendiri dengan determinannya sebagai kunci. (2) Langkah: 1. Kenali dependensi parsialnya: NamaMahasiswa ← NIM saja. 2. Pisahkan: tabel Mahasiswa (NIM, NamaMahasiswa). 3. Tabel Nilai tinggal (NIM, KodeMK, Nilai) dengan kunci asing NIM. (3) Trik: dependensi parsial selalu diperbaiki dengan memisahkan atributnya bersama determinannya — bukan dengan menghapus atributnya.

**Jebakan:** Opsi A (menghapus kolom) menggoda karena menghilangkan masalahnya, tetapi data nama mahasiswa adalah data yang harus disimpan — normalisasi memindahkan data, bukan membuangnya.

**13.** Tabel Pegawai (NIP, Nama, KodeDept, NamaDept) dengan NIP sebagai kunci primer. NamaDept bergantung pada KodeDept, dan KodeDept bergantung pada NIP. Kondisi ini melanggar …

A. 3NF — karena ada dependensi transitif
B. 1NF — karena nilai tidak atomik
C. 2NF — karena ada dependensi parsial pada kunci gabungan
D. 4NF — karena ada dependensi multivalued antar atribut
E. Tidak melanggar bentuk normal apa pun

**Kunci: A.** (1) A karena rantainya NIP → KodeDept → NamaDept: NamaDept bergantung pada NIP secara tidak langsung, lewat atribut non-kunci lain (KodeDept) — itulah dependensi transitif yang dilarang 3NF. (2) Langkah: 1. Tulis rantainya: NIP menentukan KodeDept, KodeDept menentukan NamaDept. 2. NamaDept bergantung transitif pada kunci. 3. Perbaiki dengan memisah tabel Departemen (KodeDept, NamaDept). (3) Trik: bila ada rantai tiga atribut non-kunci yang saling menentukan, curigai 3NF — dan ingat, kunci primer tunggal otomatis lolos 2NF.

**Jebakan:** Opsi C (2NF) menggoda karena sama-sama soal dependensi, tetapi dependensi parsial hanya mungkin bila kunci primernya gabungan — di sini kuncinya tunggal (NIP), jadi 2NF sudah lolos.

**14.** Sebuah tabel Kursus menyimpan data dosen dan mata kuliah dalam satu tabel. Ketika satu-satunya mata kuliah yang diajar seorang dosen dihapus, data dosen itu ikut hilang dari tabel. Masalah ini disebut …

A. Anomali penyisipan
B. Anomali pembaruan
C. Redundansi kunci primer
D. Dependensi fungsional penuh
E. Anomali penghapusan

**Kunci: E.** (1) E karena fakta yang tidak berhubungan (data dosen) ikut hilang saat baris yang memuatnya dihapus — itulah anomali penghapusan (deletion anomaly). (2) Langkah: 1. Tanyakan: fakta apa yang hilang? Data dosen. 2. Kenapa hilang? Karena data itu hanya tersimpan di baris mata kuliah yang dihapus. 3. Itu definisi anomali penghapusan. (3) Trik: hafalkan ketiganya dari kata kerjanya — sisip = tidak bisa menambah, ubah = harus ubah berkali-kali, hapus = fakta lain ikut hilang.

**Jebakan:** Opsi A (anomali penyisipan) menggoda karena sama-sama anomali, tetapi penyisipan berarti tidak bisa MENAMBAH data baru (misal dosen tanpa mata kuliah), bukan kehilangan data saat menghapus.

**15.** Suatu relasi dikatakan berada dalam Boyce-Codd Normal Form (BCNF) jika …

A. Semua nilai atributnya atomik dan tidak ada dependensi transitif.
B. Tidak ada dependensi parsial terhadap kunci primer gabungan.
C. Setiap determinan dalam relasi itu merupakan candidate key.
D. Relasi itu tidak memiliki kunci primer gabungan.
E. Semua atribut non-kunci bergantung penuh pada kunci primer.

**Kunci: C.** (1) C karena definisi BCNF: setiap determinan harus merupakan candidate key — lebih ketat dari 3NF yang hanya melarang dependensi transitif dari atribut non-kunci. (2) Langkah: 1. Ingat hierarkinya: 1NF → 2NF → 3NF → BCNF, tiap tingkat lebih ketat. 2. BCNF menambah satu syarat di atas 3NF: determinannya harus candidate key. 3. Opsi A adalah definisi 3NF, B adalah 2NF. (3) Trik: bila opsi menyebut 'determinan' dan 'candidate key' dalam satu kalimat, itu hampir pasti BCNF.

**Jebakan:** Opsi A menggoda karena benar sebagai syarat 3NF — tetapi BCNF menuntut satu syarat tambahan di atas 3NF, dan opsi A tidak menyebutnya.

---

## Soal — Bagian C: Ulangan Variasi Buku Kesalahan (Soal 16–20)

*Variasi baru dari soal simulasi yang salah — skenario, angka, dan nama berbeda; pola yang diuji sama.*

**16.** Warga desa bermusyawarah untuk menentukan prioritas pembangunan jalan desa, dan keputusan diambil bersama setelah mendengar semua pendapat. Perilaku ini merupakan pengamalan Pancasila sila …

A. Pertama
B. Kedua
C. Ketiga
D. Keempat
E. Kelima

**Kunci: D.** (1) D karena musyawarah untuk mufakat adalah pengamalan sila keempat, Kerakyatan yang Dipimpin oleh Hikmat Kebijaksanaan dalam Permusyawaratan/Perwakilan. (2) Langkah: 1. Cari kata kunci perilaku: musyawarah, keputusan bersama, mendengar semua pendapat. 2. Itu ciri sila keempat. 3. Coret sila lain yang temanya dekat. (3) Trik: 'musyawarah' dan 'mufakat' adalah kata kunci yang hampir selalu menunjuk sila keempat.

**Jebakan:** Opsi C (sila ketiga) menggoda karena warga berkumpul bersama terasa seperti persatuan — tetapi penekanan soal ini adalah CARA mengambil keputusan (musyawarah), ranah sila keempat.

**17.** Enam orang duduk melingkar menghadap ke pusat: Rina, Sinta, Tono, Udin, Vina, dan Wawan. Rina duduk berhadapan dengan Tono. Sinta duduk tepat di sebelah Rina searah jarum jam. Wawan duduk berhadapan dengan Sinta. Vina duduk berhadapan dengan Udin. Siapa yang duduk tepat di sebelah kiri Tono?

A. Rina
B. Wawan
C. Sinta
D. Vina
E. Udin

**Kunci: B.** (1) B karena penomorannya: Rina di posisi 1, Tono berhadapan di posisi 4, Sinta di posisi 2 (searah jarum jam dari Rina), Wawan berhadapan dengan Sinta di posisi 5, sisa posisi 3 dan 6 untuk Vina dan Udin yang berhadapan; kiri Tono (yang menghadap pusat) adalah searah jarum jam, yaitu posisi 5 = Wawan. (2) Langkah: 1. Nomori posisi 1–6 searah jarum jam. 2. Letakkan pasangan berhadapan dulu (selisih 3 posisi). 3. Kiri orang yang menghadap pusat = searah jarum jam. (3) Trik: gambar lingkaran dulu — jangan menebak posisi tanpa menggambar; arah 'kiri' orang yang menghadap pusat adalah searah jarum jam, bukan sebaliknya.

**Jebakan:** Soal panjang — latih tandai & lewati. Jangan membalik arah kiri: dari sudut pandang Tono yang menghadap pusat, kirinya adalah posisi searah jarum jam darinya.

**18.** Semua karyawan divisi Pemasaran memakai seragam batik setiap hari Jumat. Sebagian karyawan yang memakai seragam batik adalah anggota koperasi. Berdasarkan kedua pernyataan itu, kesimpulan manakah yang PALING TEPAT?

A. Sebagian karyawan divisi Pemasaran adalah anggota koperasi.
B. Semua anggota koperasi memakai seragam batik.
C. Semua karyawan divisi Pemasaran adalah anggota koperasi.
D. Sebagian anggota koperasi adalah karyawan divisi Pemasaran.
E. Tidak dapat disimpulkan.

**Kunci: E.** (1) E karena 'sebagian' di TENGAH rantai memutus kesimpulan: irisan pada premis 2 bisa saja seluruhnya berasal dari luar divisi Pemasaran. (2) Langkah: 1. Tulis dengan simbol: P = karyawan divisi Pemasaran, B = memakai seragam batik, K = anggota koperasi. Premis 1: (P ⊆ B). Premis 2: sebagian karyawan yang memakai seragam batik adalah anggota koperasi (B ∩ K ≠ ∅). 2. Irisan (B ∩ K) pada premis 2 bisa saja SELURUHNYA karyawan berseragam dari divisi lain — premis tidak memberi informasi apakah irisan itu menyentuh P. 3. Karena (P ∩ K) tidak dijamin ada, tidak ada kesimpulan sah tentang hubungan divisi Pemasaran dan keanggotaan koperasi. 4. Opsi A dan D sama-sama mengklaim irisan P–K yang tidak dijamin itu, hanya dibalik arahnya. (3) Trik: 'sebagian' di tengah rantai = rantai putus untuk kelompok di ujungnya — bandingkan dengan 'sebagian' di AWAL rantai yang tetap sah.

**Jebakan:** Opsi A menggoda karena 'sebagian' terasa aman, padahal subset anggota koperasi di antara pemakai seragam belum tentu mencakup satu pun karyawan Pemasaran.

**19.** Perhatikan tabel penjualan empat toko (dalam juta rupiah) berikut.

| Toko | Penjualan |
| A | 120 |
| B | 135 |
| C | 150 |
| D | 115 |

Selisih antara penjualan tertinggi dan terendah adalah …

A. 35 juta
B. 30 juta
C. 25 juta
D. 40 juta
E. 20 juta

**Kunci: A.** (1) A karena tertinggi = 150 (Toko C), terendah = 115 (Toko D), selisih = 150 − 115 = 35. (2) Langkah: 1. Cari nilai terbesar dan terkecil di tabel. 2. Kurangkan: terbesar − terkecil. 3. Jangan mencampur kolom lain. (3) Trik: soal 'selisih tertinggi–terendah' hanya butuh dua angka ekstrem — jangan menghitung rata-rata atau total dulu.

**Jebakan:** Opsi B (30 juta) muncul bila memakai 150 − 120 — tertukar antara nilai terendah (115) dan nilai pertama yang dibaca (120).

**20.** Perhatikan matriks 3×3 berikut. Bentuk yang tepat untuk mengisi kotak bertanda ? adalah…


*●◆ | ◆■ | ●■
■● | ●◆ | ■◆
◆● | ●■ | ?*

A. ●◆
B. ■●
C. ◆■
D. ●■
E. ◆●

**Kunci: C.** (1) C karena per baris berlaku XOR: bentuk yang muncul di kedua kotak pertama dihapus, sisanya dipertahankan; baris 3: ◆● dan ●■ — ● muncul dua kali (dihapus), tersisa ◆■. (2) Langkah: 1. Uji baris 1: ●◆ dan ◆■ → ◆ terhapus, tersisa ●■, cocok. 2. Uji baris 2: ■● dan ●◆ → ● terhapus, tersisa ■◆, cocok. 3. Terapkan ke baris 3. (3) Trik: pada matriks XOR, hitung kemunculan tiap bentuk per baris — muncul 2 kali berarti hilang, muncul 1 kali berarti lolos ke kotak ketiga.

**Jebakan:** Menjawab ●■ karena menggabungkan kedua kotak tanpa menghapus bentuk ganda — bentuk yang muncul dua kali justru dihapus, bukan dipertahankan.

---

## Setelah mengerjakan

- **Skor sesi ini:** Review ___ /10 benar · SKB ___ /5 benar · Ulangan ___ /5 benar. Target: review ≥8/10, SKB ≥4/5, ulangan 5/5.
- **Buku kesalahan:** soal yang salah diulang **Rabu, 25 Nov 2026** (3 hari kemudian).
- **Besok (Senin, 23 Nov):** TWK — 1 topik + soal (lanjutan rotasi).
- Distribusi kunci terverifikasi sebelum penerbitan: A4/B4/C5/D3/E4 (maks 20% per posisi). Semua kunci dihitung/diverifikasi ulang dari nol oleh Mommy sebelum diterbitkan. Korelasi panjang opsi–skor TKP: r = 0,00 (batas standar 0,35) — opsi skor-5 bukan yang terpanjang.
