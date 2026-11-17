# BRIEF — Polish Duolingo: Panel Kanan Sticky, Proporsi Tengah Simetris, Ukuran Node & Font, Warna Duolingo (13 Nov 2026)

*Penulis: Mommy Malfoy — atas perintah Sandi.
Permintaan pengguna (verbatim): "buat agar bagan yg kanan itu stcikky seperti
sama yg di duolinggo dan perhatikan lagi bagan yg tngah agar proposinla teap di
tengah dan siemtris semuanya oke tersusun rapi dan teratur pokoknnya samakan
seperti di screensht duolinggo dan untuk besar kecilnya point atau linggkaran
untuk bagan tengah diperhatikan lagi dan font nya sesuiakan oke agar past
ukurannya dan warnanya jgn terlalu kontras oke sesuaikan duolinggo aslinya theme
dan warnanya dan desain dan efek oke"
Referensi: 2 screenshot di folder ini + riset Duolingo
(`workspace/research_notes/duolingo-ui-algoritma-20261113/report.md`) + brief
layout desktop (`workspace/research_notes/duolingo-desktop-20261113/report.md`)
+ brief penyesuaian Duolingo (`workspace/research_notes/cpns-duolingo-match-20261113/report.md`).*

## Screenshot di folder ini

- `duolingo-learn-unit9.png` — duolingo.com/learn: banner unit merah
  "SECTION 1, UNIT 9 — Tell time" + GUIDEBOOK; node terkunci abu-abu +
  karakter abu-abu; panel kanan: bar statistik atas (bendera 6, api 0, gem
  2636), kartu Obsidian League, kartu Daily Quests; sidebar kiri fixed.
- `cpns-app-desktop-current.png` — aplikasi CPNS saat ini (desktop): sidebar
  "Latihan CPNS", kolom tengah dengan node Hari 2b (merah TERLEWAT), Hari 3,
  Hari 4 (node hijau besar + mahkota, judul 2–3 baris), panel kanan kartu
  "Elo 1500 — Liga Emas".

## Perubahan (5 item)

1. **Panel kanan kembali STICKY seperti Duolingo.** Kolom kanan (kartu
   statistik, Daily Quests, Buku Kesalahan, Elo) memakai position: sticky
   dengan offset atas yang pas, sehingga tetap terlihat saat halaman
   di-scroll — persis perilaku panel kanan duolingo.com/learn. **Ini
   MEMBATALKAN perubahan edit sebelumnya yang membuat panel kanan statis
   (tidak sticky).** Sidebar kiri tetap fixed seperti sekarang.
2. **Kolom tengah: proporsi di tengah, simetris, rapi, teratur.** Lebar kolom
   tengah dijaga max-width ~600px ala Duolingo dan selalu terpusat di antara
   sidebar dan panel kanan. Node-node jalur memakai pola zigzag Duolingo
   (posisi berselang-seling kiri/tengah/kanan secara simetris, bukan tumpukan
   lurus di tengah), dengan jarak vertikal yang konsisten. Judul sesi
   terpusat di bawah node-nya. Semua elemen tengah tersusun rapi dan teratur
   seperti screenshot Duolingo.
3. **Ukuran node (lingkaran/point) disesuaikan dengan Duolingo.** Node jalur
   (lingkaran) dibuat seukuran node Duolingo (~70px diameter), dengan ikon di
   dalamnya (mahkota/centang/bintang) diskalakan secara proporsional.
   Gelembung START, peti, dan trofi juga diskalakan agar proporsional dengan
   node. Node saat ini tetap berdenyut seperti Duolingo.
4. **Font disesuaikan agar pas ukurannya.** Ukuran font judul node, banner
   unit, menu sidebar, dan kartu panel kanan disesuaikan dengan skala
   Duolingo (Varela Round tetap): judul node cukup kecil agar muat 1–2 baris
   dan terpusat; teks sekunder lebih kecil dan lebih lembut. Tidak ada teks
   yang meluber atau membungkus berlebihan.
5. **Warna, tema, desain, dan efek disesuaikan dengan Duolingo asli (mode
   gelap).** Audit palet: warna aksen yang terlalu kontras/menyala diredam ke
   nilai token mode gelap Duolingo — teks sekunder lebih lembut (abu-abu
   Duolingo, bukan putih keras), node terkunci abu-abu yang lembut, merah
   status TERLEWAT diredam (tidak menyala kasar), hijau node tetap hijau
   Duolingo tapi dengan efek lip/shadow yang sama seperti Duolingo. Efek
   dipertahankan/disesuaikan: bayangan lip 3D di bawah node dan tombol, pulse
   pada node saat ini, transisi hover yang lembut. Tema bawaan tetap gelap
   navy #131F24.

## Batasan (tidak boleh dilanggar)

- Layout desktop 3 kolom tetap (sidebar 256px + kolom tengah ~600px + panel
  kanan 360px, breakpoint 1024px). Mobile tidak berubah (top bar mobile
  tetap sticky).
- Banner utama ala Duolingo dari edit sebelumnya tetap (label + judul singkat
  + Buka Materi, tanpa border emas). 4 kotak unit tetap terhapus. Popover
  node tetap.
- Token Duolingo yang sudah ada saja; Hallmark Floor (tanpa gradien
  ungu-biru, tanpa card-in-card, tanpa ikon emoji, tanpa metrik karangan).
- Jangan sentuh data dan perilaku: 714 soal, 29 sesi, streak, Elo, FSRS-6,
  draf sesi, pintasan keyboard. Placeholder simulasi (0 soal) tetap.
- Node merah TERLEWAT (Hari 1 & 2b) tetap (warnanya saja diredam). Maskot +
  tip hari ini tetap.
- Jangan pakai aset/brand Duolingo (logo, burung, teks milik Duolingo). Yang
  ditiru pola, warna, dan efeknya.

## Kriteria selesai (cara memeriksa)

- Capture DESKTOP (≥1280px) setelah scroll: panel kanan TETAP TERLIHAT
  (sticky) sementara kolom tengah ter-scroll; sidebar tetap fixed.
- Capture DESKTOP: kolom tengah terpusat dengan max-width ~600px; node-node
  berzigzag simetris dengan jarak konsisten; node berukuran ~70px; judul node
  1–2 baris, font pas.
- Capture DESKTOP + MOBILE 390px: warna lebih lembut / tidak terlalu kontras
  dibanding BEFORE; teks sekunder abu-abu lembut; node terkunci abu-abu
  lembut.
- Audit lulus: 0 console error, 0 overflow di kedua ukuran.
- Data utuh: 29 sesi, 714 soal, attempt 1, streak 7, XP 155, Elo 1500.
- Attestasi membandingkan BEFORE vs sesudah dan menyatakan perubahan di atas
  hadir.

## Non-goal

- Tidak ada sesi/soal/fitur baru. Tidak ada perubahan tema ke terang. Tidak
  ada perubahan layout mobile selain penyesuaian ukuran node/font/warna yang
  berlaku di semua ukuran.
