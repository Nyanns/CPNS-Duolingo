# BRIEF — Lingkaran Node (Lesson Path) ala Duolingo: Desain 3D, Warna Mastery (13 Nov 2026)

*Penulis: Mommy Malfoy — atas perintah Sandi.
Permintaan pengguna (verbatim): "tiru desain lingkarannya samakan assetnya dan
kalau belum mengerjakan mastery masih utih warnaya kalau sudah dikejakan oke dan
baut seperti duo linggo 3d nya dan warna nya oke"
Referensi: screenshot di folder ini + riset Duolingo
(`workspace/research_notes/duolingo-ui-algoritma-20261113/report.md`) + brief
polish (`workspace/research_notes/cpns-polish-duolingo-20261113/report.md`).*

## Screenshot di folder ini

- `duolingo-node-popover-review.png` — duolingo.com/learn: node centang hijau
  (selesai), node trofi hijau (unit review), popover hijau "Unit 1 review —
  Earn Legendary on every level to unlock the final trophy!" + tombol kuning
  "GO TO LEGENDARY"; di bawahnya node-node ungu-abu (belum dikerjakan /
  terkunci). Lingkaran-lingkaran memiliki efek 3D (lip bawah lebih gelap,
  highlight atas).

## Perubahan (3 item)

1. **Desain lingkaran (node) disamakan dengan Duolingo.** Lingkaran node jalur
   (70px, sudah disepakati) dibuat dengan efek 3D Duolingo: lip bawah
   (bayangan warna lebih gelap dari warna node, ~4–6px) + highlight atas yang
   lembut, sehingga lingkaran terlihat memiliki kedalaman seperti tombol 3D
   Duolingo; saat ditekan, lip terkompresi (efek tekan). Ikon di dalam
   lingkaran (centang, trofi, bintang, gembok, mahkota) digambar dengan gaya
   Duolingo — glyph putih tebal, terpusat, proporsi sama dengan referensi.
   JANGAN pakai file aset/gambar milik Duolingo; yang ditiru adalah gaya,
   proporsi, dan efeknya, digambar ulang dengan implementasi sendiri.
2. **Warna node mengikuti mastery (status pengerjaan) — aturan tegas.** Belum
   dikerjakan = PUTIH/ABU-ABU (tidak berwarna, seperti node terkunci/belum
   dikerjakan di Duolingo — di mode gelap, abu-abu lembut Duolingo). Sudah
   dikerjakan = BERWARNA (hijau Duolingo #58CC02 dengan ikon putih; mahkota
   emas untuk skor sempurna bila pembedaan itu sudah ada). Sesi hari ini
   (saat ini) = hijau dengan bintang + denyut + gelembung MULAI. Node
   TERLEWAT tetap merah #E05252 (sudah disepakati). Node terkunci/masa depan
   = abu-abu. Pembedaan belum-dikerjakan vs sudah-dikerjakan harus tegas dan
   langsung terlihat.
3. **Warna dan efek disamakan dengan Duolingo.** Hijau node = hijau Duolingo
   #58CC02 dengan lip hijau gelap; abu-abu node belum dikerjakan = abu-abu
   Duolingo mode gelap; merah TERLEWAT = #E05252 (sudah disepakati); efek 3D
   konsisten di semua node dan tombol terkait.

## Batasan (tidak boleh dilanggar)

- Ukuran node tetap 70×70px (sudah disepakati di polish). Zigzag simetris
  ±64px tetap. Judul node 14px tetap. Panel kanan sticky, sidebar fixed,
  banner, dan popover tidak berubah.
- Token Duolingo yang sudah ada saja; Hallmark Floor (tanpa gradien
  ungu-biru, tanpa card-in-card, tanpa ikon emoji, tanpa metrik karangan).
- Jangan sentuh data dan perilaku: 714 soal, 29 sesi, streak, Elo, FSRS-6,
  draf sesi, pintasan keyboard. Placeholder simulasi (0 soal) tetap.
- Jangan pakai aset/brand Duolingo (logo, burung, file gambar milik Duolingo).
  Yang ditiru pola, warna, dan efeknya.
- Popover "Unit review / Legendary" di screenshot HANYA referensi untuk
  lingkaran — jangan ubah popover node yang sudah ada.

## Kriteria selesai (cara memeriksa)

- Capture DESKTOP (≥1280px) + MOBILE 390px: lingkaran node terlihat 3D ala
  Duolingo (lip bawah gelap + highlight atas); node belum dikerjakan berwarna
  putih/abu-abu, node sudah dikerjakan berwarna hijau; ikon putih tebal
  terpusat; node TERLEWAT merah #E05252.
- Audit lulus: 0 console error, 0 overflow di kedua ukuran.
- Data utuh: 29 sesi, 714 soal, attempt 1, streak 7, XP 155, Elo 1500.
- Attestasi membandingkan BEFORE vs sesudah dan menyatakan perubahan di atas
  hadir.

## Non-goal

- Tidak ada sesi/soal/fitur baru (tanpa mode Legendary baru). Tidak ada
  perubahan tema, layout, banner, atau popover.
