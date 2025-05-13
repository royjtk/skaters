# Use Case Fully Dressed: Sign In

## Nama Use Case
Sign In

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer atau Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin masuk ke sistem untuk melakukan pembelian, melihat riwayat pesanan, dan mengelola keranjang belanja.
2. **Store Owner**: Ingin masuk ke sistem untuk mengelola toko, produk, dan pesanan.
3. **Sistem**: Memastikan hanya pengguna yang terautentikasi yang dapat mengakses fitur tertentu.

## Prasyarat
1. Pengguna sudah memiliki akun Google.
2. Pengguna memiliki koneksi internet.
3. Sistem autentikasi (OAuth provider) berfungsi dengan baik.

## Jaminan Kesuksesan
Pengguna berhasil masuk ke sistem dan mendapatkan akses ke fitur-fitur yang sesuai dengan perannya.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengakses halaman Sign In aplikasi Skaters.
2. **Sistem**: Menampilkan opsi autentikasi (Google).
3. **Pengguna**: Memilih Sign In dengan Google.
4. **Sistem**: Mengarahkan pengguna ke halaman autentikasi Google.
5. **Pengguna**: Memasukkan kredensial Google.
6. **Sistem**: Memvalidasi kredensial dengan Google OAuth.
7. **Sistem**: Memverifikasi/membuat data pengguna di database.
8. **Sistem**: Membuat sesi untuk pengguna.
9. **Sistem**: Mengarahkan pengguna ke halaman beranda dengan status sudah login.

## Ekstensi
1. **Langkah 6: Autentikasi Gagal**
   * Sistem menampilkan pesan kesalahan yang sesuai.
   * Pengguna dapat mencoba login kembali.
2. **Langkah 7: Akun tidak ditemukan**
   * Sistem secara otomatis membuat akun baru menggunakan data dari Google.
3. **Langkah 8: Sesi tidak dapat dibuat**
   * Sistem menampilkan pesan kesalahan.
   * Pengguna diarahkan kembali ke halaman login.

## Persyaratan Khusus
1. Proses autentikasi harus selesai dalam waktu kurang dari 5 detik.
2. Sistem harus menampilkan indikator loading selama proses autentikasi.
3. Harus ada mekanisme untuk menangani kegagalan koneksi.

## Variasi Teknologi dan Data
1. Autentikasi menggunakan Google OAuth.
2. Data pengguna yang disimpan mencakup nama, email, dan gambar profil.
3. Informasi sesi disimpan menggunakan JWT (JSON Web Token).

## Frekuensi Kejadian
Sering - Setiap pengguna harus melakukan login setidaknya sekali untuk menggunakan fitur-fitur tertentu di aplikasi.

## Lain-lain
1. Sesi login akan kedaluwarsa dalam 2 hari (sesuai dengan konfigurasi maxAge).
2. Pengguna dapat tetap masuk menggunakan fitur "remember me".
3. Halaman login harus sesuai dengan standar UI/UX aplikasi.
