# Materi SKD — Pack v1 untuk tab "Materi" aplikasi Duolingo CPNS
Disusun 2026-11-13 pagi (WIB) atas permintaan Sandi: "tambahkan page atau button di bawah khusus materi, isinya materi SKD TIU dll, cari materi di internet sampai dalam".
Aturan penulisan (jawaban atas keluhan "tulisan yg komplrk atau banyak"): tiap kartu materi maks 3 poin singkat + 1 contoh cepat + 1 jebakan. Tanpa paragraf panjang. Bahasa Indonesia ringkas.

## Acuan resmi
- KepmenPANRB 321/2024 (bukan "Permen") — kisi-kisi + passing grade SKD 2024, acuan aman sampai kisi-kisi 2026 terbit.
- SKD: 110 soal / 100 menit, CAT BKN, maks 550. TWK 30 soal (PG 65, maks 150), TIU 35 soal (PG 80, maks 175), TKP 45 soal (PG 166, maks 225, skor 1–5 per opsi, kosong = 0). Harus lolos tiap subtes + masuk 3x formasi ke SKB. Target aman Sandi: TWK 90+, TIU 110+, TKP 185+ (total 385).
- Kisi-kisi 2026 belum terbit (per 13 Nov 2026); pendaftaran umum belum dibuka, pengumuman tahapan/formasi ~20 Nov 2026.
- Sumber riset: https://hypeabis.id/read/41542/calon-asn-wajib-tahu-ini-kisi-kisi-soal-tes-skd-cpns-2024 ; https://www.pejuangcpns.com/belajar/pancasila ; https://suratplus.com/blog/kisi-kisi-materi-pancasila-dan-uud-1945-untuk-twk-cpns ; https://note.raisilham.com/TIU ; https://www.relic.id/materi-tiu-cpns-2026-lengkap-dengan-contoh-soal-dan-pembahasannya/ ; https://belajarbro.id/cpns/soal-tkp-skd ; https://lulus-cpns.com/tips-mengerjakan-tes-karakteristik-pribadi/ ; https://daftarsekolah.spmb.teknokrat.ac.id/2026/01/panduan-lengkap-tkp-skd-2025-strategi-kisi-kisi-dan-contoh-soal-terupdate/

## Struktur halaman Materi (untuk builder)
- Akses: tab bawah ke-6 "Materi" (ikon buku) — pertahankan 5 tab lama; kalau 6 tab terlalu padat di HP, gabungkan tab Info CPNS sebagai seksi di dalam halaman Materi. Jangan hapus tab apa pun tanpa kata Sandi.
- Isi: kartu ringkas per topik, bisa dibuka satu-satu (accordion). Tiap kartu: "Inti" 1 baris, "Rumus cepat" ≤3 poin, "Contoh" 1 soal mini, "Jebakan" 1 baris. Di akhir tiap subtes: tombol "Latihan topik ini" (masuk ke bank soal topik itu).
- Maskot Mommy tampil di header halaman Materi sebagai pemandu (lihat brief maskot di bawah).

---

## TWK — Tes Wawasan Kebangsaan (30 soal, PG 65)
### 1. Pancasila
- Inti: rumusan SAH ada di Pembukaan UUD 1945 alinea 4, disahkan PPKI 18 Agu 1945. Bukan rumusan pidato 1 Juni, bukan Piagam Jakarta.
- Rumus cepat: 1 Jun 1945 pidato Soekarno → 22 Jun 1945 Piagam Jakarta → 18 Agu 1945 rumusan sah. Lambang sila: 1 Bintang, 2 Rantai, 3 Pohon Beringin, 4 Kepala Banteng, 5 Padi & Kapas. 45 butir pengamalan (Tap MPR I/2003).
- Contoh: sikap menolong korban bencana tanpa membedakan suku/agama = sila 2.
- Jebakan: soal TWK jarang tanya hafalan sila mentah — yang diuji pengaitan sikap/kasus ke sila & butir pengamalan.
### 2. UUD 1945
- Inti: setelah 4x amandemen (1999–2002): Pembukaan + 21 bab, 73 pasal (sebelumnya 16 bab, 37 pasal).
- Rumus cepat: Pasal 6 = syarat Presiden; 6A = cara memilih Presiden. 21 = DPR ajukan RUU; 22 = Perppu. 24 = kekuasaan kehakiman; 24A = MA; 24C = MK. 1(2) kedaulatan di tangan rakyat. 27(3) bela negara; 28E(1) kebebasan beragama; 29(2) jaminan negara atas kemerdekaan beragama; 31(1) hak pendidikan; 33(3) SDA dikuasai negara untuk kemakmuran rakyat.
- Contoh: cabang produksi penting dikuasai negara = 33(2); kekayaan alam = 33(3).
- Jebakan: pasal "kembar" (6/6A, 21/22, 24/24A) — bedakan SYARAT vs CARA, dan MA vs MK.
### 3. Bhinneka Tunggal Ika
- Inti: "berbeda-beda tetapi tetap satu jua". Dari Kitab Sutasoma, Mpu Tantular, abad XIV, Majapahit. Semboyan resmi 17 Agu 1950 (PP 66/1951), UUD 1945 Pasal 36A.
- Rumus cepat: pengusul ke Soekarno = Muh Yamin. Tertulis di pita Garuda Pancasila.
- Contoh: menghormati adat daerah lain = pengamalan Bhinneka.
- Jebakan: jangan tertukar sumbernya dengan Negarakertagama (itu asal kata "Pancasila", Empu Prapanca).
### 4. NKRI
- Inti: negara kesatuan — kedaulatan di tangan rakyat, bentuk negara tidak bisa diubah (Pasal 37 ayat 5: bentuk NKRI tidak dapat diubah).
- Rumus cepat: 4 pilar kebangsaan = Pancasila, UUD 1945, NKRI, Bhinneka Tunggal Ika.
- Contoh: gerakan separatis = ancaman terhadap NKRI.
- Jebakan: otonomi daerah ≠ federal — daerah otonom tetap dalam NKRI.
### 5. Nasionalisme & Bela Negara
- Inti: nasionalisme = mewujudkan kepentingan nasional dengan tetap menjaga identitas nasional. Bela negara = hak & kewajiban tiap warga (Pasal 27(3), 30(1)).
- Rumus cepat: bela negara bentuknya: cinta tanah air, sadar berbangsa, setia Pancasila, rela berkorban, kemampuan awal bela negara.
- Contoh: ASN netral di Pemilu/Pilkada = nasionalisme + integritas.
- Jebakan: bela negara bukan hanya wajib militer — sikap sehari-hari ikut dihitung.
### 6. Integritas & Netralitas ASN
- Inti: ASN netral dari pengaruh/parpol, tidak berpihak, tidak terlibat politik praktis (UU 20/2023 tentang ASN).
- Rumus cepat: integritas = jujur, tidak KKN, tolak gratifikasi, laporkan pelanggaran.
- Contoh: ASN kampanye untuk calon tertentu = pelanggaran netralitas.
- Jebakan: "netral" bukan "tidak peduli" — ASN tetap wajib melayani semua warga secara adil.
### 7. Bahasa Indonesia
- Inti: bahasa persatuan (Sumpah Pemuda 1928), bahasa negara (Pasal 36 UUD 1945).
- Rumus cepat: ide pokok, kata bercetak miring, sinonim/antonim dalam konteks kalimat.
- Contoh: cari gagasan utama paragraf, bukan detailnya.
- Jebakan: jangan terkecoh kata sulit — jawab dari konteks kalimat, bukan hafalan kamus.

## TIU — Tes Intelegensi Umum (35 soal, PG 80)
### 1. Analogi (verbal)
- Inti: cari hubungan pasangan kata pertama, terapkan ke pasangan kedua.
- Rumus cepat: hubungan umum = alat–profesi (stetoskop:dokter), sebab–akibat, bagian–keseluruhan, sinonim, antonim, gangguan–aktivitas (insomnia:tidur = disleksia:membaca).
- Contoh: KOMPAS : NAKHODA = MIKROSKOP : PENELITI.
- Jebakan: jangan pilih yang "mirip topiknya" — pilih yang hubungan logisnya sama persis.
### 2. Silogisme
- Inti: tarik kesimpulan yang PASTI benar dari 2–3 premis.
- Rumus cepat: "semua" → "sebagian" itu VALID (subalternasi: sebagian = "ada yang", bukan "hanya sebagian"). Rantai putus = "tidak dapat disimpulkan". Modus tollens: jika P maka Q; tidak Q → tidak P.
- Contoh: Semua PNS wajib lapor LHKPN. Sebagian peserta seminar adalah PNS. → Sebagian peserta seminar wajib lapor LHKPN.
- Jebakan: "tidak dapat disimpulkan" hanya benar kalau rantai putus — jangan over-pakai (kesalahan Sandi Hari 5 No. 20 & 29).
### 3. Penalaran Analitis
- Inti: susun info (posisi, urutan, jadwal, kategori) lalu simpulkan.
- Rumus cepat: gambar skema dulu (meja bundar, garis lurus, tabel). Cari info yang mengunci posisi.
- Contoh: 6 orang duduk melingkar, A berhadapan D, B di antara A dan C → yang berhadapan dengan B adalah E.
- Jebakan: "di sebelah kiri" tergantung arah hadap — baca soal pelan-pelan.
### 4. Berhitung Cepat
- Inti: operasi dasar, pecahan, desimal, persen — cepat & tepat.
- Rumus cepat: 12,5% = 1/8; 25% = 1/4; 33,33% = 1/3; 37,5% = 3/8; 62,5% = 5/8. a²−b² = (a+b)(a−b).
- Contoh: 2025² − 2024² = (2025+2024)(1) = 4049.
- Jebakan: jangan hitung panjang — cari jalan pintas identitas dulu.
### 5. Deret Angka
- Inti: cari pola selisih / rasio antar suku.
- Rumus cepat: cek selisih dulu → tetap = aritmetika; berlipat = geometri; tidak berpola = coba jumlah 2 suku sebelumnya / selisih bertingkat / dua larik selang-seling. Deret huruf = ubah ke nomor abjad (A=1).
- Contoh: 3, 6, 11, 18, 27, 38 → selisih +3,+5,+7,+9,+11 → berikut 51, 66. A,C,F,J,O → +2,+3,+4,+5 → U.
- Jebakan: deret dua operasi (mis. ×2 lalu −1) dan larik ganda sering keluar di soal HOTS.
### 6. Perbandingan Kuantitatif
- Inti: bandingkan dua nilai X dan Y: X>Y, X<Y, X=Y, atau tidak dapat ditentukan.
- Rumus cepat: sederhanakan dulu ke bentuk paling kecil sebelum membandingkan.
- Contoh: X = 33,33% dari 75 = 25; Y = 1/4 dari 100 = 25 → X = Y.
- Jebakan: "tidak dapat ditentukan" hanya kalau info memang kurang — jangan jadikan pelarian.
### 7. Soal Cerita
- Inti: terjemahkan cerita ke persamaan.
- Rumus cepat: rata-rata, perbandingan senilai/berbalik nilai, jarak = kecepatan × waktu, volume = debit × waktu, aritmetika sosial (untung/rugi, diskon), proyek (pekerja × hari).
- Contoh: baca soal, tulis "diketahui–ditanya" 10 detik sebelum menghitung.
- Jebakan: satuan beda (jam vs menit, km vs m) — samakan dulu.
### 8. Figural — Analogi, Ketidaksamaan, Serial
- Inti: pola gambar: rotasi, pencerminan, jumlah unsur, tambah/kurang elemen.
- Rumus cepat: cermin vertikal = kiri-kanan terbalik, atas-bawah tetap (segitiga tetap menunjuk ke atas). Rotasi 180° = putar, bukan cermin.
- Contoh: cari 1 gambar yang beda dari 4 gambar lain (ketidaksamaan).
- Jebakan: soal cermin vertikal — kesalahan verifikasi Mommy di Hari 8, jangan ulangi.
### 9. Matriks Figural 9 Kotak
- Inti: 3×3, pola bisa per baris ATAU per kolom: jumlah unsur, rotasi bertahap, operasi (gabung/kurang/irisan).
- Rumus cepat: cek baris dulu, kalau gagal cek kolom. Hitung jumlah elemen tiap sel — sering polanya aritmetika.
- Contoh: baris 1: 1+2=3 elemen → baris 2 & 3 ikut pola yang sama.
- Jebakan: pola bisa gabungan dua aturan sekaligus (mis. rotasi + tambah elemen).

## TKP — Tes Karakteristik Pribadi (45 soal, PG 166, skor 1–5)
Rumus umum 5 poin (berlaku semua aspek): aktif + konkret + sesuai prosedur + libatkan pihak yang tepat + tidak melanggar aturan. Diplomasi lunak saat aturan dilanggar = jebakan (kesalahan Sandi Hari 7 No. 22 & 28).
### 1. Pelayanan Publik
- Inti: ramah, tanggap, adil, tanpa diskriminasi, utamakan kepuasan warga sesuai tugas & wewenang.
- Contoh: warga berkas kurang → jelaskan syaratnya & bantu lengkapi, bukan menolak mentah-mentah.
- Jebakan: "baik hati tapi melanggar SOP" bukan 5 poin.
### 2. Jejaring Kerja
- Inti: bangun & bina hubungan, berbagi info, kolaborasi efektif.
- Contoh: butuh data dari unit lain → koordinasi resmi, bukan jalan pintas pribadi.
- Jebakan: kerja sendiri saat tim bisa membantu = bukan jawaban terbaik.
### 3. Sosial Budaya
- Inti: adaptasi & kerja efektif di masyarakat majemuk (agama, suku, budaya).
- Contoh: ditempatkan di daerah budaya berbeda → pelajari adat setempat, hormati, sesuaikan diri.
- Jebakan: bedakan dari anti-radikalisme — sosial budaya tanpa unsur ideologis.
### 4. Teknologi Informasi & Komunikasi
- Inti: manfaatkan teknologi untuk kinerja + jaga kerahasiaan data/informasi.
- Contoh: rekan minta bocoran soal tes internal → tolak tegas, ingatkan integritas (Hari 7 No. 22).
- Jebakan: membagikan info internal "demi membantu" tetap pelanggaran.
### 5. Profesionalisme
- Inti: laksanakan tugas sesuai wewenang & jabatan, konsisten, disiplin, tanggung jawab.
- Contoh: rekan menolak upacara karena ideologi → ingatkan kewajiban ASN, laporkan bila tetap menolak (Hari 7 No. 28).
- Jebakan: mengajak diskusi saja tanpa ketegasan prosedural = 3 poin, bukan 5.
### 6. Anti Radikalisme
- Inti: saring, tolak, laporkan paham radikal; setia Pancasila, UUD 1945, NKRI, Bhinneka (UU 20/2023, PP 94/2021, SKB 11 K/L 2019).
- Contoh: ada ajakan mengganti ideologi / intoleransi / provokasi anti-NKRI → tolak & laporkan.
- Jebakan: bedakan dari sosial budaya — anti-radikalisme selalu ada unsur ideologi/kekerasan/provokasi.

## Strategi waktu SKD (kartu penutup halaman Materi)
- 100 menit / 110 soal = ~54 detik per soal. Kerjakan yang mudah dulu, tandai yang ragu, kembali di akhir.
- Jangan kosongkan soal: TWK/TIU salah = 0 sama dengan kosong; TKP kosong = 0 padahal opsi terburuk masih 1.
- Urutan CAT: TWK → TIU → TKP (ikuti urutan ujian).
