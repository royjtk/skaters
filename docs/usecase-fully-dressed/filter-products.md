# Use Case Fully Dressed: Filter Products by Category

## Nama Use Case
Filter Products by Category

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin menemukan produk dalam kategori tertentu dengan cepat dan mudah.
2. **Store Owner**: Ingin produk mereka dapat ditemukan dalam kategori yang tepat.
3. **Platform Skaters**: Ingin menyediakan navigasi yang intuitif berdasarkan kategori.

## Prasyarat
1. Sistem telah memuat daftar kategori yang tersedia.
2. Produk telah dikategorikan dengan benar dalam database.

## Jaminan Kesuksesan
Pengguna dapat memfilter dan melihat produk berdasarkan kategori yang dipilih dengan akurat dan efisien.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengakses halaman produk.
2. **Sistem**: Mengambil semua kategori.
3. **Sistem**: Mengambil produk awal.
4. **Sistem**: Menampilkan halaman dengan produk dan daftar kategori.
5. **Pengguna**: Memilih kategori tertentu dari filter.
6. **Sistem**: Menerapkan filter kategori.
7. **Sistem**: Mengambil produk yang sesuai dengan kategori.
8. **Sistem**: Memperbarui URL dengan parameter kategori.
9. **Sistem**: Menampilkan produk yang difilter.
10. **Pengguna**: Menggulir ke bawah untuk melihat lebih banyak produk.
11. **Sistem**: Mengambil lebih banyak produk dengan filter kategori yang sama.
12. **Sistem**: Menampilkan produk tambahan.
13. **Pengguna**: Menghapus filter kategori.
14. **Sistem**: Menghapus filter.
15. **Sistem**: Mengambil produk tanpa filter.
16. **Sistem**: Memperbarui URL tanpa parameter kategori.
17. **Sistem**: Menampilkan semua produk.

## Ekstensi
1. **Langkah 7: Tidak ada produk dalam kategori**
   * Sistem menampilkan pesan bahwa tidak ada produk dalam kategori ini.
   * Sistem menyarankan kategori lain atau menyarankan untuk menghapus filter.
2. **Langkah 8: Gagal memperbarui URL**
   * Sistem tetap menampilkan produk yang difilter tetapi tidak memperbarui URL.
   * URL tetap dapat digunakan untuk navigasi normal.
3. **Langkah 11: Tidak ada produk tambahan**
   * Sistem menunjukkan bahwa semua produk dalam kategori telah dimuat.

## Persyaratan Khusus
1. Perubahan kategori harus segera terlihat tanpa reload halaman penuh.
2. URL harus mencerminkan filter yang diterapkan untuk bookmark dan berbagi.
3. Pengambilan produk harus efisien dan tidak mengambil semua produk sekaligus.
4. Filter kategori harus tetap aktif saat navigasi antar halaman.

## Variasi Teknologi dan Data
1. Penggunaan parameter URL untuk filter kategori.
2. Implementasi infinite scroll untuk loading inkremental.
3. Server-side filtering untuk performa yang lebih baik.
4. Caching hasil filter untuk kategori yang sering diakses.

## Frekuensi Kejadian
Sangat sering - Filtering berdasarkan kategori adalah metode navigasi utama di toko online.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan filter bertingkat atau multi-filter.
2. Perlu dipertimbangkan untuk menambahkan tampilan visual kategori dengan ikon atau gambar.
3. Perlu menambahkan breadcrumbs untuk navigasi kategori yang lebih intuitif.
