# Use Case Fully Dressed: Process Payment

## Nama Use Case
Process Payment

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Sistem

## Aktor Utama
Sistem (Processor Pembayaran)

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin proses pembayaran yang aman, cepat, dan berhasil.
2. **Store Owner**: Ingin menerima pembayaran dengan benar.
3. **Platform Skaters**: Ingin memproses pembayaran dengan aman dan dapat diandalkan.
4. **Gateway Pembayaran (Midtrans)**: Ingin memproses transaksi dengan benar dan aman.

## Prasyarat
1. Pengguna telah menyelesaikan langkah checkout dan memilih metode pembayaran.
2. Detail pesanan dan total pembayaran sudah dikalkulasi dengan benar.
3. Koneksi dengan gateway pembayaran Midtrans aktif dan berfungsi.

## Jaminan Kesuksesan
Pembayaran berhasil diproses, pesanan dicatat, dan konfirmasi dikirimkan kepada pelanggan.

## Skenario Utama Keberhasilan
1. **Sistem**: Menerima permintaan pembayaran.
2. **Sistem**: Menyiapkan data pembayaran.
3. **Sistem**: Mengirim permintaan pembayaran ke API Midtrans.
4. **Midtrans API**: Memproses pembayaran.
5. **Midtrans API**: Mengembalikan status pembayaran.
6. **Sistem**: Menerima konfirmasi pembayaran berhasil.
7. **Sistem**: Memperbarui status pesanan sebagai "dibayar".
8. **Sistem**: Menghasilkan faktur.
9. **Sistem**: Mengirim notifikasi sukses.

## Ekstensi
1. **Langkah 3: Gagal menghubungi API Midtrans**
   * Sistem mencatat kesalahan koneksi.
   * Sistem mencoba ulang hingga batas tertentu.
   * Jika tetap gagal, sistem menampilkan pesan kesalahan kepada pengguna.
2. **Langkah 5: Pembayaran gagal**
   * Sistem mencatat kegagalan pembayaran.
   * Sistem mengirim notifikasi kegagalan.
   * Sistem memberikan opsi untuk mencoba metode pembayaran lain.
3. **Langkah 7: Gagal memperbarui status pesanan**
   * Sistem mencatat kesalahan.
   * Sistem mencoba ulang operasi database.
   * Sistem mengirim peringatan ke administrator jika tetap gagal.

## Persyaratan Khusus
1. Semua data pembayaran harus dienkripsi.
2. Komunikasi dengan gateway pembayaran harus aman menggunakan HTTPS.
3. Sistem harus menyimpan log transaksi untuk audit.
4. Timeout untuk proses pembayaran adalah 5 menit.

## Variasi Teknologi dan Data
1. Integrasi dengan API Midtrans untuk pemrosesan pembayaran.
2. Penyimpanan data transaksi dalam database dengan status yang tepat.
3. Penggunaan webhook untuk menangani callback dari gateway pembayaran.
4. Pembuatan token pembayaran sekali pakai untuk keamanan.

## Frekuensi Kejadian
Sering - Setiap kali pembelian dilakukan.

## Lain-lain
1. Sistem harus memiliki mekanisme untuk membatalkan transaksi jika diperlukan.
2. Perlu adanya sistem rekonsiliasi otomatis untuk memastikan semua pembayaran tercatat dengan benar.
3. Sistem perlu menangani berbagai mata uang dan metode pembayaran di masa mendatang.
