# Use Case Fully Dressed: View Store Orders

## Nama Use Case
View Store Orders

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Store Owner**: Ingin melihat, mengelola, dan melacak semua pesanan untuk tokonya.
2. **Customer**: Ingin pesanan diproses dengan benar dan tepat waktu.
3. **Platform Skaters**: Ingin memastikan pesanan dikelola dengan efisien oleh penjual.

## Prasyarat
1. Store Owner telah login ke sistem.
2. Store Owner memiliki toko aktif.
3. Toko memiliki setidaknya satu pesanan.

## Jaminan Kesuksesan
Store Owner dapat melihat, mengelola, dan memperbarui status semua pesanan untuk tokonya.

## Skenario Utama Keberhasilan
1. **Store Owner**: Mengakses dashboard toko.
2. **Sistem**: Memverifikasi kepemilikan toko.
3. **Sistem**: Menampilkan dashboard toko.
4. **Store Owner**: Memilih tab "Pesanan".
5. **Sistem**: Mengambil pesanan toko.
6. **Sistem**: Menampilkan daftar pesanan.
7. **Store Owner**: Memfilter pesanan berdasarkan status.
8. **Sistem**: Menerapkan filter status.
9. **Sistem**: Menampilkan pesanan yang difilter.
10. **Store Owner**: Memilih pesanan tertentu.
11. **Sistem**: Mengambil detail pesanan.
12. **Sistem**: Mengambil item pesanan.
13. **Sistem**: Menampilkan detail pesanan.
14. **Store Owner**: Memperbarui status pesanan.
15. **Sistem**: Memvalidasi perubahan status.
16. **Sistem**: Memperbarui catatan pesanan.
17. **Sistem**: Menghasilkan notifikasi untuk pelanggan.
18. **Sistem**: Menampilkan konfirmasi pembaruan status.

## Ekstensi
1. **Langkah 5: Tidak ada pesanan**
   * Sistem menampilkan pesan bahwa toko belum memiliki pesanan.
   * Sistem menyarankan langkah untuk meningkatkan penjualan.
2. **Langkah 9: Tidak ada pesanan dengan status tersebut**
   * Sistem menampilkan pesan bahwa tidak ada pesanan dengan status yang dipilih.
   * Sistem menyarankan untuk menggunakan filter lain.
3. **Langkah 15: Validasi perubahan status gagal**
   * Sistem menampilkan pesan kesalahan.
   * Store Owner dapat memilih status yang valid.
4. **Langkah 17: Gagal menghasilkan notifikasi**
   * Sistem mencatat kegagalan.
   * Sistem tetap memperbarui status pesanan.
   * Sistem menandai notifikasi untuk pengiriman ulang.

## Persyaratan Khusus
1. Daftar pesanan harus diurutkan dengan pesanan terbaru di atas.
2. Status pesanan harus ditampilkan dengan indikator visual yang jelas.
3. Perubahan status harus segera terlihat di interface.
4. Store Owner harus dapat melihat riwayat perubahan status.

## Variasi Teknologi dan Data
1. Menggunakan server components untuk mengambil data pesanan.
2. Menggunakan client components untuk fungsionalitas interaktif.
3. Status pesanan disimpan dalam database dengan relasi ke tabel pesanan.
4. Notifikasi dikirim melalui email atau notifikasi in-app.

## Frekuensi Kejadian
Sering - Store Owner secara teratur memeriksa dan mengelola pesanan yang masuk.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur ekspor data pesanan.
2. Perlu ditambahkan fitur catatan internal untuk pesanan.
3. Perlu dipertimbangkan untuk menambahkan fitur komunikasi dengan pelanggan dalam konteks pesanan.
