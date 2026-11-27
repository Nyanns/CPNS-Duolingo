# Latihan CPNS Hari 9 — Minggu, 15 November 2026
**Fokus: Review mingguan + SKB ringan (Subnetting) + ulangan buku kesalahan · 21 soal (Review 10 + SKB 5 + Ulangan 6) · Target: review ≥8/10, SKB ≥4/5, ulangan 6/6 · Waktu soal: ~45 menit, total sesi ~2 jam termasuk pelajaran & koreksi**

*Sesuai rotasi mingguan: Minggu = review mingguan + SKB ringan. Semua soal di bawah ini BARU — tidak satu pun mengulang soal Hari 1–8 maupun simulasi 14 Nov. Soal dibuat dari pola yang sama dengan soal SKD 2023–2024 (bukan soal resmi BKN — BKN tidak mempublikasikan soal SKD). Kerjakan di aplikasi (klik), bukan lewat chat.*

---

## ⚠️ Status sebelum mulai — baca dulu

- **Simulasi penuh Sabtu 14 Nov BELUM dikerjakan.** Sesi 110 soal / 100 menit masih live di aplikasi (slug `simulasi-penuh-2026-11-14`) — kerjakan hari ini atau jadwalkan ulang secepatnya, karena inilah satu-satunya ukuran jujur kesiapanmu sebelum pengumuman formasi ~20 Nov.
- **Streak kembali 0** (terakhir latihan Kamis 12 Nov; Jumat istirahat, Sabtu simulasi tidak jalan). Satu sesi hari ini langsung menghidupkannya lagi — freeze 1 masih tersedia.
- **Masih menunggu jawaban:** Hari 1, Hari 2b, dan Hari 8 (figural). Hari 8 tetap bisa dikerjakan kapan saja di aplikasi.
- **Buku kesalahan jatuh tempo hari ini (2 item):** Hari 6 (deret kuadrat−1, soal cerita) + Hari 7 (TKP ketegasan prosedural) — keduanya diulang di Bagian C sesi ini sebagai soal variasi baru.

---

## Pelajaran fundamental 1: kilas balik minggu ini (7 pola yang harus sudah otomatis)

| Pola | Aturan satu baris | Bukti kamu sudah bisa |
|---|---|---|
| Implementasi pasal UUD 1945 dalam kasus | Cari **kata kerja + subjek** di soal, cocokkan ke pasal — bukan hafal nomornya | Hari 4: 27/30; ulangan 3/3 lunas |
| Silogisme "sebagian" | "Sebagian" di tengah rantai = **rantai putus**; "sebagian" = "ada yang", jadi dari "semua" boleh ditarik "sebagian" | Hari 5: 28/30 (2 salah karena refleks "tidak dapat disimpulkan" over-firing) |
| Deret dua operasi | Cek selisih dulu; kalau selisihnya berpola, itu **dua lapis**; kalau tidak, coba ×/÷ +/− | Hari 6: deret 13/15 |
| Soal cerita → persamaan | **Terjemah dulu ke persamaan, baru hitung**; cek satuan waktu sebelum menghitung | Hari 6: 3 soal cerita salah karena ini |
| TKP ketegasan prosedural | Saat aturan dilanggar: **tolak/ingatkan tegas dulu, baru tawarkan jalur resmi** — diplomasi lunak bukan jawaban 5 poin | Hari 7: No. 22 & 28 (keduanya 3 poin) |
| Figural 9 kotak | Cari perubahan **satu elemen** per baris/kolom; uji XOR (yang sama di dua gambar, hilang di gambar ketiga) | Hari 8: belum dikerjakan — figural masih dingin |
| Analogi 3 kata | Relasi harus cocok di **ketiga** unsur (mis. profesi : tempat : aktivitas) | Hari 5: analogi 16 soal, hampir sempurna |

**Pemanasan 60 detik sebelum mulai:** tulis dari ingatan — *6 = syarat calon Presiden; 6A = cara memilih · 21 = DPR mengajukan RUU; 22 = Perppu · 24A = MA menguji peraturan di bawah UU; 24C = MK menguji UU terhadap UUD* — lalu kerjakan Bagian A sebagai ceknya.

---

## Pelajaran fundamental 2: SKB ringan — Subnetting (jaringan komputer)

*Topik SKB #2 untuk Pranata Komputer. Menjawab juga soal tes SKB yang dulu belum terjawab: "/26 = berapa host usable?"*

### 1. Tiga angka yang harus hafal

| Prefix | Total alamat | Host usable | Dipakai untuk |
|---|---|---|---|
| /24 | 256 | 254 | Satu jaringan kantor kecil |
| /25 | 128 | 126 | Dua segmen dari /24 |
| /26 | 64 | **62** | Subnet 60-an host |
| /27 | 32 | 30 | Subnet 30-an host |
| /28 | 16 | 14 | Subnet kecil (printer, CCTV) |
| /29 | 8 | 6 | Link point-to-point |
| /30 | 4 | 2 | Link antar-router |

### 2. Rumus — dan kenapa dikurangi 2

Jumlah host usable = **2^(32 − prefix) − 2**. Dua alamat yang tidak bisa dipakai: **network address** (semua bit host 0 — alamat jaringannya sendiri) dan **broadcast address** (semua bit host 1 — alamat untuk menyapa semua host). Contoh /26: 2^6 = 64, dikurangi 2 = **62**.

### 3. Cara cepat membagi subnet

- Satu bit pinjaman = jumlah subnet **×2**, ukuran tiap subnet **÷2**. /24 → /25 = 2 subnet × 126 host; /24 → /26 = 4 subnet × 62 host; /24 → /27 = 8 subnet × 30 host.
- **Alamat broadcast** suatu subnet = satu alamat sebelum network address subnet berikutnya. Contoh: 192.168.1.0/25 membelah .0–.127 dan .128–.255 → broadcast subnet pertama **.127**, network subnet kedua **.128**.
- **Pilih prefix paling efisien:** cari prefix terkecil yang host usable-nya ≥ kebutuhan. Butuh 100 host → /26 (62) tidak cukup → **/25 (126)**. Jangan boros ambil /24 kalau /25 cukup — alamat IP kantor itu terbatas.

### 4. Jebakan yang sering keluar

- Menjawab **64** untuk /26 (lupa mengurangi network + broadcast) — jawaban pengecoh paling klasik.
- Mengira /25 pertama berakhir di .128 — padahal .128 adalah network address subnet kedua; broadcast-nya .127.
- Menukar "jumlah subnet" dengan "jumlah host": /24 → /27 menghasilkan **8 subnet**, masing-masing **30 host** — dua angka yang berbeda.

---

## Soal — Bagian A: Review mingguan (10 soal baru)

**1. (TWK — implementasi pasal dalam kasus)** Pemerintah daerah menetapkan sebuah peraturan daerah yang isinya bertentangan dengan undang-undang. Lembaga negara yang berwenang menguji peraturan di bawah undang-undang terhadap undang-undang adalah…
A. Mahkamah Konstitusi
B. Komisi Yudisial
C. Dewan Perwakilan Rakyat
D. Mahkamah Agung

**2. (TWK — Bahasa Indonesia)** Bacalah teks berikut: *"Digitalisasi pelayanan publik bukan sekadar memindahkan antrean ke layar ponsel. Keberhasilannya ditentukan oleh kesiapan infrastruktur, literasi digital warga, dan kemauan birokrasi mengubah proses kerja — bukan hanya membeli aplikasi baru. Tanpa ketiganya, layanan digital hanya memindahkan antrean lama ke tempat baru."* Ide pokok teks tersebut adalah…
A. Layanan digital hanya memindahkan antrean warga dari loket fisik ke layar ponsel mereka masing-masing
B. Membeli aplikasi baru adalah langkah utama dalam digitalisasi pelayanan publik di daerah
C. Keberhasilan digitalisasi ditentukan infrastruktur dan literasi warga serta perubahan proses kerja
D. Warga harus mempelajari layanan digital agar antrean panjang di loket fisik cepat berkurang
E. Digitalisasi berhasil bila warga bersedia mengantre lewat ponsel dan bukan lagi di loket fisik

**3. (TIU verbal — analogi 3 kata)** GURU : SEKOLAH : MENGAJAR = …
A. KOKI : RESTORAN : MEMASAK
B. SOPIR : MOBIL : MENGEMUDI
C. PETANI : PADI : MENANAM
D. PELUKIS : KANVAS : MELUKIS

**4. (TIU verbal — silogisme rantai panjang)** Semua mahasiswa yang lulus ujian praktik wajib mengikuti magang. Sebagian mahasiswa yang mengikuti magang ditempatkan di luar kota. Rina lulus ujian praktik. Kesimpulan yang tepat adalah…
A. Rina ditempatkan di luar kota
B. Semua mahasiswa yang magang ditempatkan di luar kota
C. Tidak dapat disimpulkan
D. Rina wajib mengikuti magang

**5. (TIU verbal — silogisme "tidak ada")** Tidak ada anggota dewan yang boleh menerima hadiah dari kontraktor. Semua anggota panitia pengadaan adalah anggota dewan. Kesimpulan yang tepat adalah…
A. Sebagian anggota panitia pengadaan boleh menerima hadiah dari kontraktor
B. Tidak ada anggota panitia pengadaan yang boleh menerima hadiah dari kontraktor
C. Semua kontraktor adalah anggota dewan
D. Tidak dapat disimpulkan

**6. (TIU numerik — deret dua operasi)** 2, 5, 14, 41, 122, …
A. 245
B. 364
C. 365
D. 366

**7. (TIU numerik — analisis tabel)** Penjualan (dalam unit) empat toko selama tiga bulan:

| Toko | Jan | Feb | Mar |
|---|---|---|---|
| A | 120 | 140 | 160 |
| B | 150 | 130 | 170 |
| C | 180 | 110 | 150 |
| D | 90 | 200 | 140 |

Selisih total penjualan Toko B dan Toko D selama tiga bulan adalah… unit.
A. 20
B. 10
C. 30
D. 40

**8. (TIU numerik — soal cerita multi-langkah)** Seorang pedagang membeli 40 kg beras seharga Rp12.000 per kg. Ia menjual 25 kg dengan harga Rp14.000 per kg dan sisanya dengan harga Rp13.000 per kg. Keuntungan total pedagang itu adalah…
A. Rp55.000
B. Rp75.000
C. Rp45.000
D. Rp65.000

**9. (TIU figural — matriks 9 kotak)** Dalam matriks 3×3, tiap baris mengikuti aturan: gambar ketiga adalah gabungan dua gambar pertama, tetapi bagian yang sama di kedua gambar dihapus. Baris 1: ○, △, ○△. Baris 2: □, ○, □○. Baris 3: △, □, … Gambar yang tepat mengisi tanda tanya adalah…
A. ○△
B. △□
C. □○
D. △○

**10. (TIU figural — serial gambar)** Sebuah panah berputar 90° searah jarum jam pada tiap langkah, dan jumlah titik di sampingnya bertambah satu tiap langkah. Gambar 1: panah ke atas + 1 titik. Gambar 2: panah ke kanan + 2 titik. Gambar 3: panah ke bawah + 3 titik. Gambar 4: panah ke kiri + 4 titik. Gambar 5 adalah…
A. Panah ke kanan + 5 titik
B. Panah ke atas + 4 titik
C. Panah ke atas + 5 titik
D. Panah ke bawah + 5 titik

---

## Soal — Bagian B: SKB ringan — Subnetting (5 soal baru)

**11.** Sebuah jaringan memakai subnet mask /26. Berapa jumlah host yang dapat dipakai (usable) dalam jaringan itu?
A. 64
B. 30
C. 126
D. 62

**12.** Sebuah kantor membutuhkan 100 host dalam satu subnet. Prefix CIDR yang paling efisien untuk kebutuhan itu adalah…
A. /25
B. /24
C. /26
D. /27

**13.** Alamat jaringan 192.168.1.0/25 dibagi menjadi dua subnet. Alamat broadcast subnet pertama adalah…
A. 192.168.1.128
B. 192.168.1.127
C. 192.168.1.255
D. 192.168.1.0

**14.** Berapa jumlah subnet yang terbentuk bila jaringan 192.168.0.0/24 dipecah menjadi subnet-subnet /27?
A. 4
B. 6
C. 16
D. 8

**15.** Sebuah printer jaringan diberi alamat 10.0.0.5/28. Berapa host usable dalam subnet printer itu?
A. 16
B. 30
C. 14
D. 12

---

## Soal — Bagian C: Ulangan buku kesalahan (6 soal variasi baru)

*Soal 16–17 mengulang pola salah Hari 7 (TKP ketegasan prosedural). Soal 18–21 mengulang pola salah Hari 6 (deret kuadrat−1, soal cerita pekerja-hari, rata-rata gabungan, jumlah–selisih). Skenario dan angkanya BARU — yang diuji polanya, bukan hafalan jawabannya.*

**16. (Ulangan buku kesalahan — TKP integritas)** Anda duduk di panitia seleksi beasiswa pelatihan yang akan mengumumkan hasilnya besok pagi. Seorang rekan dekat meminta Anda memberitahukan skor wawancara seorang kandidat lain agar ia bisa memperkirakan peluangnya, dan ia berjanji merahasiakan informasi itu. Anda memegang daftar skor yang belum boleh disebarkan. Sikap Anda adalah…
A. Memberitahukan skor kandidat itu secara lisan, karena informasi lisan lebih sulit dilacak daripada dokumen tertulis.
B. Menolak memberitahukan skor itu dan mengarahkan rekan itu menunggu pengumuman resmi besok pagi di kantor.
C. Memberitahukan kisaran skor kandidat itu secara umum, agar rekan itu mendapat gambaran peluangnya sebelum pengumuman.
D. Menolak memberitahukan skor itu dan mengarahkan rekan menunggu pengumuman serta mencatat permintaan itu untuk panitia.
E. Mengalihkan rekan itu dengan menjelaskan kriteria penilaian secara umum yang sudah dipublikasikan panitia secara resmi.

**17. (Ulangan buku kesalahan — TKP profesionalisme)** Anda menjadi panitia upacara bendera Hari Kemerdekaan yang akan digelar besok pagi di kantor. Seorang rekan menyatakan ia enggan ikut serta dan mengajak rekan lain absen dari upacara itu, dengan alasan upacara bukan pekerjaan yang sesungguhnya. Sikap Anda adalah…
A. Menjelaskan kewajiban upacara bendera bagi ASN dan mengajak rekan hadir serta melaporkan ajakannya bila berlanjut.
B. Menjelaskan bahwa upacara bendera adalah kewajiban ASN dan mengajak rekan itu hadir bersama seluruh tim besok pagi.
C. Membiarkan rekan itu absen dari upacara karena keikutsertaan upacara adalah pilihan pribadi setiap pegawai di kantor.
D. Mengajak rekan itu berdiskusi panjang tentang makna upacara bendera agar ia memahami nilai kebangsaan di baliknya.
E. Mengabaikan ajakan rekan itu dan berharap rekan lain tetap hadir besok atas kemauan mereka sendiri di kantor.

**18. (Ulangan Hari 6 No. 15 — deret)** 3, 8, 15, 24, 35, …
A. 46
B. 47
C. 49
D. 48

**19. (Ulangan Hari 6 No. 17 — soal cerita pekerja-hari)** 18 pekerja menyelesaikan sebuah proyek dalam 12 hari. Jika jumlah pekerja ditambah menjadi 24 orang dengan kecepatan kerja yang sama, proyek itu selesai dalam… hari.
A. 9
B. 8
C. 10
D. 11

**20. (Ulangan Hari 6 No. 18 — soal cerita rata-rata)** Rata-rata nilai 6 siswa adalah 82. Setelah 4 siswa lain bergabung, rata-rata 10 siswa menjadi 79. Berapa jumlah total nilai 4 siswa yang bergabung itu?
A. 288
B. 308
C. 298
D. 318

**21. (Ulangan Hari 6 No. 26 — soal cerita jumlah–selisih)** Jumlah dua bilangan adalah 84 dan selisihnya 16. Bilangan yang lebih kecil adalah…
A. 32
B. 34
C. 36
D. 50

---

## Kunci jawaban + pembahasan

### Bagian A — Review

**1. D — Mahkamah Agung (Pasal 24A ayat 1).** MA berwenang menguji peraturan perundang-undangan di bawah UU terhadap UU. Jebakan: MK (A) menguji UU terhadap UUD — arahnya berlawanan. Ingat: "MA = peraturan DI BAWAH UU, MK = UU terhadap UUD."

**2. C.** Ide pokok = kalimat yang merangkum seluruh isi teks: keberhasilan digitalisasi ditentukan tiga hal sekaligus — infrastruktur, literasi warga, dan perubahan proses kerja. A terlalu sempit (hanya memindahkan antrean — justru yang dikritik teks), B bertentangan dengan teks (membeli aplikasi disebut bukan langkah utama), D hanya satu penentu (literasi saja tidak cukup), E mengantre lewat ponsel tetap antrean lama di tempat baru. Jebakan: B terdengar masuk akal karena membeli aplikasi memang bagian dari digitalisasi — padahal teks menegaskan aplikasi baru saja tidak cukup tanpa ketiga penentu itu.

**3. A — KOKI : RESTORAN : MEMASAK.** Relasi soal: profesi : tempat kerja : aktivitas khas. Hanya A yang cocok di ketiga unsur. B: mobil adalah alat, bukan tempat kerja. C: padi adalah hasil, bukan tempat. D: kanvas adalah media, bukan tempat kerja.

**4. D — Rina wajib mengikuti magang.** Premis 1 ("semua yang lulus wajib magang") + Rina lulus → Rina wajib magang, rantai tersambung penuh. A salah: "sebagian" di premis 2 memutus rantai ke penempatan luar kota — tidak bisa disimpulkan Rina termasuk sebagian itu. C salah: ada kesimpulan valid (D), jadi "tidak dapat disimpulkan" tidak berlaku. Ini persis jebakan Hari 5 No. 20 & 29 — jangan over-firing D.

**5. B.** "Tidak ada anggota dewan yang boleh menerima hadiah" + "semua panitia adalah anggota dewan" → tidak ada anggota panitia yang boleh menerima hadiah. Kuantor "tidak ada" merambat ke bawah lewat "semua". A dan C membalik arah rantai; D salah karena kesimpulan valid tersedia.

**6. C — 365.** Pola ×3−1: 2×3−1=5, 5×3−1=14, 14×3−1=41, 41×3−1=122, 122×3−1=**365**. Selisihnya (+3, +9, +27, +81) dikali 3 tiap langkah — tanda pola perkalian, bukan penjumlahan tetap. Jebakan: B (364) muncul bila menghitung 122×3−2; D (366) bila lupa mengurangi 1; A (245) memakai pola ×2+1 yang hanya cocok di suku pertama (2×2+1=5) tetapi gagal di suku kedua (5×2+1=11, bukan 14) — selalu uji pola ke SEMUA suku sebelum memilih.

**7. A — 20.** Total B = 150+130+170 = 450. Total D = 90+200+140 = 430. Selisih = 450−430 = **20**. Jebakan: tergoda membandingkan satu bulan saja (Feb: D 200 vs B 130) — soal meminta total tiga bulan.

**8. D — Rp65.000.** Modal: 40×12.000 = 480.000. Penjualan: 25×14.000 = 350.000; sisa 15 kg ×13.000 = 195.000; total 545.000. Untung = 545.000−480.000 = **65.000**. Jebakan: lupa menghitung sisa 15 kg (40−25) atau memakai harga yang sama untuk semua.

**9. B — △□.** Aturan XOR: gabungan dua gambar, bagian yang sama dihapus. Baris 3: △ + □, tidak ada yang sama → gabungan △□. Jebakan: A dan D memasukkan ○ yang tidak ada di baris 3; C urutannya benar tapi isinya salah (□○ bukan △□).

**10. C — Panah ke atas + 5 titik.** Putaran: atas → kanan → bawah → kiri → **atas** (satu putaran penuh). Titik: 1, 2, 3, 4 → **5**. Jebakan: B memakai jumlah titik gambar 4 (4) — titik bertambah tiap langkah, jadi gambar 5 = 5 titik.

### Bagian B — SKB Subnetting

**11. D — 62.** /26 → 2^(32−26) = 2^6 = 64 alamat, dikurangi network + broadcast = **62** usable. Jebakan: A (64) lupa mengurangi 2 — ini sekaligus menjawab soal tes SKB "/26 = berapa host usable?".

**12. A — /25.** /26 hanya 62 host (tidak cukup), /25 = 126 host (cukup, paling efisien), /24 = 254 (boros). Aturan: pilih prefix terkecil yang host usable-nya ≥ kebutuhan.

**13. B — 192.168.1.127.** /25 membelah .0–.127 dan .128–.255. Broadcast subnet pertama = alamat terakhir subnet itu = **.127**. Jebakan: A (.128) adalah network address subnet kedua, bukan broadcast subnet pertama.

**14. D — 8.** /24 → /27 meminjam 3 bit → 2^3 = **8 subnet**, masing-masing 30 host usable. Jebakan: C (16) adalah hasil kalau meminjam 4 bit (/28).

**15. C — 14.** /28 → 2^(32−28) = 2^4 = 16 alamat, dikurangi 2 = **14** usable.

### Bagian C — Ulangan buku kesalahan

**16. D (5) — A (1), B (4), C (2), E (3).** Skor wawancara yang belum diumumkan adalah informasi rahasia panitia; janji rekan untuk merahasiakannya tidak mengubah sifat informasi itu. D paling tepat (skor 5): menolak memberitahukan, mengarahkan menunggu pengumuman resmi, dan mencatat permintaan itu untuk panitia — meninggalkan jejak atas upaya kebocoran. B baik tetapi permintaan itu tidak dicatat, sehingga panitia tidak tahu kerahasiaan seleksi sudah diuji (skor 4). E hanya mengalihkan ke kriteria umum tanpa penolakan tegas dan tanpa pencatatan (skor 3). C membocorkan kisaran — tetap membocorkan (skor 2). A paling buruk (skor 1): membocorkan secara lisan justru agar sulit dilacak.
**Jebakan:** B terdengar sempurna karena penolakan dan arahannya benar — padahal permintaan kebocoran yang tidak dicatat membuat panitia tidak tahu bahwa kerahasiaan seleksi sudah diuji.

**17. A (5) — B (4), C (2), D (3), E (1).** Upacara bendera adalah kewajiban ASN; rekan yang enggan hadir dan mengajak rekan lain absen harus ditegakkan kewajibannya, bukan dibiarkan. A paling tepat (skor 5): menjelaskan kewajiban, mengajak hadir, dan melaporkan ajakannya bila berlanjut. B baik tetapi ajakan rekan kepada rekan lain tidak ditindaklanjuti (skor 4). D hanya berdiskusi tentang makna upacara tanpa menegakkan kewajiban dan membiarkan ajakan itu (skor 3). C membiarkan pelanggaran dengan dalih pilihan pribadi (skor 2). E paling buruk (skor 1): pasif, menyerahkan kehadiran rekan lain kepada kemauan mereka sendiri.
**Jebakan:** B terdengar lengkap karena penjelasan dan ajakannya benar — padahal rekan yang terus mengajak rekan lain absen membuat upacara besok tetap terancam sepi.

**18. D — 48.** Pola n²−1: 2²−1=3, 3²−1=8, 4²−1=15, 5²−1=24, 6²−1=35, 7²−1=**48**. Ini pola Hari 6 No. 15 (deret yang sama, angka lanjutannya berbeda). Jebakan: C (49) adalah 7² tanpa dikurangi 1.

**19. A — 9 hari.** Total pekerja-hari = 18×12 = 216. Dengan 24 pekerja: 216÷24 = **9 hari**. Jebakan: B (8) muncul kalau kamu membagi 216 dengan 27; D (11) kalau kamu mengira menambah pekerja hanya mengurangi 1 hari.

**20. C — 298.** Total 6 siswa = 6×82 = 492. Total 10 siswa = 10×79 = 790. Total 4 siswa yang bergabung = 790−492 = **298**. Jebakan Hari 6 No. 18 terulang di sini: jangan rata-ratakan rata-rata (82 dan 79 tidak bisa dirata-rata langsung karena jumlah siswanya berbeda) — selalu lewat total dulu.

**21. B — 34.** Bilangan kecil = (jumlah − selisih) ÷ 2 = (84−16) ÷ 2 = **34**. (Bilangan besar = 50 — itu opsi D, jebakan untuk yang lupa membagi dua atau mengambil yang besar.)

---

## Setelah mengerjakan

- **Skor review (Soal 1–10):** ___ / 10. Target: ≥8. Di bawah 8 → buka kembali pelajaran fundamental 1 dan kerjakan Bank Latihan topik yang salah.
- **Skor SKB (Soal 11–15):** ___ / 5. Target: ≥4. Soal 11 sekaligus menutup soal tes SKB "/26 = 62 host usable" dari 7 Nov.
- **Skor ulangan (Soal 16–21):** ___ / 6. Target: 6/6 — soal yang pernah salah tidak boleh salah dua kali. Kalau No. 16/17 masih di bawah 5 poin, drill lagi rumus jawaban 5 poin TKP (Hari 7) sebelum sesi berikutnya.
- **Distribusi kunci sesi ini (diperiksa sebelum diterbitkan):** A5 / B4 / C5 / D7 — tidak ada posisi di atas 40% (pelajaran cacat Hari 7).
- **Buku kesalahan:** soal yang salah di sesi ini masuk buku kesalahan aplikasi (jadwal FSRS 1–3–7–14–30 hari).
- **Besok (Senin, 16 Nov):** TWK — 1 topik + soal (lanjutan rotasi: TWK narasi panjang + Bahasa Indonesia, atau pasal yang belum keluar).
- **Tertunda — jangan lupa:** simulasi penuh 14 Nov (110 soal / 100 menit) BELUM dikerjakan; Hari 1, 2b, dan 8 juga masih menunggu. Kerjakan simulasi secepatnya — prediksi skor jujur hanya bisa dibuat setelah ada data waktu nyata.
