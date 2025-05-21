 Penilaian Sumatif Akhir Tahun (PSAT) 2024/2025

  Fitur Utama

Dashboard: Menampilkan data yang telah diinput dalam bentuk tabel.
Input Data: Formulir untuk menambahkan data baru ke dalam database.
Edit Data: Memungkinkan pengguna untuk mengubah data yang sudah ada.
Hapus Data: Menghapus data yang tidak diperlukan.
Autentikasi Sederhana: Login dengan username dan password default.
Penggunaan File `.env`: Menyimpan konfigurasi database secara terpisah untuk keamanan dan kemudahan pengelolaan.

Struktur Direktori

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

Persiapan dan Instalasi

1. Buat File `.env`

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

2.Gunakan AWS
-Masuk ke Aurora&RDS
-Masuk ke Database lalu create database
-Engine Type : pilih MySQL
-Templates : Free tier

-DB cluster identifier : (Nama bebas)

-Master Username : (biarkan admin)
-Master Password : (password terserah anda)
-Public access : No
-Security group pastikan buat/pilih yang accept port inbound 3306 dari 0.0.0.0/0
-Lalu klik create database
-Didatabase klik nama database anda lalu lihat di connectivity & Security,tunggu sampai endpoint muncul

3.Masuk ke EC2 Lalu instance
-Launch instance
-Nama instance(terserah anda)
-Application : Ubuntu
-Instance type : t2micro atau t2nano
-Keypair : vockey
-Security groups : SSH, HTTP, HTTPS, anywhere 0.0.0.0/0
-Advance detail lalu scroll kebawah klik di user data
-Isi user data dengan perintah deploy
-Lalu instance

4.Perintah Deploy
sudo apt update -y

sudo apt install -y apache2 php php-mysql libapache2-mod-php mysql-client

sudo rm -rf /var/www/html/{*,.*}

sudo git clone (alamat repository anda) /var/www/html

sudo chmod -R 777 /var/www/html

echo DB_USER=(nama user) > /var/www/html/.env
echo DB_PASS=(password database anda)  >> /var/www/html/.env
echo DB_NAME=(nama databasae anda)  >> /var/www/html/.env
echo DB_HOST=(endpoint anda) >> /var/www/html/.env

5 Jalankan Aplikasi

Buka file `index.php` di browser Anda. Masuk menggunakan kredensial berikut:

Username: `admin`
Password: `123`