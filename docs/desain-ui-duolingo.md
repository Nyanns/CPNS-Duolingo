# Riset UI: Tiru Tampilan Asli Duolingo (Screenshot Sandi, 13 Nov 2026)
Permintaan Sandi (verbatim): "Buat seperi ini ui nya clean oke dan ada pilihan menu seperti app ini biar clean oke jadi tidak kebawah semua"
Referensi visual (ADA DI FOLDER INI — baca kedua file gambar sebelum mendesain):
- `duolingo-home-nyanns.jpg` — layar Beranda aplikasi Duolingo asli (akun Sandi).
- `duolingo-profile-nyanns.jpg` — layar Profil aplikasi Duolingo asli.

## Yang diminta (inti)
Buat UI aplikasi Duolingo CPNS seperti Duolingo asli: CLEAN, dan ada PILIHAN MENU (navigasi bawah/tab) seperti aplikasi ini — supaya konten tidak menumpuk semua ke bawah dalam satu scroll panjang. Beranda hanya menampilkan yang esensial; sisanya pindah ke tab/menu masing-masing.

## Screen 1 — Beranda Duolingo (duolingo-home-nyanns.jpg)
- Tema GELAP: latar belakang navy gelap pekat (#131F24-ish), teks putih/abu terang.
- Top bar: avatar bundar kiri; bendera + angka (129); ikon api streak + angka 0 dengan badge peringatan merah "!"; badge "SUPER" warna-warni kanan.
- Banner hijau terang membulat: baris kecil "13 NOVEMBER" + judul besar "Penyegaran Harian".
- Lesson path berliku (bukan daftar lurus): node-node tersusun zig-zag ke bawah. Node aktif = lingkaran hijau besar berisi ikon (dumbbell) + balon ucapan "MULAI" di atasnya. Node terkunci = lingkaran abu-abu gelap berisi ikon gembok. Di tengah path ada maskot (burung hantu hijau membaca buku di atas tumpukan buku). Badge karakter kecil "9 hari" dengan gambar penyihir di kiri atas path.
- Bottom navigation bar (5–6 ikon): Beranda (aktif, diberi kotak sorot), Liga/buku, trofi, hati, dll + tombol "..." (menu lainnya). Inilah pola menu yang diminta.

## Screen 2 — Profil Duolingo (duolingo-profile-nyanns.jpg)
- Header berwarna (salmon/merah muda) dengan tombol X kiri dan ikon gir (pengaturan) kanan.
- Nama tampilan besar "nyanns" + subteks "Super sejak 2026", avatar ilustrasi besar di tengah header, badge SUPER.
- Baris identitas: "@NYANSKUY · BERGABUNG SEJAK 2019".
- Statistik 3 kolom: Kursus (+6), Mengikuti (8), Pengikut (1).
- Tombol besar "TAMBAHKAN TEMAN" + tombol QR di kanan.
- Kartu promo ungu: "Dapatkan kostum baru!" + "9 HARI" + tombol "LIHAT DEH".
- Bagian "RINGKASAN" (grid 2 kolom): streak 0 hari, angka 129, liga Obsidian, 6375 XP.

## Rencana penerapan ke aplikasi Duolingo CPNS
1. **Bottom navigation (WAJIB, inti permintaan):** 5 tab — Beranda, Quest, Buku Kesalahan (FSRS), Info CPNS, Profil. Setiap tab layarnya sendiri. TIDAK ADA LAGI satu halaman beranda yang berisi semuanya (quest + FSRS + mastery + briefing + dashboard menumpuk ke bawah).
2. **Beranda = hanya ini:** top bar (avatar Mommy, streak + freeze, XP), banner hijau "tanggal + sesi hari ini" (contoh: "13 NOVEMBER / Hari 8 — TIU Figural"), lesson path berliku (node Hari 1→8 → HOTS → Simulasi; aktif = hijau + balon "MULAI"; selesai = centang; terkunci = gembok), dan bottom nav. Maskot di tengah path: Lumiina/Hoshi (bukan burung hantu Duolingo).
3. **Tab Quest:** panel Daily Quests (4 misi, bar tipis, hadiah XP, countdown reset 10:00) + streak strip 7 hari + freeze.
4. **Tab Buku Kesalahan:** antrean FSRS jatuh tempo + rating Lupa/Sulit/Lumayan/Mudah + chip D/S/R + mastery per topik.
5. **Tab Info CPNS:** kotak briefing terbaru + sumber resmi + kuis cek info.
6. **Tab Profil:** tiru struktur profil Duolingo: header berwarna + nama "Sandi" + statistik (streak, XP total, liga/rank dari Elo, sesi selesai) + ringkasan (TWK/TIU/TKP vs target 90/110/185, prediksi skor) + tombol pengaturan (mode nilai langsung on/off, mode gelap/terang).
7. **Tema:** gelap ala Duolingo (navy gelap, hijau #58CC02 sebagai warna aksi utama, amber untuk streak, ungu untuk kartu promo) — ganti palet slate-teal saat ini. Tetap ada mode terang sebagai opsi di Profil.
8. **Perilaku saat sesi dibuka:** layar soal tetap fokus satu soal per layar (seperti sekarang); setelah selesai → layar payoff (XP, akurasi, waktu, streak) lalu kembali ke path.

## Batasan (jangan dilanggar)
- Data TIDAK BOLEH hilang: 12 sesi / 261 soal, riwayat skor (attempt Hari 8 155/160 adalah verifikasi Mommy, BUKAN skor Sandi), buku kesalahan FSRS (3 jatuh tempo), briefing CPNS 12 Nov, quest, streak 7 + freeze 1, Elo 1500, mastery.
- Tetap: bahasa Indonesia; target TWK 90 / TIU 110 / TKP 185; PG TWK 65 / TIU 80 / TKP 166; soal HOTS tetap sulit; cron cpns-daily-practice + updater harian aplikasi (applyDailyUpdate) + aksi addSession tetap berfungsi.
- Jangan meniru aset berhak cipta Duolingo (maskot burung hantu, logo, nama) — tiru TATA LETAK dan POLANYA saja; maskot kita Lumiina/Hoshi, nama aplikasi tetap "Duolingo CPNS".
- Verifikasi seperti edit sebelumnya: audit lulus tanpa error konsol, probe HP + desktop, dan pastikan SEMUA tab bisa dibuka dari bottom nav (uji klik tiap tab — ini inti permintaan, jangan sampai ada tab mati).
