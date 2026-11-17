# Referensi Duolingo — UI, Algoritma, Arsitektur (untuk edit UI aplikasi CPNS)

**Tanggal:** 13 November 2026
**Sumber:** pencarian web publik — design docs, paper riset yang dipublikasikan, repo clone open-source.
**Catatan penting:** Duolingo adalah closed source — tidak ada kode proprietary untuk di-reverse-engineer. Referensi yang dipakai: design system publik, paper riset, dan clone open-source berlisensi.

## 1. Design tokens (terverifikasi dari 3 sumber independen)

| Token | Hex | Peran |
|---|---|---|
| Green | `#58CC02` | Primary brand, CTA, jawaban benar |
| Green deep / lip | `#58A700` | Bayangan bawah tombol (4px bottom lip) |
| Green soft | `#D7FFB8` | Highlight / success tint |
| Blue | `#1CB0F6` | Secondary action, aksen XP/progress |
| Streak orange | `#FF9600` | Api streak (deep `#CC7A00`) |
| Gem yellow | `#FFC800` | Gem counter |
| Gem purple | `#CE82FF` | Reward / streak support |
| Red | `#FF4B4B` | Salah / warning / hati hilang |
| Ink | `#4B4B4B` | Teks utama |
| Border | `#E5E5E5` | Outline kartu |
| Surface | `#F7F7F7` | Background sekunder / kartu terkunci |
| Canvas | `#FFFFFF` | Background utama |

- **Tombol:** tinggi 50px, radius 12px, fill hijau + lip bawah 4px `#58A700` (box-shadow 0 4px 0); saat ditekan lip-nya collapse (efek 3D mainan). Label putih uppercase 15px/700, tracking 0.8px.
- **Tipografi:** Feather Bold (display/headline — BERLISENSI, jangan embed file font aslinya; alternatif gratis: **Varela Round**). Body: DIN Next Rounded Pro → pakai rounded sans sistem (atau Mona Sans/Inter sebagai fallback).
- **Bentuk:** semua membulat — kartu 16–24px, tile jawaban 12px, node skill lingkaran penuh, pill button 9999px. Spacing base 4px.

## 2. Lesson path / roadmap (pola Duolingo asli)

- Jalur vertikal **berliku sinusoidal** (bukan garis lurus), kolom ~320px, di tengah layar.
- Node skill 80×72px, lingkaran, dengan **4 state**: `LOCKED` (abu-abu, gembok) / `AVAILABLE` (aktif, hijau) / `IN_PROGRESS` (cincin progres radial) / `COMPLETED` (mahkota/crown emas).
- Node aktif: animasi pulse 1.0 → 1.05 tiap 1.6 detik; gelembung `START` mengambang; popover saat diklik (XP reward, tombol mulai).
- Unit banner di atas tiap bagian dengan palet warna berotasi.
- **Top bar selalu terlihat:** api streak + angka, gem, hati, XP ring, bendera course.
- **Daily goal ring:** cincin api yang terisi dari XP hari ini, berubah emas saat target harian tercapai.
- Maskot muncul di onboarding, error, dan perayaan streak.

**Aturan warna roadmap aplikasi kita (perintah Sandi, 13 Nov):** hari yang BELUM dikerjakan = MERAH, bukan hijau. Hijau hanya untuk yang sudah selesai. (Menyimpang dari konvensi Duolingo asli yang memakai abu-abu untuk terkunci — ini pilihan Sandi.)

## 3. Streak — aturan acuan (dari clone open-source + perilaku Duolingo)

- Streak naik **maksimal 1× per hari kalender**, saat lesson selesai.
- Hari yang sama = no-op (tidak naik lagi). Hari berikutnya = +1. Jeda lebih dari 1 hari = reset ke 1 (kecuali streak freeze dipakai).
- **Backend bersifat otoritatif:** client tidak pernah memutuskan benar/salah jawaban, XP, hati, streak, atau unlock — semua dihitung dan disimpan server-side dalam transaksi database.

## 4. Algoritma spaced repetition — HLR vs FSRS

- **Duolingo memakai Half-Life Regression (HLR)** — Settles & Meeder 2016, "A Trainable Spaced Repetition Model for Language Learning" (ACL 2016): `p = 2^(−Δ/h)`, `ĥ(x) = 2^(θ·x)`. Diuji operasional: engagement harian +12%. Revisi 2026 (Ilídio dkk., PMLR 339): mixed-effects HLR + Random Forest.
- **Aplikasi kita sudah memakai FSRS-6** di buku kesalahan — itu algoritma spaced repetition modern yang direkomendasikan sumber-sumber 2026 di atas SM-2 dan setara/lebih baru dari HLR Duolingo. **Keputusan: PERTAHANKAN FSRS-6, jangan downgrade ke HLR.** Yang diperbaiki adalah UI/UX dan bug streak/roadmap, bukan algoritmanya.

## 5. Arsitektur clone open-source (referensi stack)

- TheAyushTandon/Duolingo-clone: Next.js 16 + TypeScript + Tailwind v4 + FastAPI + SQLAlchemy 2.0 + Pydantic; backend otoritatif; sinusoidal path; 4 node state.
- sanjuvemula/duolingo-clone: Next.js 16 + FastAPI + SQLite; aturan streak seperti §3.
- LibreLingo: AGPL-3.0, Python + Svelte, self-hosted, course via YAML.

## 6. Backend/VPS — status aplikasi kita

- Aplikasi CPNS **sudah punya backend + database** (runtime artifact fullstack): semua attempt, skor, streak, error book, dan FSRS dihitung server-side dan tersimpan (data: 29 sesi / 714 soal).
- Yang diminta Sandi ("backend + database cepat di VPS dengan Docker/Redis") adalah **migrasi ke stack self-hosted**, bukan penambahan. Skala saat ini (1 user, 714 soal, beberapa request/hari) tidak akan terasa lebih cepat dengan Redis/Docker — dan VPS menambah beban maintenance + mode gagal baru (VM diganti deployment → proses mati kecuali ada systemd).
- Jika tetap dimau: rencana = **Go** (bahasa yang sedang dipelajari Sandi; cepat, single binary) + **PostgreSQL** (data) + **Redis** (cache/sesi) + **Docker Compose**, dengan unit systemd untuk recovery. Keputusan menunggu konfirmasi Sandi setelah bug + UI selesai.
