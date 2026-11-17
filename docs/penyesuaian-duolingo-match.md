# BRIEF — Samakan dengan Duolingo Asli: Hapus 4 Kotak Unit, Desain Ulang Kotak Utama, Top Bar Tidak Sticky di Desktop (13 Nov 2026)

*Penulis: Mommy Malfoy — atas perintah Sandi.
Permintaan pengguna (verbatim): "sesuaikan dgn duolinggo aslinya dan hapus saja
4 bagan/kotak unit tiu tkp campuran dan twk dan untuk kotak utama itu desain nya
desain ulang dan hapus boder emas dan kata katanya di persingkat agar lebih rapi
dan untuk yg bars yg atas jgn dibuat stcikky kalau saat sesi desktop"
Referensi: 2 screenshot di folder ini + riset Duolingo
(`workspace/research_notes/duolingo-ui-algoritma-20261113/report.md`) + brief
layout desktop (`workspace/research_notes/duolingo-desktop-20261113/report.md`).*

## Screenshot di folder ini

- `duolingo-node-popover.png` — duolingo.com/learn: banner unit ungu
  "SECTION 1, UNIT 2 — Describe people" + tombol GUIDEBOOK; node yang diklik
  membuka popover (kartu melayang di atas node): judul + satu baris deskripsi
  + tombol PRACTICE +5 XP (putih) dan LEGENDARY +40 XP (kuning); node START
  di bawahnya; panel kanan Obsidian League + Daily Quests.
- `cpns-app-unit-bands.png` — aplikasi CPNS saat ini: kotak utama ber-border
  emas "JUMAT, 13 NOVEMBER — Hari 8 — TIU Figural + Ulangan Hari 5" + 4 kotak
  unit (TWK biru 1/1, TIU hijau 3/6, TKP ungu 1/1, Campuran oranye 2/3)
  masing-masing dengan tombol BUKA MATERI dan bar progres.

## Perubahan (4 item)

1. **HAPUS 4 kotak unit (TWK, TIU, TKP, Campuran) — seluruhnya**, termasuk
   tombol BUKA MATERI dan bar progres di dalamnya, di SEMUA ukuran layar.
   Setelah dihapus, Beranda langsung menampilkan kotak utama (banner) lalu
   jalur belajar (node). Tidak ada pengganti untuk kotak-kotak ini; progres
   tiap subtes tetap terlihat dari status node (selesai = mahkota/centang
   emas, saat ini = berdenyut, terkunci = abu-abu, terlewat = merah).
2. **DESAIN ULANG kotak utama (banner sesi hari ini)** mengikuti banner unit
   Duolingo: label kecil "BAGIAN SKD, UNIT 8" (tanpa panah kembali — aplikasi
   ini tidak punya navigasi unit sebelumnya) + judul singkat "TIU Figural" +
   tombol "Buka Materi" di kanan (padanan GUIDEBOOK). **HAPUS border emas.**
   Kata-kata DIPERSINGKAT: hapus baris tanggal "JUMAT, 13 NOVEMBER",
   deskripsi panjang ("Jumat, 13 November 2026: TIU Figural (30 soal baru)
   + ulangan silogisme Hari 5 No. 20 & 29 (2 soal variasi baru) · 32 soal"),
   dan baris skor ("Terakhir: 155/160 — kerjakan lagi"); maksimal satu
   sub-baris pendek ("Hari 8 · 32 soal"). Pill kecil "HARI INI" boleh
   dipertahankan sebagai penanda sesi hari ini, asalkan tetap rapi di dalam
   banner baru. Banner tetap memakai warna unit-nya (hijau TIU) seperti
   banner Duolingo yang berwarna per unit.
3. **Panel node yang diperluas mengikuti pola popover Duolingo:** saat sebuah
   node diklik, tampil kartu melayang di atas node berisi judul sesi + SATU
   baris deskripsi pendek + tombol-tombol aksi YANG SUDAH ADA (tanpa fitur
   baru, tanpa tombol LEGENDARY/XP karangan — aplikasi ini tidak punya itu).
   Chip subtes dari refresh tetap ada di dalam popover. Perilaku panel tidak
   berubah, hanya tampilannya.
4. **Top bar TIDAK sticky di desktop (≥1024px):** top bar (baris atas dengan
   streak/XP/cincin target) menjadi statis dan ikut ter-scroll bersama
   halaman. Di mobile (<1024px) top bar TETAP sticky seperti sekarang.
   Sidebar kiri dan panel kanan desktop tidak berubah (sidebar tetap fixed —
   itu bukan top bar).

## Batasan (tidak boleh dilanggar)

- Layout desktop 3 kolom dari edit sebelumnya tetap (sidebar 256px + kolom
  tengah + panel kanan 360px, breakpoint 1024px).
- Token Duolingo yang sudah ada saja; Hallmark Floor (tanpa gradien
  ungu-biru, tanpa card-in-card, tanpa ikon emoji, tanpa metrik karangan).
- Jangan sentuh data dan perilaku: 714 soal, 29 sesi, streak, Elo, FSRS-6,
  draf sesi, pintasan keyboard. Placeholder simulasi (0 soal) tetap.
- Node merah TERLEWAT (Hari 1 & 2b) tetap. Maskot + tip hari ini tetap.
  Tema bawaan tetap gelap navy #131F24.
- Jangan pakai aset/brand Duolingo (logo, burung, teks milik Duolingo). Yang
  ditiru polanya, bukan asetnya.

## Kriteria selesai (cara memeriksa)

- Capture DESKTOP (≥1280px): 4 kotak unit HILANG; kotak utama tampil sebagai
  banner bersih gaya Duolingo (label + judul singkat + Buka Materi, tanpa
  border emas, tanpa deskripsi panjang); top bar tidak sticky (capture
  setelah scroll menunjukkan top bar ikut ter-scroll); popover node tampil
  saat node diklik (judul + 1 baris + tombol aksi yang sudah ada).
- Capture MOBILE 390px: top bar TETAP sticky; 4 kotak unit juga hilang;
  banner utama yang baru tampil di mobile.
- Audit lulus: 0 console error, 0 overflow di kedua ukuran.
- Data utuh: 29 sesi, 714 soal, attempt 1, streak 7, XP 155, Elo 1500.
- Attestasi membandingkan BEFORE vs sesudah dan menyatakan perubahan di atas
  hadir.

## Non-goal

- Tidak ada sesi/soal/fitur baru. Tidak ada perubahan tema. Tidak ada
  perubahan layout mobile selain penghapusan 4 kotak unit dan banner baru
  (yang berlaku di semua ukuran).
