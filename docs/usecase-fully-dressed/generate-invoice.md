# Use Case Fully Dressed: Generate Invoice

## Nama Use Case
Generate Invoice

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Sistem

## Aktor Utama
Sistem (Generator Faktur)

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin menerima faktur yang akurat dan profesional untuk pembukuan.
2. **Store Owner**: Ingin faktur yang benar diterbitkan untuk pesanan.
3. **Platform Skaters**: Ingin menyediakan dokumentasi resmi untuk transaksi.
4. **Otoritas Pajak**: Memerlukan faktur yang sesuai dengan peraturan.

## Prasyarat
1. Pembayaran untuk pesanan telah berhasil diproses.
2. Data pesanan lengkap dan tersedia di database.
3. Detail pembayaran tersedia dan valid.

## Jaminan Kesuksesan
Faktur yang akurat dan sesuai peraturan berhasil dibuat, disimpan, dan tersedia untuk pelanggan.

## Skenario Utama Keberhasilan
1. **Sistem**: Menerima notifikasi pembayaran berhasil.
2. **Sistem**: Mengambil detail pesanan dari database.
3. **Sistem**: Mengambil item pesanan.
4. **Sistem**: Mengambil informasi pelanggan.
5. **Sistem**: Mengambil informasi toko.
6. **Sistem**: Menghasilkan dokumen faktur dengan semua informasi yang diperlukan.
7. **Sistem**: Menghitung total dan pajak.
8. **Sistem**: Memformat tata letak faktur.
9. **Sistem**: Menyimpan faktur dalam database.
10. **Sistem**: Mengaitkan faktur dengan pesanan.
11. **Sistem**: Menghasilkan PDF faktur.
12. **Sistem**: Mengirim faktur ke email pelanggan.

## Ekstensi
1. **Langkah 2-5: Gagal mengambil data yang diperlukan**
   * Sistem mencatat kesalahan.
   * Sistem menandai faktur untuk pembuatan manual.
   * Sistem mengirim notifikasi ke administrator.
2. **Langkah 11: Gagal menghasilkan PDF**
   * Sistem mencoba ulang dengan format alternatif.
   * Jika tetap gagal, sistem menyimpan data faktur mentah.
3. **Langkah 12: Gagal mengirim email**
   * Sistem mencatat kegagalan pengiriman.
   * Sistem menandai faktur untuk pengiriman ulang.
   * Sistem membuat faktur tersedia untuk diunduh di akun pengguna.

## Persyaratan Khusus
1. Faktur harus sesuai dengan format standar akuntansi.
2. Semua informasi hukum yang diperlukan harus disertakan (nomor pajak, alamat perusahaan, dll).
3. PDF faktur harus ditandatangani secara digital jika diperlukan oleh peraturan.
4. Nomor faktur harus unik dan berurutan.

## Variasi Teknologi dan Data
1. Menggunakan library PDF generator untuk membuat dokumen faktur.
2. Menyimpan template faktur untuk penggunaan kembali.
3. Menggunakan layanan email untuk pengiriman faktur.
4. Enkripsi faktur untuk keamanan data.

## Frekuensi Kejadian
Sering - Setiap pesanan yang berhasil memerlukan pembuatan faktur.

## Lain-lain
1. Sistem harus menyimpan riwayat faktur untuk jangka waktu yang sesuai dengan peraturan perpajakan.
2. Perlu dipertimbangkan untuk menambahkan fitur faktur koreksi jika terjadi kesalahan.
3. Format faktur mungkin perlu disesuaikan untuk berbagai negara dengan peraturan berbeda.
