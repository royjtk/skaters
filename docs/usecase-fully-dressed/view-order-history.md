# Use Case Fully Dressed: View Order History

## Nama Use Case
View Order History

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin melihat dan melacak semua pesanan yang telah dibuat.
2. **Platform Skaters**: Ingin memberikan transparansi dan akses ke riwayat pesanan.
3. **Store Owner**: Ingin pelanggan dapat melihat pesanan mereka dengan benar.

## Prasyarat
1. Pengguna telah login ke akun mereka.
2. Pengguna memiliki setidaknya satu pesanan yang telah dibuat.

## Jaminan Kesuksesan
Pengguna dapat melihat daftar lengkap dan detail pesanan mereka dengan akurat dan mudah.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengakses halaman riwayat pesanan.
2. **Sistem**: Mengautentikasi pengguna.
3. **Sistem**: Mengambil pesanan pengguna dari database.
4. **Sistem**: Menampilkan daftar pesanan dengan detail singkat.
5. **Pengguna**: Melihat daftar pesanan.
6. **Pengguna**: Mengklik pada pesanan tertentu untuk detail.
7. **Sistem**: Mengambil detail lengkap pesanan.
8. **Sistem**: Mengambil item pesanan.
9. **Sistem**: Menampilkan halaman detail pesanan.
10. **Pengguna**: Melihat detail pesanan termasuk produk, harga, status, dll.
11. **Pengguna**: Memfilter pesanan berdasarkan status.
12. **Sistem**: Menerapkan filter status.
13. **Sistem**: Menampilkan pesanan yang difilter.

## Ekstensi
1. **Langkah 3: Tidak ada pesanan**
   * Sistem menampilkan pesan bahwa pengguna belum memiliki pesanan.
   * Sistem menyarankan untuk menjelajahi produk.
2. **Langkah 7-8: Gagal mengambil detail pesanan**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menawarkan untuk mencoba lagi.
3. **Langkah 13: Tidak ada pesanan dengan status tersebut**
   * Sistem menampilkan pesan bahwa tidak ada pesanan dengan status yang dipilih.
   * Sistem menyarankan untuk menggunakan filter lain.

## Persyaratan Khusus
1. Daftar pesanan harus diurutkan dengan pesanan terbaru di atas.
2. Status pesanan harus ditampilkan dengan indikator visual yang jelas.
3. Halaman harus responsif dan berfungsi di semua ukuran layar.
4. Daftar pesanan harus dimuat secara inkremental untuk kinerja yang lebih baik.

## Variasi Teknologi dan Data
1. Menggunakan infinite scroll untuk memuat pesanan inkremental.
2. Filter status menggunakan parameter URL.
3. Caching data pesanan untuk kinerja yang lebih baik.
4. Menggunakan server-side rendering untuk SEO dan kinerja awal yang lebih baik.

## Frekuensi Kejadian
Sering - Pengguna secara teratur memeriksa status pesanan mereka dan melihat riwayat pesanan.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur pencarian dalam pesanan.
2. Perlu ditambahkan opsi untuk mengunduh faktur atau tanda terima.
3. Sistem perlu menyimpan riwayat pesanan untuk jangka waktu yang memadai (minimal 1 tahun).
