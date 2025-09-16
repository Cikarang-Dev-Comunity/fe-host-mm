📌 Deskripsi
Service host yang berfungsi sebagai container utama. Bertugas memanggil dan mengorkestrasi seluruh service microfrontend lain, serta menyediakan halaman utama untuk autentikasi user.

⚙️ Tech Stack
- React.js
- Webpack 5 (Module Federation)

🔗 Integrasi
Service ini menjadi entry point dan melakukan load remote module dari:
- fe-notif-mm
- fe-workspace-management-mm
- fe-transaction-mm
- fe-rbac-mm
- fe-dashboard-mm
- fe-report-mm

📝 Catatan
- Harus dijalankan sebelum service lain agar remote entry dapat dipanggil.
- Pastikan semua remoteEntry.js service lain sudah dikonfigurasi di webpack.config.js.
- Kelola autentikasi di sini agar tidak redundant di service lain.

🏗 Arsitektur
- Microfrontend: service host memuat remote frontend lain.
- Microservices: komunikasi ke backend menggunakan API gateway.