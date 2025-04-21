Tentu! Berikut adalah `README.md` lengkap dengan konfigurasi dan cara menjalankan aplikasi **Absensi Karyawan HRD** berbasis **CodeIgniter 3**.

```markdown
# Aplikasi Absensi Karyawan - HRD

## Deskripsi

**Aplikasi Absensi Karyawan** adalah aplikasi berbasis web yang dikembangkan untuk membantu HRD dalam memantau dan mengelola absensi karyawan. Aplikasi ini memungkinkan HRD untuk melihat, menambah, mengedit, dan menghapus data absensi karyawan. Karyawan dapat mencatat absensi mereka berdasarkan tanggal, jenis cuti, alasan ketidakhadiran (misalnya Sakit, Izin, Cuti, Alpa, atau Telat), dan durasi absensi.

Aplikasi ini dibangun menggunakan **CodeIgniter 3**, sebuah framework PHP yang efisien dan mudah digunakan untuk pengembangan aplikasi web.

---

## Fitur

- **Manajemen Absensi Karyawan**: HRD dapat mengelola semua data absensi karyawan, termasuk menambah, mengedit, dan menghapus absensi.
- **Jenis Absensi dan Cuti**: Karyawan dapat memilih jenis absensi seperti Sakit, Izin, Cuti, Alpa, atau Telat.
- **Pelaporan Absensi**: HRD dapat melihat laporan terkait absensi, termasuk jumlah hari cuti, sakit, atau ketidakhadiran lainnya.
- **Pengelolaan Data Karyawan**: Menyimpan data absensi beserta alasan dan durasi ketidakhadiran karyawan.
- **Autentikasi dan Keamanan**: Hanya HRD yang dapat mengakses dan mengelola data absensi.

---

## Struktur Database

Aplikasi ini menggunakan database dengan beberapa tabel yang berfungsi untuk menyimpan data absensi karyawan. Berikut adalah tabel `absensi` yang utama:

### Tabel: `absensi`

| Nama Kolom            | Tipe Data         | Deskripsi                                      |
|-----------------------|-------------------|------------------------------------------------|
| `id_absen`            | `int(11)`         | ID unik untuk setiap catatan absensi.          |
| `nik_karyawan_absen`  | `varchar(16)`      | ID Karyawan yang terkait dengan absensi.      |
| `tanggal_absen`       | `date`            | Tanggal absensi yang dicatat.                 |
| `tanggal_selesai`     | `date`            | Tanggal berakhirnya cuti atau absensi.        |
| `keterangan_absen`    | `enum`            | Jenis absensi: Sakit, Izin, Cuti, Alpa, Telat. |
| `lama_absen`          | `varchar(10)`      | Durasi absensi (dalam jam atau hari).          |
| `keterangan`          | `varchar(50)`      | Catatan tambahan mengenai absensi.             |
| `jenis_cuti`          | `enum`            | Jenis cuti, jika berlaku.                     |

---

## Cara Instalasi

Ikuti langkah-langkah berikut untuk menginstal dan menjalankan aplikasi **Absensi Karyawan** ini di server lokal Anda.

### 1. Clone Repositori

Clone repositori ini ke dalam folder lokal Anda menggunakan Git:

```bash
git clone https://github.com/username/absensi-hrd.git
```

### 2. Instalasi Dependensi

Pastikan Anda sudah menginstal **PHP** dan **MySQL** di mesin lokal Anda. Aplikasi ini dibangun menggunakan **CodeIgniter 3**, yang memerlukan PHP versi 5.6 ke atas. Anda juga perlu memastikan bahwa **mod_rewrite** sudah diaktifkan di server Apache.

### 3. Impor Database

Impor database yang disediakan (file `achmadfi_awp.sql`) ke dalam MySQL Anda. Gunakan command berikut di terminal MySQL Anda:

```bash
mysql -u username -p < achmadfi_awp.sql
```

Gantilah `username` dengan nama pengguna MySQL Anda. Anda bisa menggunakan phpMyAdmin atau tool lainnya untuk mengimpor file SQL.

### 4. Konfigurasi Database

Setelah mengimpor database, buka file konfigurasi database di **CodeIgniter** (`application/config/database.php`) dan sesuaikan dengan pengaturan database MySQL Anda, seperti nama database, username, dan password.

```php
$db['default'] = array(
    'dsn'	=> '',
    'hostname' => 'localhost',
    'username' => 'username_mysql',
    'password' => 'password_mysql',
    'database' => 'nama_database',
    'dbdriver' => 'mysqli',
    'dbprefix' => '',
    'pconnect' => FALSE,
    'db_debug' => (ENVIRONMENT !== 'production'),
    'cache_on' => FALSE,
    'cachedir' => '',
    'char_set' => 'utf8',
    'dbcollat' => 'utf8_general_ci',
    'swap_pre' => '',
    'encrypt' => FALSE,
    'compress' => FALSE,
    'stricton' => FALSE,
    'failover' => array(),
    'save_queries' => TRUE
);
```

Gantilah `username_mysql`, `password_mysql`, dan `nama_database` sesuai dengan pengaturan di server Anda.

### 5. Konfigurasi URL (Opsional)

Jika aplikasi ini berada di subdirektori (misalnya `http://localhost/absensi-hrd/`), Anda mungkin perlu menyesuaikan konfigurasi **Base URL** di file `application/config/config.php`:

```php
$config['base_url'] = 'http://localhost/absensi-hrd/';
```

### 6. Jalankan Aplikasi

Setelah konfigurasi selesai, jalankan aplikasi menggunakan server lokal Anda. Jika Anda menggunakan Apache, pastikan **mod_rewrite** diaktifkan dan Anda bisa mengakses aplikasi melalui URL lokal Anda seperti:

```
http://localhost/absensi-hrd/
```

Jika menggunakan server PHP built-in, Anda bisa menjalankan perintah berikut di direktori aplikasi:

```bash
php -S localhost:8080
```

Kemudian akses aplikasi di:

```
http://localhost:8080/
```

---

## Media Sosial

Ikuti kami untuk pembaruan terbaru atau untuk dukungan lebih lanjut:

- **Twitter**: [Masukkan link Twitter Anda di sini]
- **LinkedIn**: [Masukkan link LinkedIn Anda di sini]
- **Facebook**: [Masukkan link Facebook Anda di sini]

---

## Donasi

Jika Anda merasa aplikasi ini bermanfaat dan ingin mendukung pengembangannya, Anda bisa memberikan donasi untuk mendukung pengembangan lebih lanjut. Setiap bantuan sangat berarti!

### Beli Saya Kopi ☕
![Beli Saya Kopi](https://example.com/icon-coffee.png)

[Donasi via PayPal](https://www.paypal.me/username)

---

Terima kasih telah menggunakan **Aplikasi Absensi Karyawan** ini! Jangan ragu untuk memberikan kontribusi atau saran perbaikan!
```

---

### Penjelasan:

- **Deskripsi dan Fitur**: Menyediakan gambaran umum tentang aplikasi HRD untuk mengelola absensi karyawan.
- **Struktur Database**: Menyediakan penjelasan tentang struktur tabel `absensi` yang digunakan oleh aplikasi ini.
- **Cara Instalasi**: Menyediakan instruksi lengkap mulai dari cloning repositori hingga menjalankan aplikasi dengan **CodeIgniter 3**. 
    - **Langkah Konfigurasi** untuk database.
    - **Konfigurasi URL** jika aplikasi tidak di root URL.
    - **Menjalankan aplikasi** baik menggunakan Apache atau server PHP built-in.
- **Media Sosial dan Donasi**: Menyediakan link untuk media sosial dan opsi donasi agar pengguna dapat mendukung aplikasi ini.

Silakan sesuaikan URL dan informasi lainnya sesuai dengan detail aplikasi Anda. Jika ada bagian yang perlu diperbaiki atau ditambahkan, beri tahu saya!
