# SIRUSAK — Sistem Informasi Rumah Sakit Berbasis Web

[![PHP](https://img.shields.io/badge/PHP-7.4%20%7C%208.x-blue.svg)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-Database-orange.svg)](https://www.mysql.com/)
[![TCPDF](https://img.shields.io/badge/TCPDF-PDF%20Report-red.svg)](https://tcpdf.org/)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)]()

**SIRUSAK (Sistem Informasi Rumah Sakit)** adalah platform manajemen pelayanan rumah sakit berbasis web yang dirancang untuk mengotomasi alur operasional medis secara terintegrasi, mulai dari pendaftaran pasien di *front-office*, rekam medis dan pemeriksaan dokter, hingga tata kelola poliklinik/departemen dan pencetakan laporan rekam medis secara terpadu.

Proyek ini dikembangkan oleh **Firstyatama Auzan Farhadi** (NIM: 1203220009) dalam mata kuliah Penjaminan Mutu Perangkat Lunak (PMPL) di **Universitas Telkom Surabaya**, dilengkapi dengan dokumen pengujian formal **PDHUPL (Penetapan & Dokumentasi Hasil Uji Perangkat Lunak)**.

---

## 🏥 Fitur & Modul Utama

### 1. Modul Front-Office
- Registrasi dan manajemen data pasien baru maupun pasien lama.
- Penjadwalan antrean konsultasi rawat jalan dan alokasi ke poliklinik tujuan.
- Pencarian dan filter data registrasi pasien dengan cepat.

### 2. Modul Dokter & Rekam Medis
- Akses daftar antrean pasien terdaftar per dokter spesialis.
- Pencatatan keluhan pasien, diagnosis medis klinis, dan riwayat rekam medis pasien.
- Input data resep obat dan tindakan medis.

### 3. Modul Poliklinik & Departemen
- Manajemen data departemen / poliklinik (Poli Umum, Gigi, Anak, dsb.).
- Pemetaan jadwal dinas dokter terhadap poliklinik terkait.

### 4. Pelaporan Otomatis (PDF Reporting)
- Cetak kartu periksa pasien dan laporan resume rekam medis menggunakan library **TCPDF**.

---

## 🗄️ Basis Data Relasional
Skema basis data relasional dikelola menggunakan MySQL (`rumah_sakit.sql`), mencakup tabel:
- Data Master Pasien
- Data Dokter & Jadwal Praktik
- Poliklinik / Departemen
- Transaksi Pemeriksaan Medis
- Rekam Diagnosa & Resep

---

## 🧪 Dokumentasi & Pengujian Mutu (PMPL)
Proyek ini mengimplementasikan kaidah rekayasa perangkat lunak dan penjaminan mutu yang terdokumentasi lengkap dalam:
👉 **[PDHUPL UAS PMPL.pdf](PDHUPL%20UAS%20PMPL.pdf)**  
Mencakup pengujian fungsional *black-box testing*, *boundary value analysis*, dan pengujian alur navigasi pengguna.

---

## 🚀 Panduan Instalasi Lokal

### 1. Kloning Repositori
```bash
git clone https://github.com/FirstyatamaAuzan/sirusak.git
```

### 2. Pindahkan ke Web Server Lokal
Pindahkan folder proyek ke dalam direktori web server lokal:
- **XAMPP**: `C:/xampp/htdocs/sirusak`
- **Laragon**: `C:/laragon/www/sirusak`

### 3. Impor Basis Data
1. Buka browser dan akses `http://localhost/phpmyadmin`
2. Buat database baru bernama `rumah_sakit`
3. Impor berkas `rumah_sakit.sql` ke dalam database tersebut

### 4. Konfigurasi Koneksi
Periksa berkas `konfig.php` dan sesuaikan kredensial basis data:
```php
<?php
$host = "localhost";
$user = "root";
$pass = "";
$db   = "rumah_sakit";
$konek = mysqli_connect($host, $user, $pass, $db);
?>
```

### 5. Jalankan Aplikasi
Buka peramban (browser) dan akses:
`http://localhost/sirusak/index.php`

---

## 👤 Pengembang
**Firstyatama Auzan Farhadi**  
- LinkedIn: [linkedin.com/in/firstyatama](https://www.linkedin.com/in/firstyatama/)  
- GitHub: [@FirstyatamaAuzan](https://github.com/FirstyatamaAuzan)  
- S1 Informatika, Universitas Telkom Surabaya
