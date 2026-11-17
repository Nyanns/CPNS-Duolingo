# Brief — Fase 1 Algoritma Duolingo (Aplikasi Duolingo CPNS)

**Tanggal:** 13 November 2026
**Artifact:** duolingo-cpns-latihan-soal-interaktif
**Sumber riset:** `~/workspace/research_notes/duolingo-algoritma-20261113/report.md` (baca dulu — pemetaan 14 item, jawaban FSRS-6 vs HLR dan Birdbrain vs Elo, urutan Fase 1/2, 5 gap verifikasi)

## Verbatim request (kata-kata Sandi)

- "maintance app ini terus ya mom algoritmanya samakn dgn algorima duolinggo" (13 Nov 16:16)
- Persetujuan: "Jalankan Fase 1" (13 Nov 16:36, lewat pilihan pada usulan Mommy) — Fase 1 = (1) Birdbrain-lite, (2) strength meter per topik, (3) daily goal bisa diatur + cincin emas, (4) milestone streak 7/30/100, (5) monthly quest + badge + quest "5 benar beruntun".

## Outcome (apa yang berubah untuk Sandi)

- Aplikasi makin terasa seperti Duolingo di sisi algoritma: soal diurutkan dari mudah ke sulit berdasarkan prediksi kemampuan (bukan urutan tetap), tiap topik punya "kekuatan" yang meluruh dan bisa "retak" lalu diperbaiki, target harian bisa ia atur sendiri, streak 7 harinya dirayakan, dan ada quest bulanan + badge.
- TIDAK ada perubahan soal, kunci, atau skor historis. TIDAK ada perubahan tampilan besar — ini pekerjaan algoritma + mekanik, bukan redesign.

## User / audiens

Sandi, satu-satunya pengguna. Sesi harian jam 10:00 WIB; simulasi penuh Sabtu 14 Nov 10:00 (110 soal/100 menit) — pekerjaan ini TIDAK BOLEH mengganggu simulasi: jangan ubah isi sesi, jangan ubah placeholder simulasi, jangan ubah skor/attempt yang ada.

## Constraints (keras)

- FSRS-6 TETAP — jangan ganti ke HLR Duolingo (keputusan riset: FSRS-6 log loss 0,3460 vs HLR 0,4694; downgrade dilarang).
- Elo TETAP sebagai mesin ability/difficulty — yang ditambah adalah cara pakainya (Birdbrain-lite), bukan mesin baru. JANGAN bangun LSTM 40-dim (Birdbrain V2) — 1 user, 714 soal, overfit.
- JANGAN mengarang lawan: tidak ada liga multiplayer palsu, tidak ada nama/pesaing fiktif. Solo ladder adalah Fase 2, bukan Fase 1.
- JANGAN hearts (friksi monetisasi) — tidak ada di Fase 1 maupun seterusnya.
- Urutan soal simulasi (TWK→TIU→TKP, 110 soal) TIDAK BOLEH diacak/diurutkan ulang oleh P(correct) — simulasi memakai urutan ujian. P(correct) ordering hanya untuk sesi latihan dan antrean error-book.
- Tema default tetap gelap navy #131F24; node 70×70 dengan lip 3D 6px + warna mastery (belum putih/abu, sudah hijau #58CC02, sempurna mahkota emas, TERLEWAT #E05252) tetap; right rail desktop tetap sticky; banner Duolingo-style + popover node tetap; mascot (Mommy membaca buku) tetap; ResultView/payoff tetap; isi tab Materi (termasuk Cheat Sheet A–F) tetap.
- Data HARUS utuh: 29 sesi / 714 soal, attempt 1 (verifikasi Mommy, BUKAN skor Sandi), streak 7, XP 155, Elo 1500, error book aktif 2 / due 2, score_history 8. Jangan reset/menimpa apa pun.

## Verifikasi dulu — 5 gap (jawab dari kode, bukan asumsi; laporkan hasilnya)

1. Apakah Elo soal ikut bergerak setelah attempt? Berapa K-factor item vs K-factor pengguna?
2. Apakah target daily goal sudah bisa diatur pengguna?
3. Apa yang dilakukan tombol "Ronde Legendary" di popover node? (provenance belum terverifikasi — JANGAN ubah perilakunya di Fase 1, verifikasi saja.)
4. Apakah XP tampil langsung di layar payoff?
5. Apakah FSRS-6 memakai parameter default atau sudah dioptimasi per-user?

## Scope Fase 1 (5 item)

1. **Birdbrain-lite**
   - Pastikan update Elo dua sisi: ability pengguna DAN difficulty soal bergerak setiap jawaban (bila Elo soal belum bergerak, tambahkan update item dengan K lebih kecil dari K pengguna).
   - Hitung P(correct) = 1 / (1 + 10^(-(ability − difficulty)/400)) per soal.
   - Pakai P(correct) untuk mengurutkan soal di dalam sesi (mudah → sulit, momentum dulu) dan mengurutkan antrean error-book. Sesi harian TETAP cakupannya (jangan ubah sesi harian jadi adaptif penuh — itu Fase 2).
2. **Strength meter per topik (prioritas tertinggi)**
   - Rata-ratakan FSRS Retrievability per topik menjadi batang kekuatan yang meluruh seiring waktu.
   - Tandai topik "retak" bila R jatuh di bawah ambang (awal: R < 0,70 — ambang hipotesis, sesuaikan dari data; jangan klaim sebagai angka Duolingo).
   - Tambahkan ajakan perbaikan (latihan topik yang retak) — memakai data yang sudah ada, tanpa model baru.
3. **Daily goal bisa diatur + cincin emas**
   - Bila belum bisa diatur: jadikan pilihan (mis. 20/50/100 XP); cincin goal berubah emas saat tercapai.
   - XP dari review FSRS tetap dihitung ke daily goal (seperti Duolingo).
4. **Milestone streak 7/30/100 + perayaan**
   - Perayaan milestone saat tercapai. Streak saat ini 7 — milestone 7 hari relevan sekarang; rayakan dengan benar (jangan picu perayaan palsu/berulang untuk milestone yang sama).
5. **Monthly quest + badge + quest "5 benar beruntun"**
   - Quest bulanan (mis. selesaikan 30 quest dalam sebulan) + badge.
   - Quest "5 benar beruntun" (counter runtun jawaban benar dalam satu sesi).
   - Quest harian yang sudah ada (4 quest, reset harian) jangan diubah.

## Done-criteria (bagaimana kita tahu ini berhasil)

- 5 gap di atas terjawab dengan bukti dari kode dan dilaporkan.
- P(correct) dihitung dan TERLIHAT dipakai: urutan soal dalam sesi mengikuti mudah → sulit; antrean error-book terurut oleh P(correct).
- Strength meter per topik terlihat (batang + status retak + ajakan perbaikan).
- Daily goal bisa dipilih (20/50/100 XP) dan cincin jadi emas saat tercapai.
- Milestone streak 7/30/100 ada + perayaan muncul saat tercapai (tanpa duplikasi).
- Monthly quest + badge + quest "5 benar beruntun" ada dan berfungsi.
- Data utuh (29 sesi / 714 soal / attempt 1 / streak 7 / XP 155 / Elo 1500 / error book 2 aktif).
- Audit lolos: 0 console error, 0 overflow di desktop 1440 dan mobile 390; semua state UI sebelumnya utuh (node, banner, popover, sticky rail, tema gelap).

## Non-goals (JANGAN dikerjakan di Fase 1)

- Fase 2: solo league ladder, mode latihan adaptif penuh, response-time logging, evaluasi FSRS-7.
- Jangan pernah: HLR, hearts, liga multiplayer palsu, notifikasi bandit, LSTM Birdbrain V2.
- Jangan ubah perilaku tombol "Ronde Legendary" (verifikasi saja).
- Jangan ubah isi sesi harian, bank soal, kunci, skor historis, placeholder simulasi, atau tab Materi.

## Risks / unknowns

- K-factor item Elo belum diketahui sampai kode dibaca.
- Konfigurabilitas daily goal belum diketahui.
- Perilaku "Ronde Legendary" belum diketahui (provenance belum terverifikasi).
- Tampilan XP di payoff belum diketahui.
- Parameter FSRS-6 (default vs per-user) belum diketahui.
- Streak 7 saat ini: perayaan milestone 7 harus tepat sasaran, tidak berulang.
