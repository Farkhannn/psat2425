# Penilaian Sumatif Akhir Tahun (PSAT) 2024/2025

## 📌 Deskripsi Proyek

Repositori ini berisi aplikasi berbasis web yang dikembangkan sebagai bagian dari Penilaian Sumatif Akhir Tahun (PSAT) untuk mata pelajaran DevOps kelas XI TJKT 1 di SMKN 1 Banyumas pada Tahun Ajaran 2024/2025. Aplikasi ini dirancang untuk mengelola data dengan fitur CRUD (Create, Read, Update, Delete) sederhana menggunakan PHP dan MySQL, serta dihosting di layanan cloud AWS RDS.

## 🧰 Fitur Utama

- **Dashboard**: Menampilkan data yang telah diinput dalam bentuk tabel.
- **Input Data**: Formulir untuk menambahkan data baru ke dalam database.
- **Edit Data**: Memungkinkan pengguna untuk mengubah data yang sudah ada.
- **Hapus Data**: Menghapus data yang tidak diperlukan.
- **Autentikasi Sederhana**: Login dengan username dan password default.
- **Penggunaan File `.env`**: Menyimpan konfigurasi database secara terpisah untuk keamanan dan kemudahan pengelolaan.

## 🗂️ Struktur Direktori

```
├── index.php          # Halaman login utama
├── dashboard.php      # Menampilkan data yang tersimpan
├── input.php          # Menambahkan data baru
├── edit.php           # Mengedit data
├── delete.php         # Menghapus data
├── menu.php           # Navigasi menu
├── logout.php         # Logout dari sesi pengguna
├── db.php             # Koneksi ke database
├── .env               # Konfigurasi database
├── style.css          # Styling aplikasi
├── uploads/           # Folder penyimpanan file upload (jika digunakan)
└── README.md          # Dokumentasi proyek ini
```

## ⚙️ Persiapan dan Instalasi

### 1. Buat File `.env`

Buat file `.env` di direktori utama proyek untuk menyimpan konfigurasi koneksi database:

```env
DB_USER=your_db_username
DB_PASS=your_db_password
DB_NAME=your_db_name
DB_HOST=your_db_host
```

Contoh:

```env
DB_USER=admin
DB_PASS=P4ssw0rd123
DB_NAME=psat2425
DB_HOST=rdsku.czt6n8ylfvyb.us-east-1.rds.amazonaws.com
```

### 2. Jalankan Aplikasi

Buka file `index.php` di browser Anda. Masuk menggunakan kredensial berikut:

- **Username**: `admin`
- **Password**: `123`

> ⚠️ **Catatan:** Ubah username dan password default di `index.php` untuk alasan keamanan.

## 🚀 Deployment

Aplikasi ini dapat dijalankan secara lokal maupun dihosting secara online. Untuk deployment online:

- Hosting harus mendukung PHP dan MySQL.
- File `.env` harus dikonfigurasi sesuai dengan lingkungan hosting.
- Database harus sudah dibuat dan tersedia.

## 👨‍💻 Kontribusi

Proyek ini adalah bagian dari penilaian individu dan tidak dibuka untuk kontribusi umum. Namun, Anda dipersilakan untuk fork dan mengembangkan sendiri aplikasi ini sesuai kebutuhan.

## 📄 Lisensi

Proyek ini dibuat untuk keperluan edukasi dan tidak memiliki lisensi resmi. Silakan gunakan kode dalam repositori ini untuk pembelajaran pribadi.

---

📫 Jika ada pertanyaan atau saran, silakan buat issue di repositori ini.