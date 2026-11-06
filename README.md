# Kas Keluarga

Aplikasi web untuk memantau keuangan rumah tangga: pemasukan, pengeluaran harian dan bulanan, anggaran, tujuan tabungan, dasbor, dan indikator kesehatan keuangan. Bisa dipasang di ponsel seperti aplikasi (PWA) dan jalan tanpa internet.

## Penyimpanan data
- Data **hanya tersimpan di perangkat pengguna** (localStorage + salinan IndexedDB + salinan harian otomatis). Tidak ada server, akun, atau pelacakan.
- Tulis ganda dengan verifikasi baca-ulang, disimpan segera saat halaman ditutup, dan digabung otomatis bila beberapa tab terbuka.
- Bila data peramban terhapus sebagian, aplikasi memulihkan dari salinan lain. Pengingat cadangan muncul berkala; ekspor JSON/CSV tersedia di Pengaturan.
- Catatan iOS: pasang ke Layar Utama (Bagikan, lalu Tambah ke Layar Utama) agar data tidak dibersihkan Safari bila lama tidak dibuka.

## Menjalankan
Berkas statis murni, tanpa build. Buka lewat server statis apa pun (mis. `python3 -m http.server`) atau GitHub Pages. Service worker butuh HTTPS atau localhost.

## Berkas
`index.html` (seluruh aplikasi), `manifest.webmanifest`, `sw.js`, `icons/`.
