# Materi SKD — Pack v1 untuk tab "Materi" aplikasi Duolingo CPNS
Disusun 2026-11-13 pagi (WIB) atas permintaan Sandi: "tambahkan page atau button di bawah khusus materi, isinya materi SKD TIU dll, cari materi di internet sampai dalam".
Aturan penulisan (jawaban atas keluhan "tulisan yg komplrk atau banyak"): tiap kartu materi maks 3 poin singkat + 1 contoh cepat + 1 jebakan. Tanpa paragraf panjang. Bahasa Indonesia ringkas.

## Acuan resmi
- KepmenPANRB 674/2026 (ditetapkan 20 Nov 2026; bukan "Permen") — kisi-kisi + passing grade SKD 2026, MENGGANTIKAN KepmenPANRB 321/2024. Struktur & ambang batas tidak berubah dari 2024.
- SKD: 110 soal / 100 menit, CAT BKN, maks 550. TWK 30 soal (PG 65, maks 150), TIU 35 soal (PG 80, maks 175), TKP 45 soal (PG 166, maks 225, skor 1–5 per opsi, kosong = 0). Harus lolos tiap subtes + masuk 3x formasi ke SKB. Target aman Sandi: TWK 90+, TIU 110+, TKP 185+ (total 385).
- PG kebutuhan khusus (674/2026): cumlaude & diaspora total ≥ 311 + TIU ≥ 85 (tanpa ambang TWK/TKP per subtes); disabilitas & Papua total ≥ 286 + TIU ≥ 60.
- SKB: CAT BKN 90 menit (120 menit disabilitas sensorik netra), benar 5 / salah-kosong 0 — 80 soal bila dominan hitungan/teknis komputasi, 100 soal bila dominan konsep/teori.
- Pendaftaran CPNS 2026 dibuka 27 Nov 2026; 154.052 formasi (instansi pusat).
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
- BARU 674/2026: Bahasa Indonesia menguji MEMAHAMI, MENGGUNAKAN, MENGEVALUASI, dan MEREFLEKSI informasi/argumen — bukan sekadar EYD. Latih: evaluasi argumen (apakah kesimpulan didukung bukti?), kelemahan penalaran (generalisasi berlebihan, bukti tidak relevan), refleksi atas teks (implikasi/sikap apa yang tepat dari isi teks?).
- EYD murni (ejaan, kata baku, kalimat efektif) hanya pemanasan — tetap kuasai sebagai poin cepat, tapi jangan jadikan fokus utama.

## TIU — Tes Intelegensi Umum (35 soal, PG 80)
### 1. Analogi (verbal)
- Inti: cari hubungan pasangan kata pertama, terapkan ke pasangan kedua.
- Rumus cepat: hubungan umum = alat–profesi (stetoskop:dokter), sebab–akibat, bagian–keseluruhan, sinonim, antonim, gangguan–aktivitas (insomnia:tidur = disleksia:membaca).
- Contoh: KOMPAS : NAKHODA = MIKROSKOP : PENELITI.
- Jebakan: jangan pilih yang "mirip topiknya" — pilih yang hubungan logisnya sama persis.
- CATATAN 674/2026: analogi verbal TURUN ke pemanasan/drill — daftar verbal resmi 2026 hanya Silogisme, Penalaran Induktif, Analitis. Simulasi verbal fokus ke tiga itu; analogi tetap melatih pola hubungan, tapi tidak boleh memakan kuota simulasi (terutama kuota Penalaran Induktif).
### 2. Silogisme
- Inti: tarik kesimpulan yang PASTI benar dari 2–3 premis.
- Rumus cepat: "semua" → "sebagian" itu VALID (subalternasi: sebagian = "ada yang", bukan "hanya sebagian"). Rantai putus = "tidak dapat disimpulkan". Modus tollens: jika P maka Q; tidak Q → tidak P.
- Contoh: Semua PNS wajib lapor LHKPN. Sebagian peserta seminar adalah PNS. → Sebagian peserta seminar wajib lapor LHKPN.
- Jebakan: "tidak dapat disimpulkan" hanya benar kalau rantai putus — jangan over-pakai (kesalahan Sandi Hari 5 No. 20 & 29).
### 3. Penalaran Induktif (BARU 2026)
- Inti (definisi resmi 674/2026): mengidentifikasi pola hubungan, tren, atau prinsip umum dari serangkaian informasi yang terpisah untuk merumuskan generalisasi, penjelasan, atau perkiraan yang PALING BERPELUANG BENAR. Bukan silogisme deduktif (kesimpulannya pasti), bukan sekadar pemahaman bacaan.
- Rumus cepat — cara menggeneralisasi: (1) petakan tiap fakta (variabel + hasil); (2) cari tren searah di semua fakta (naik/turun bersama); (3) pilih generalisasi yang didukung SEMUA fakta dan tidak dibantah satu pun; (4) tolak klaim yang melampaui data (angka pasti, "selalu", "hanya", kausalitas terbalik).
- Contoh (exemplar v2, kunci B — lulus penuh audit): Enam desa, stunting turun: A mingguan 12%; B mingguan+pelatihan 18%; C bulanan 3%; D tidak aktif naik 2%; E mingguan+PMT 20%; F mingguan+pelatihan+PMT 24%. Kunci B: "Semakin teratur layanan posyandu dan semakin lengkap intervensi gizinya, semakin besar penurunan angka stunting." Desa F menuntaskan gradasi 0→1→2 intervensi (12%→18%/20%→24%) — klaim "semakin lengkap" berdiri di atas bukti utuh.
- Jebakan: A = fokus variabel tunggal (dibantah sebaran desa mingguan 12–24%); C = dibantah satu fakta (Desa C hanya 3%, bukan ≥10%); D = over-generalisasi n=1 (20% vs 18% satu pasangan desa); E = kausalitas terbalik (penurunan mendorong posyandu aktif). Waspada kata absolut di pengecoh (hanya/selalu/pasti/tidak berhubungan) — tapi kunci v2 bebas kata absolut, jadi jangan menebak dari kata absolut saja.
### 4. Penalaran Analitis
- Inti: susun info (posisi, urutan, jadwal, kategori) lalu simpulkan.
- Rumus cepat: gambar skema dulu (meja bundar, garis lurus, tabel). Cari info yang mengunci posisi.
- Contoh: 6 orang duduk melingkar, A berhadapan D, B di antara A dan C → yang berhadapan dengan B adalah E.
- Jebakan: "di sebelah kiri" tergantung arah hadap — baca soal pelan-pelan.
### 5. Berhitung Cepat
- Inti: operasi dasar, pecahan, desimal, persen — cepat & tepat.
- Rumus cepat: 12,5% = 1/8; 25% = 1/4; 33,33% = 1/3; 37,5% = 3/8; 62,5% = 5/8. a²−b² = (a+b)(a−b).
- Contoh: 2025² − 2024² = (2025+2024)(1) = 4049.
- Jebakan: jangan hitung panjang — cari jalan pintas identitas dulu.
### 6. Deret Angka
- Inti: cari pola selisih / rasio antar suku.
- Rumus cepat: cek selisih dulu → tetap = aritmetika; berlipat = geometri; tidak berpola = coba jumlah 2 suku sebelumnya / selisih bertingkat / dua larik selang-seling. Deret huruf = ubah ke nomor abjad (A=1).
- Contoh: 3, 6, 11, 18, 27, 38 → selisih +3,+5,+7,+9,+11 → berikut 51, 66. A,C,F,J,O → +2,+3,+4,+5 → U.
- Jebakan: deret dua operasi (mis. ×2 lalu −1) dan larik ganda sering keluar di soal HOTS.
### 7. Perbandingan Kuantitatif (2 & 3 data)
- Inti (definisi resmi 674/2026): menarik kesimpulan berdasarkan DUA atau TIGA data kuantitatif. Format 2 data (P vs Q) dan 3 data (P, Q, R) — jangan hanya terpaku P vs Q.
- Rumus cepat: sederhanakan dulu ke bentuk paling kecil sebelum membandingkan. Pecahan istimewa: 12,5% = 1/8; 62,5% = 5/8; 37,5% = 3/8. Teknik bagi-dulu: bagi pengali dengan penyebut sebelum mengalikan (96 ÷ 8 = 12, lalu × 5 = 60).
- Contoh (exemplar v2, kunci D — lulus penuh audit): P = 62,5% dari 96 = 60; Q = 5/9 dari 135 = 75; R = 0,6 × 125 = 75 → Q = R > P. Representasi campuran (persen istimewa/pecahan/desimal) + pengali berbeda + relasi kesamaan; selesai 20–35 detik dengan bagi-dulu. Nilai kembar Q = R menghukum yang hanya mengira-ngira.
- Variasi relasi (jangan hafal template Q=R>P): tiga nilai berbeda yang berdekatan, atau relasi operasi (P+Q vs 2R). Varian aljabar outlier (porsi 10–15% pamungkas): 0<x<1, P=x², Q=√x, R=1/x → P<Q<R.
- Jebakan: "tidak dapat ditentukan" hanya kalau info memang kurang — jangan jadikan pelarian. Heuristik pembilang terbesar menyesatkan (v1 gagal: 11/16 vs 7/12 vs 5/8 dengan pengali ×96 identik merosot jadi urutan pecahan dasar).
### 8. Soal Cerita
- Inti: terjemahkan cerita ke persamaan.
- Rumus cepat: rata-rata, perbandingan senilai/berbalik nilai, jarak = kecepatan × waktu, volume = debit × waktu, aritmetika sosial (untung/rugi, diskon), proyek (pekerja × hari).
- Contoh: baca soal, tulis "diketahui–ditanya" 10 detik sebelum menghitung.
- Jebakan: satuan beda (jam vs menit, km vs m) — samakan dulu.
### 9. Figural — Analogi, Ketidaksamaan, Serial
- Inti: pola gambar: rotasi, pencerminan, jumlah unsur, tambah/kurang elemen.
- Rumus cepat: cermin vertikal = kiri-kanan terbalik, atas-bawah tetap (segitiga tetap menunjuk ke atas). Rotasi 180° = putar, bukan cermin.
- Contoh: cari 1 gambar yang beda dari 4 gambar lain (ketidaksamaan).
- Jebakan: soal cermin vertikal — kesalahan verifikasi Mommy di Hari 8, jangan ulangi.
- CATATAN 674/2026 — BEDAKAN TEGAS: Ketidaksamaan (odd-one-out: 5 gambar sejajar, cari 1 yang berbeda) adalah item resmi 2024; di 2026 slotnya digantikan Penalaran Matriks. Odd-one-out tetap sah sebagai latihan pola, tapi BUKAN matriks — jangan pernah menghitungnya sebagai penalaran matriks.
### 10. Penalaran Matriks (menggantikan Ketidaksamaan di 2026)
- Inti (definisi resmi 674/2026): memahami pola melalui BERBAGAI MACAM PERSPEKTIF dan menentukan perspektif mana yang dapat menyelesaikan permasalahan. Wujudnya: grid (mis. 3×3 dengan 1 sel kosong) — analisis multi-perspektif: per baris, per kolom, rotasi, operasi penjumlahan/pengurangan elemen.
- Rumus cepat: cek baris dulu, kalau gagal cek kolom. Hitung jumlah elemen tiap sel — sering polanya aritmetika.
- Contoh: baris 1: 1+2=3 elemen → baris 2 & 3 ikut pola yang sama.
- Jebakan: pola bisa gabungan dua aturan sekaligus (mis. rotasi + tambah elemen). Jangan hitung odd-one-out sebagai matriks (lihat §9).

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
### 4. Teknologi Informasi & Komunikasi (Adaptasi TIK)
- Inti (674/2026): pemanfaatan TIK secara BIJAK dengan tetap mematuhi PRINSIP-PRINSIP ETIS — kerahasiaan data, keamanan informasi, etika komunikasi digital. Bukan sekadar "melek teknologi": skor 5 = memanfaatkan teknologi SEKALIGUS menjaga etika & keamanan datanya.
- Contoh: rekan minta bocoran soal tes internal → tolak tegas, ingatkan integritas (Hari 7 No. 22).
- Jebakan: membagikan info internal "demi membantu" tetap pelanggaran; "proaktif belajar sistem baru" saja belum 5 bila mengabaikan keamanan data.
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
- SKB (bila lolos): CAT BKN 90 menit (120 menit disabilitas sensorik netra) — 80 soal bila dominan hitungan/teknis komputasi, 100 soal bila dominan konsep/teori. Benar 5, salah/kosong 0.
