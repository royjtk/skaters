# Use Case Fully Dressed: Checkout

## Nama Use Case
Checkout

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin menyelesaikan pembelian dengan cepat, aman, dan mendapatkan konfirmasi pemesanan.
2. **Store Owner**: Ingin menerima pesanan dengan detail lengkap.
3. **Sistem Pembayaran**: Memproses transaksi dengan aman dan akurat.
4. **Perusahaan**: Ingin memastikan transaksi tercatat dengan benar dan meningkatkan penjualan.

## Prasyarat
1. Pengguna telah menambahkan produk ke keranjang belanja.
2. Keranjang belanja tidak kosong.
3. Pengguna telah masuk ke sistem (login).

## Jaminan Kesuksesan
Pesanan berhasil dibuat, pembayaran diproses, dan konfirmasi pesanan dikirim kepada pelanggan.

## Skenario Utama Keberhasilan
1. **Pengguna**: Membuka halaman keranjang belanja.
2. **Pengguna**: Mengklik tombol "Checkout".
3. **Sistem**: Menampilkan formulir informasi pengiriman.
4. **Pengguna**: Mengisi informasi pengiriman (alamat, nomor telepon).
5. **Pengguna**: Mengklik tombol "Lanjutkan ke Pembayaran".
6. **Sistem**: Memvalidasi informasi pengiriman.
7. **Sistem**: Menampilkan ringkasan pesanan dan opsi pembayaran.
8. **Pengguna**: Memilih metode pembayaran (melalui Midtrans).
9. **Pengguna**: Mengkonfirmasi pesanan.
10. **Sistem**: Memproses pembayaran melalui Midtrans.
11. **Sistem**: Membuat catatan pesanan di database.
12. **Sistem**: Mengurangi stok produk yang dibeli.
13. **Sistem**: Mengosongkan keranjang belanja.
14. **Sistem**: Menghasilkan faktur.
15. **Sistem**: Menampilkan halaman konfirmasi pesanan.
16. **Sistem**: Mengirim email konfirmasi pesanan kepada pelanggan.

## Ekstensi
1. **Langkah 6: Validasi gagal**
   * Sistem menampilkan pesan kesalahan pada formulir.
   * Pengguna diminta untuk memperbaiki informasi yang tidak valid.
2. **Langkah 10: Pembayaran gagal**
   * Sistem menampilkan pesan kesalahan pembayaran.
   * Pengguna dapat mencoba metode pembayaran lain atau mencoba lagi.
3. **Langkah 11-12: Gagal menyimpan pesanan**
   * Sistem membatalkan transaksi.
   * Sistem mengembalikan status pembayaran jika sudah diproses.
   * Sistem menampilkan pesan kesalahan dan menyarankan pengguna untuk mencoba lagi.

## Persyaratan Khusus
1. Proses checkout harus aman dengan menggunakan enkripsi data.
2. Halaman pembayaran harus mematuhi standar keamanan PCI DSS.
3. Sistem harus memberikan umpan balik yang jelas pada setiap langkah proses.
4. Waktu load halaman checkout tidak boleh lebih dari 3 detik.

## Variasi Teknologi dan Data
1. Integrasi dengan gateway pembayaran Midtrans.
2. Data pesanan disimpan di database dengan relasi ke produk dan pengguna.
3. Email konfirmasi dikirim menggunakan layanan email yang terintegrasi.
4. Faktur dihasilkan dalam format PDF.

## Frekuensi Kejadian
Sering - Setiap pembelian yang sukses akan melalui proses checkout.

## Lain-lain
1. Sistem harus mampu menangani checkout dengan banyak produk.
2. Perlu adanya mekanisme timeout untuk menjaga slot stok.
3. Perlu adanya riwayat pesanan untuk pengguna.
4. Sistem harus mampu menangani beberapa checkout bersamaan.
