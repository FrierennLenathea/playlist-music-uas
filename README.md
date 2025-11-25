Tugas uas project playlist music :))

🎵 Music Playlist App
Aplikasi web untuk mengelola playlist musik pribadi dengan fitur lengkap:
✅ Login
✅ Cari lagu
✅ Putar lagu dengan simpan progress
✅ Buat & kelola playlist
✅ Drag & drop untuk atur urutan lagu
✅ Hapus lagu/playlist

Dibangun dengan frontend-only (React + Vite via CDN) + backend Express.js sederhana.
Tidak perlu npm di frontend! Cukup buka file HTML di browser.

📁 Struktur Project
123456
music-playlist/
├── backend/              # Server Express.js (Node.js)
│   └── server.js
├── frontend/             # Frontend (1 file HTML)
│   └── index.html
└── README.md             # Kamu di sini!

🚀 Cara Menjalankan
1. Jalankan Backend (Express.js)
Pastikan kamu sudah menginstall Node.js (LTS).

bash
123456789
# Masuk ke folder backend
cd backend

# Install dependensi (sekali saja)
npm init -y
npm install express cors

# Jalankan server
node server.js
✅ Server akan jalan di: http://localhost:5000
✅ Data dummy tersedia:

Email: user@gmail.com
Password: 123456
2. Jalankan Frontend
Tidak perlu install apa-apa!
Cukup buka file HTML di browser.

Buka file: frontend/index.html
Klik 2x atau buka via VS Code → Live Server
Login dengan akun di atas
Nikmati aplikasi!

✨ Fitur
Fitur
Deskripsi

🔐 Login
Autentikasi sederhana (data dummy)

🔍 Cari Lagu
Cari berdasarkan judul atau artis

▶️ Putar Lagu
Audio player bawaan browser

💾 Simpan Progress
Otomatis lanjut dari posisi terakhir (disimpan di localStorage)

➕ Buat Playlist
Tambah playlist baru via tombol

🖱️ Drag & Drop
Atur ulang urutan lagu di playlist dengan seret-seret

❌ Hapus
Hapus lagu dari playlist atau hapus seluruh playlist

🛠️ Teknologi
Frontend:
React (via CDN)
Tailwind CSS (via CDN)
Babel Standalone (untuk JSX)
localStorage untuk simpan progress & token
Backend:
Node.js + Express.js
CORS enabled
Data sementara (array JavaScript) — bisa dikembangkan ke MySQL

🔒 API Endpoints (Backend)
Method
Endpoint
Fungsi
POST
/api/auth/login
Login
GET
/api/songs
Ambil semua lagu
GET
/api/playlists
Ambil playlist user
POST
/api/playlists
Buat playlist baru
POST
/api/playlists/:id/songs
Tambah lagu ke playlist
DELETE
/api/playlists/:id
Hapus playlist
DELETE
/api/playlists/:id/songs/:songId
Hapus lagu dari playlist
PUT
/api/playlists/:id/order
Update urutan lagu (drag & drop)

💡 Catatan Pengembangan
Data disimpan di memori → restart server = data hilang
(Untuk produksi, ganti ke database seperti MySQL/PostgreSQL)
Progress lagu disimpan di localStorage → hanya berlaku per device & browser
Tidak ada validasi kompleks → untuk demo & pembelajaran
CORS sudah diaktifkan → frontend bisa akses dari file:// atau http://localhost

🙌 Dibuat Untuk
Developer yang ingin frontend tanpa ribet npm
Demo aplikasi music sederhana
Belajar integrasi React + Express.js
Prototipe cepat dengan fitur drag & drop + audio
