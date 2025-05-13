# Use Case Fully Dressed: Manage Product Inventory

## Nama Use Case
Manage Product Inventory

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Store Owner**: Ingin mengelola stok dan ketersediaan produk dengan efisien.
2. **Customer**: Ingin informasi ketersediaan produk yang akurat.
3. **Platform Skaters**: Ingin memastikan informasi produk selalu aktual.

## Prasyarat
1. Store Owner telah login ke sistem.
2. Store Owner memiliki toko aktif.
3. Toko memiliki setidaknya satu produk yang terdaftar.

## Jaminan Kesuksesan
Store Owner dapat mengelola inventaris produk dengan efektif, memperbarui stok, dan mengatur ketersediaan produk.

## Skenario Utama Keberhasilan
1. **Store Owner**: Mengakses dashboard toko.
2. **Sistem**: Memverifikasi kepemilikan toko.
3. **Sistem**: Mengambil produk toko.
4. **Sistem**: Menampilkan daftar produk.
5. **Store Owner**: Memilih "Manajemen Inventaris".
6. **Sistem**: Mengambil informasi inventaris.
7. **Sistem**: Menampilkan dashboard inventaris.
8. **Store Owner**: Memperbarui jumlah stok produk tertentu.
9. **Sistem**: Memvalidasi input jumlah.
10. **Sistem**: Memperbarui catatan produk.
11. **Sistem**: Menampilkan konfirmasi pembaruan.
12. **Store Owner**: Menandai produk sebagai "Stok Habis".
13. **Sistem**: Memperbarui ketersediaan produk.
14. **Sistem**: Memperbarui tampilan status produk.
15. **Store Owner**: Mengaktifkan/menonaktifkan visibilitas produk.
16. **Sistem**: Mengubah status arsip produk.
17. **Sistem**: Menampilkan status yang diperbarui.
18. **Store Owner**: Melihat peringatan stok rendah.
19. **Sistem**: Memeriksa ambang batas inventaris.
20. **Sistem**: Menampilkan item dengan stok rendah.

## Ekstensi
1. **Langkah 9: Validasi input gagal**
   * Sistem menampilkan pesan kesalahan.
   * Store Owner dapat memperbaiki input dan mencoba lagi.
2. **Langkah 10: Gagal memperbarui catatan**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menyarankan untuk mencoba lagi nanti.
3. **Langkah 16: Gagal mengubah status arsip**
   * Sistem mencatat kesalahan.
   * Sistem menampilkan pesan kesalahan.
   * Store Owner dapat mencoba lagi.

## Persyaratan Khusus
1. Pembaruan stok harus segera terlihat oleh pelanggan.
2. Produk dengan stok nol harus secara otomatis ditandai sebagai "Stok Habis".
3. Sistem harus mendukung pembaruan inventaris massal untuk beberapa produk.
4. Dashboard harus menampilkan peringatan visual untuk produk dengan stok rendah.

## Variasi Teknologi dan Data
1. Penggunaan fitur database untuk melacak perubahan inventaris.
2. Implementasi batch updates untuk efisiensi.
3. Penggunaan webhooks untuk memicu pemberitahuan stok rendah.
4. Integrasi dengan sistem analitik untuk prediksi inventaris.

## Frekuensi Kejadian
Sangat sering - Store Owner secara rutin memperbarui stok dan ketersediaan produk.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur riwayat perubahan inventaris.
2. Sistem perlu mendukung impor/ekspor data inventaris massal.
3. Perlu dipertimbangkan untuk mengintegrasikan dengan sistem manajemen inventaris eksternal.
4. Perlu ditambahkan pemberitahuan otomatis untuk stok rendah atau habis.
