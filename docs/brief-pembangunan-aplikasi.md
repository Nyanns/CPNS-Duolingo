# Brief: Aplikasi Web Latihan CPNS (Duolingo CPNS) — 12 Nov 2026

## Permintaan pengguna (verbatim)
"mulai sekrang soalnya buat seperti wweb app mom jadi bisa di klik klik jadi aku gak nulis manual, tapi sesuai dgn yg sudah kita diskusikan oke soal soalnya dll"

Artinya: mulai sekarang SEMUA sesi latihan CPNS disampaikan lewat aplikasi web interaktif — pengguna menjawab dengan KLIK, bukan menulis jawaban manual. Isi, kisi-kisi, tingkat kesulitan, dan semua keputusan yang sudah didiskusikan tetap berlaku penuh (lihat bawah). Aplikasi ini menggantikan pengiriman file markdown harian sebagai medium latihan (file tetap boleh disimpan sebagai arsip, tapi latihan dikerjakan di aplikasi).

## Pengguna
Sandi — S1 Informatika, IPK 3,94, fresh graduate (lulus Sep 2025), Yogyakarta. Bahasa antarmuka: Bahasa Indonesia. Tujuan: lolos CPNS (SKD diperkirakan Feb–Mar 2027; pendaftaran ditargetkan Nov 2026). Target skor aman SKD: TWK 90+, TIU 110+, TKP 185+, total 385/550.

## Struktur resmi yang TIDAK BOLEH salah
- SKD: 110 soal / 100 menit, urutan CAT: TWK 30 → TIU 35 → TKP 45. Skor maks 550.
- TWK/TIU: benar 5, salah/kosong 0. TKP: tiap opsi bernilai 1–5, kosong 0.
- Passing grade (acuan 2024): TWK 65, TIU 80, TKP 166. Harus lolos ketiganya; hanya peringkat 3× formasi yang ke SKB; nilai akhir 40% SKD + 60% SKB.
- Kisi-kisi resmi = **KepmenPANRB 321/2024** (BUKAN "PermenPANRB"; Kepmen 320/2024 = Mekanisme Seleksi, BUKAN kisi-kisi). Belum ada Kepmen CPNS 2026 per 12 Nov 2026 — acuan tetap 321/2024.
- TWK: nasionalisme, integritas, bela negara, pilar negara (Pancasila, UUD 1945, NKRI, Bhinneka Tunggal Ika), bahasa negara. TIU verbal: analogi, silogisme (2 premis), analitis. TIU numerik: berhitung, deret, perbandingan kuantitatif, soal cerita. TIU figural: analogi gambar, ketidaksamaan, serial. TKP: pelayanan publik, jejaring kerja, sosial budaya, TIK, profesionalisme, anti radikalisme.
- KEJUJURAN WAJIB: semua soal di aplikasi adalah soal LATIHAN berpola sama dengan SKD (bukan soal resmi BKN — BKN tidak mempublikasikan soal). Beri label pada tiap sesi: "[Latihan — mengacu kisi-kisi Kepmen 321/2024]". Jangan pernah menyebut soal sebagai soal asli/bocoran BKN.

## Kalibrasi isi (hasil riset mendalam 12 Nov 2026 — WAJIB diikuti)
Sumber: `~/workspace/research_notes/cpns-vs-kedinasan-kisi-kisi-hots-20261112-0312/report.md` (§4–§6). Ringkasnya:
- TAMBAH: TWK Bahasa Indonesia (ide pokok, inti kalimat, sinonim kata bercetak miring, kesimpulan teks) ~4–6 dari 30 soal TWK; TIU analisis tabel & perbandingan kuantitatif format tabel ~5–7 dari 35 TIU; TIU figural 9 kotak (matriks 3×3: kombinasi baris/kolom + rotasi 90°) ~4–6 soal; TIU penalaran analitis (urutan duduk melingkar, susunan/posisi, SPOK) ~3–4 soal; analogi 3 kata & analogi kalimat; TWK narasi panjang "seperti TKP" 5–10 soal (netralitas ASN Pemilu/Pilkada, nasionalisme digital, wewenang MK vs MA dalam kasus); TKP teknologi/spionase/kerahasiaan informasi, inovasi kantor, manajemen waktu/prioritas; TKP campuran narasi panjang + pendek.
- KURANGI: hafalan murni TWK (<15% porsi TWK — ubah jadi soal implementasi/kasus); deret satu operasi yang sangat mudah (pemanasan saja; porsi utama: dua operasi, dua lapis/berselang, Fibonacci/campuran); silogisme 1 premis & analogi 2 kata trivial (ganti silogisme 2 premis narasi termasuk kuantor "sebagian" yang memutus rantai, dan analogi 3 kata/kalimat); TKP "baik vs buruk" yang jelas (ganti opsi bernuansa: semua tampak benar, pembeda proaktif vs pasif, prosedural vs melanggar wewenang).
- HAPUS dari bank SKD: Bahasa Inggris, TPA, Matematika/Fisika SMA lanjut (itu materi seleksi lanjutan kedinasan, bukan SKD).
- JANGAN pakai label "pasal kembar UUD 1945" sebagai kategori soal — istilah itu tidak ada di laporan peserta soal asli. Pakai "implementasi pasal UUD 1945 dalam kasus" / "wewenang MK vs MA". (Kebingungan pasalnya nyata — 3 soal Hari 4 salah karena itu — tapi labelnya diganti.)
- Jebakan yang harus ada: opsi TWK "benar sebagian" (pilih jawaban paling lengkap); "sebagian" memutus rantai silogisme; deret dua operasi/dua lapis; pengecoh anggaran di soal cerita; perbandingan kuantitatif format hubungan (X>Y, X=Y, X<Y, tidak dapat ditentukan); figural perubahan kecil satu elemen; TKP pasif-yang-terdengar-bijak vs proaktif-prosedural; soal TIU panjang di awal paket simulasi untuk melatih menandai & melewati.
- TKP: kunci berdasarkan PRINSIP (prosedural, netral, proaktif, sesuai wewenang), dengan pembahasan per-opsi (mengapa opsi ini 5, itu 4/3/2). Kunci TKP antar bimbel bisa bertentangan — jangan kalibrasi pada satu kunci; kalibrasi pada prinsip.

## ATURAN KUALITAS (pelajaran dari kesalahan sebelumnya — WAJIB)
1. **Posisi kunci jawaban HARUS diacak di setiap sesi.** Pada Hari 7, SEMUA 30 jawaban 5 poin berada di posisi B — cacat fatal yang membuat skor tidak bisa dipercaya. Periksa distribusi sebelum sesi diterbitkan: tiap posisi A–D harus roughly seimbang, tidak ada posisi yang memuat >40% kunci dalam satu sesi. TKP: posisi jawaban 5 poin harus tersebar.
2. **Nomor soal selalu tampil; soal yang dilewati terlacak otomatis** (pelajaran Hari 6: jawaban tanpa nomor menyebabkan salah alignment dan skor 20/30 yang keliru, baru terkoreksi jadi 25/30). Di aplikasi ini masalah itu hilang dengan sendirinya — jawaban terikat ke nomor soal — tapi pastikan UI selalu menampilkan nomor soal dan status (dijawab / ditandai / dilewati).
3. **Verifikasi kunci sebelum menerbitkan sesi** — baca ulang tiap kunci dan pembahasan; jangan ada kunci yang bertentangan dengan pembahasannya sendiri.

## Fitur aplikasi (fullstack — menyimpan jawaban, skor, dan buku kesalahan)
1. **Bermain soal dengan klik:** satu soal per layar, opsi jawaban berupa tombol besar yang bisa diklik; timer sesi (mundur); bilah progres (Soal X dari Y); tombol "Tandai & lewati" (Ghost Walk — kembali di akhir); navigasi grid nomor soal dengan warna status (dijawab = hijau, ditandai = kuning, belum = abu-abu); tombol "Selesai & lihat skor".
2. **Mode sesi harian:** 30–33 soal (sesuai rotasi: Senin TWK, Selasa TIU verbal, Rabu TIU numerik, Kamis TKP, Jumat TIU figural, Sabtu tryout/simulasi, Minggu review + SKB ringan). Tiap sesi diawali ringkasan pelajaran fundamental singkat (ditampilkan di atas soal pertama atau sebagai kartu intro).
3. **Mode Simulasi Penuh:** 110 soal / 100 menit, urutan CAT asli (TWK 30 → TIU 35 → TKP 45), timer 100:00 yang tidak bisa dijeda, instruksi simulasi (kerjakan nonstop, HP disingkirkan, soal mudah dulu → tandai yang ragu → kembali di akhir). Target: TWK 90 / TIU 110 / TKP 185 (total ≥385/550).
4. **Penilaian otomatis:** TWK/TIU benar = 5, salah/kosong = 0. TKP = skor per opsi (1–5) sesuai rubrik soal. Hasil per subtes + total + status vs passing grade (65/80/166) dan vs target aman (90/110/185). Tampilkan skor mentah dan persentase.
5. **Pembahasan setelah selesai:** tiap soal menampilkan kunci, pembahasan singkat, dan jebakannya. Soal yang salah otomatis masuk Buku Kesalahan.
6. **Buku Kesalahan (spaced repetition):** daftar soal yang pernah salah, dengan jadwal ulang (1–3–7–14–30 hari). Mode "Ulangi soal yang salah" yang memutar soal-soal itu (dengan posisi opsi diacak ulang agar bukan hafalan posisi).
7. **Dasbor progres:** riwayat skor per hari (lihat "Skor sejauh ini" di bawah), streak hari latihan, dan prediksi saat ini (TWK 110–130, TIU 125–155, TKP 170–200, total ~445 — perkiraan, bukan janji).
8. **Aksi untuk penambahan sesi (PENTING — untuk cron harian):** aplikasi HARUS menyediakan aksi/server action `addSession` (menerima: judul, tanggal, topik, daftar soal lengkap dengan opsi/kunci/pembahasan/skor TKP per opsi) dan `listSessions`, sehingga sesi-sesi baru (Hari 9 dst., dan 110 soal simulasi Sabtu 14 Nov) bisa dimasukkan tanpa rebuild. Sesi simulasi Sabtu BELUM dibuat saat aplikasi ini dibangun — modenya harus sudah ada, dan soalnya akan dimasukkan Sabtu pagi lewat aksi ini (sampai saat itu tampilkan "Soal simulasi akan dimasukkan Sabtu pagi, 14 Nov").
9. **Figural:** soal figural dirender sebagai grid visual — gunakan simbol Unicode (▲ ■ ● ◆ ★ ◐ dll.) dan/atau SVG sederhana untuk matriks 3×3, pola rotasi, dan ketidaksamaan. Harus terbaca jelas di HP.

## Isi awal (transkripsi WAJIB dari file sumber — JANGAN mengarang soal baru kecuali yang diminta)
Transkripsikan SELURUH soal dari file-file ini kata-per-kata (teks soal, semua opsi, kunci, pembahasan, jebakan; TKP beserta skor tiap opsi). Jika ada soal yang tidak bisa ditranskripsi dengan setia (mis. figural yang butuh gambar dan tidak bisa diwakili simbol/SVG), lewati soal itu dan laporkan nomornya — jangan mengarang pengganti.
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-1-2026-11-06.md` — 10 analogi TIU.
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-2-2026-11-07.md` — 15 soal campuran (tryout mini).
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-2b-2026-11-07.md` — 16 soal (fundamental deret + soal baru).
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-3-2026-11-08.md` — 10 soal review + 5 soal SKB (ITIL Incident Management).
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-4-2026-11-09.md` — 30 soal TWK (pasal UUD 1945).
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-5-2026-11-10.md` — 30 soal TIU verbal (analogi + silogisme).
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-6-2026-11-11.md` — 30 soal TIU numerik (deret + soal cerita).
- `~/workspace/goals/lolos-cpns/files/latihan-cpns-hari-7-2026-11-12.md` — 30 soal TKP + 3 soal ulangan pasal.
- Bank 42 soal: `~/workspace/research_notes/cpns-bank-soal-metode-belajar-20261106-0408/report.md` — 42 soal (TWK 9, TIU verbal 8, TIU numerik 9, TIU figural 8, TKP 8) beserta kunci/pembahasan/sumber. Masukkan sebagai mode "Bank Latihan" terpisah.
- Detail jadwal, skor, dan buku kesalahan: `~/workspace/goals/lolos-cpns/hidden_files/run-log.md` dan `~/workspace/goals/lolos-cpns/GOAL.md`.

## Sesi Hari 8 — BUAT BARU di dalam aplikasi (sesi aktif besok, Jumat 13 Nov)
Buat sesi "Hari 8 — Jumat, 13 November 2026: TIU Figural + ulangan Hari 5" — 32 soal: 30 soal figural BARU (BUKAN daur ulang soal figural Hari 2/2b/3 atau bank 42) + 2 soal ulangan silogisme Hari 5 (No. 20 & 29 — refleks "tidak dapat disimpulkan" yang over-firing — buat variasi baru dengan rantai yang sama, bukan soal identik). Komposisi figural (ikuti kalibrasi): matriks 9 kotak ~5 soal, serial ~8, ketidaksamaan ~6, analogi gambar ~6, penalaran analitis (duduk melingkar, susunan/posisi) ~5. Target: figural ≥24/30, ulangan 2/2. Pelajaran fundamental singkat di awal: cara membaca matriks 9 kotak (kombinasi baris/kolom + rotasi), pola serial, dan aturan analitis. Posisi kunci DIACAK (periksa distribusinya). Sertakan kunci + pembahasan + jebakan tiap soal.

## Buku Kesalahan yang masih aktif (masukkan sebagai item review dengan jadwalnya)
- Hari 5 No. 20 & 29 (silogisme — refleks "tidak dapat disimpulkan" over-firing): diulang di Hari 8 (13 Nov).
- Hari 6 No. 15, 17, 18, 26 (deret kuadrat−1; soal cerita pekerja-hari, rata-rata, jumlah-selisih): diulang pasca-simulasi Sabtu 14 Nov.
- Hari 7 No. 22 & 28 (TKP — pilih opsi diplomasi lunak, bukan tegas prosedural): diulang Minggu 15 Nov.
- Hari 4 No. 7, 10, 15: LUNAS (diulang Hari 7, 3/3 benar) — tampilkan sebagai "selesai", bukan item aktif.

## Skor sejauh ini (tampilkan di dasbor)
- Hari 1 (6 Nov): 10 soal analogi — BELUM dijawab.
- Hari 2 (7 Nov): 15/15 SEMPURNA (tryout mini campuran).
- Hari 2b (7 Nov): 16 soal — BELUM dijawab.
- Hari 3 (8 Nov): 15/15 SEMPURNA (review 10/10 + SKB 5/5).
- Hari 4 (9 Nov): TWK 27/30 (135/150).
- Hari 5 (10 Nov): TIU verbal 28/30 (~163 poin).
- Hari 6 (11 Nov): TIU numerik 25/30 (125 poin) — setelah koreksi alignment (No. 11 kosong).
- Hari 7 (12 Nov): TKP 146/150 — DENGAN CATATAN: semua kunci 5 poin ada di posisi B (cacat file); ulangan pasal 3/3.

## Jadwal ke depan (untuk mode sesi)
- Jumat 13 Nov: Hari 8 figural + ulangan Hari 5 (dibuat di aplikasi ini).
- Sabtu 14 Nov 10:00: SIMULASI PENUH 110 soal/100 menit (soal dimasukkan Sabtu pagi via aksi addSession).
- Minggu 15 Nov: review mingguan + SKB ringan topik #2 + ulang Hari 7 No. 22, 28.
- Senin 16 Nov dst.: rotasi normal (Senin TWK, Selasa TIU verbal, Rabu TIU numerik, Kamis TKP, Jumat figural, Sabtu tryout mini, Minggu review + SKB).
