# Use Case Fully Dressed: Manage Cart Items

## Nama Use Case
Manage Cart Items

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin mengelola item dalam keranjang belanja dengan mudah dan fleksibel.
2. **Store Owner**: Ingin pelanggan memiliki pengalaman yang baik saat mengelola keranjang belanja.
3. **Platform Skaters**: Ingin menyediakan fungsionalitas keranjang yang intuitif dan responsif.

## Prasyarat
1. Pengguna telah menambahkan setidaknya satu produk ke keranjang belanja.
2. Data keranjang tersimpan dalam localStorage browser.

## Jaminan Kesuksesan
Pengguna dapat melihat, memperbarui, dan menghapus item dari keranjang belanja dengan lancar dan intuitif.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengklik ikon keranjang.
2. **Sistem**: Mengambil data item keranjang dari localStorage.
3. **Sistem**: Menampilkan halaman keranjang dengan daftar item.
4. **Pengguna**: Mengubah kuantitas item tertentu.
5. **Sistem**: Memperbarui item dalam localStorage.
6. **Sistem**: Menghitung ulang total harga.
7. **Sistem**: Memperbarui tampilan keranjang.
8. **Pengguna**: Menghapus item dari keranjang.
9. **Sistem**: Menghapus item dari localStorage.
10. **Sistem**: Menghitung ulang total harga.
11. **Sistem**: Memperbarui tampilan keranjang.
12. **Pengguna**: Mengklik "Lanjutkan Belanja".
13. **Sistem**: Mengarahkan pengguna ke halaman produk.
14. **Pengguna**: Mengklik "Checkout".
15. **Sistem**: Memvalidasi item keranjang.
16. **Sistem**: Mengarahkan pengguna ke halaman checkout.

## Ekstensi
1. **Langkah 2: Keranjang kosong**
   * Sistem menampilkan pesan bahwa keranjang kosong.
   * Sistem menyarankan produk atau kategori untuk dilihat.
2. **Langkah 5: Gagal memperbarui localStorage**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menyarankan untuk memeriksa pengaturan browser.
3. **Langkah 15: Validasi gagal**
   * Sistem menampilkan pesan kesalahan (misalnya, stok tidak cukup).
   * Sistem meminta pengguna untuk menyesuaikan kuantitas atau menghapus item.

## Persyaratan Khusus
1. Perubahan dalam keranjang harus instan tanpa reload halaman.
2. Keranjang harus menyimpan data bahkan setelah browser ditutup.
3. Tampilan keranjang harus responsif di semua ukuran layar.
4. Sistem harus mendukung pembaruan secara bulk jika diperlukan.

## Variasi Teknologi dan Data
1. Menggunakan Zustand untuk manajemen state keranjang.
2. Data keranjang disimpan dalam localStorage menggunakan JSON.
3. Menggunakan React hooks untuk mengelola perubahan state.

## Frekuensi Kejadian
Sering - Pengguna secara teratur mengelola item dalam keranjang sebelum menyelesaikan pembelian.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur "Simpan untuk nanti".
2. Sistem harus memverifikasi ketersediaan stok saat checkout.
3. Perlu dipertimbangkan untuk menambahkan fitur keranjang yang persisten (server-side) untuk pengguna yang login.
