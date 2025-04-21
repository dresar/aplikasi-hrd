# Aplikasi Absensi

## Deskripsi

**Aplikasi Absensi** adalah aplikasi berbasis web yang dirancang untuk membantu perusahaan dalam mengelola absensi karyawan. Aplikasi ini memungkinkan karyawan untuk mencatat absensi mereka, memilih jenis cuti (misalnya Sakit, Izin, Cuti, Alpa, atau Telat), serta melacak durasi setiap absensi. Administrator dapat mengelola data absensi karyawan dan mendapatkan laporan terkait absensi.

---

## Fitur

- **Pencatatan Absensi Karyawan**: Karyawan dapat mencatat absensi mereka sesuai dengan tanggal, alasan, dan durasi.
- **Jenis Cuti yang Beragam**: Jenis cuti yang dapat dipilih oleh karyawan: Sakit, Izin, Cuti, Alpa, dan Telat.
- **Manajemen Absensi**: Administrator dapat melihat, menambah, mengedit, dan menghapus data absensi karyawan.
- **Laporan Absensi**: Sistem menyediakan laporan yang dapat membantu untuk memantau kinerja dan ketidakhadiran karyawan.

---

## Struktur Database

Aplikasi ini menggunakan database dengan beberapa tabel untuk menyimpan data absensi karyawan. Salah satu tabel yang paling penting adalah tabel `absensi`. Berikut adalah struktur tabel tersebut:

### Tabel: `absensi`

| Nama Kolom            | Tipe Data         | Deskripsi                                      |
|-----------------------|-------------------|------------------------------------------------|
| `id_absen`            | `int(11)`         | Identifier unik untuk setiap catatan absensi.  |
| `nik_karyawan_absen`  | `varchar(16)`      | ID Karyawan yang terkait dengan absensi.      |
| `tanggal_absen`       | `date`            | Tanggal absensi yang dicatat.                 |
| `tanggal_selesai`     | `date`            | Tanggal berakhirnya cuti atau absensi.        |
| `keterangan_absen`    | `enum`            | Jenis absensi: Sakit, Izin, Cuti, Alpa, Telat. |
| `lama_absen`          | `varchar(10)`      | Durasi absensi dalam jam atau hari.           |
| `keterangan`          | `varchar(50)`      | Catatan tambahan terkait absensi.             |
| `jenis_cuti`          | `enum`            | Jenis cuti, jika berlaku.                     |

---

## Cara Menjalankan Aplikasi

Ikuti langkah-langkah di bawah ini untuk menjalankan aplikasi ini di lingkungan lokal Anda:

1. **Clone Repositori**:
    ```bash
    git clone https://github.com/username/absensi-app.git
    ```
2. **Instalasi Dependensi**:
    Pastikan Anda telah menginstal PHP dan MySQL di mesin lokal Anda. Jika menggunakan server Apache, pastikan mod_rewrite telah diaktifkan.
   
3. **Impor Database**:
    Impor file SQL yang disediakan (`achmadfi_awp.sql`) ke dalam database MySQL Anda:
    ```bash
    mysql -u username -p < achmadfi_awp.sql
    ```
    Jangan lupa mengganti `username` dengan nama pengguna MySQL Anda.

4. **Konfigurasi Koneksi Database**:
    Sesuaikan file konfigurasi aplikasi untuk menghubungkan ke database MySQL yang telah diimpor.

5. **Menjalankan Aplikasi**:
    Jalankan aplikasi menggunakan server lokal atau layanan hosting Anda yang mendukung PHP.

---

## Media Sosial

Untuk update dan dukungan lebih lanjut, ikuti kami di media sosial:

- **Twitter**: [Masukkan link Twitter Anda di sini]
- **LinkedIn**: [Masukkan link LinkedIn Anda di sini]
- **Facebook**: [Masukkan link Facebook Anda di sini]

---

## Donasi

Jika Anda merasa aplikasi ini bermanfaat dan ingin mendukung pengembangan lebih lanjut, Anda bisa memberikan donasi melalui link di bawah ini. Setiap dukungan sangat berarti!

### Beli Saya Kopi ☕
![Beli Saya Kopi](https://example.com/icon-coffee.png)

[Donasi via PayPal](https://www.paypal.me/username)

---

Terima kasih telah menggunakan **Aplikasi Absensi**!

