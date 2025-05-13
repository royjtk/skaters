# Use Case Fully Dressed: Manage Store

## Nama Use Case
Manage Store

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Store Owner**: Ingin mengelola informasi dan pengaturan toko dengan mudah dan efektif.
2. **Platform Skaters**: Ingin memastikan toko dikelola dengan baik dan aktif.
3. **Customer**: Ingin informasi toko akurat dan terpercaya.

## Prasyarat
1. Store Owner telah login ke sistem.
2. Store Owner memiliki toko yang telah dibuat.
3. Toko dalam keadaan aktif (tidak dinonaktifkan oleh sistem).

## Jaminan Kesuksesan
Informasi dan pengaturan toko berhasil diperbarui dan store owner dapat mengelola aspek-aspek toko dengan efektif.

## Skenario Utama Keberhasilan
1. **Store Owner**: Mengakses dashboard toko.
2. **Sistem**: Memverifikasi kepemilikan toko.
3. **Sistem**: Mengambil detail toko.
4. **Sistem**: Menampilkan dashboard toko dengan opsi pengelolaan.
5. **Store Owner**: Memilih "Edit Toko".
6. **Sistem**: Mengambil informasi toko.
7. **Sistem**: Menampilkan formulir edit toko.
8. **Store Owner**: Memperbarui nama toko.
9. **Store Owner**: Memperbarui deskripsi toko.
10. **Store Owner**: Mengirimkan perubahan.
11. **Sistem**: Memvalidasi informasi toko.
12. **Sistem**: Memperbarui catatan toko di database.
13. **Sistem**: Menampilkan pesan sukses.
14. **Sistem**: Kembali ke dashboard toko dengan informasi yang diperbarui.
15. **Store Owner**: Melihat analitik toko.
16. **Sistem**: Mengambil statistik toko.
17. **Sistem**: Menghasilkan laporan toko.
18. **Sistem**: Menampilkan dashboard analitik.

## Ekstensi
1. **Langkah 11: Validasi gagal**
   * Sistem menampilkan pesan kesalahan pada field yang tidak valid.
   * Store Owner dapat memperbaiki input dan mencoba lagi.
2. **Langkah 12: Gagal memperbarui database**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menyarankan untuk mencoba lagi nanti.
3. **Langkah 16-17: Gagal mengambil statistik/laporan**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menampilkan data yang tersedia (jika ada).
   * Sistem menyediakan opsi untuk meminta ulang data.

## Persyaratan Khusus
1. Nama toko harus tetap unik dalam sistem setelah pembaruan.
2. Nama toko harus minimal 3 karakter dan maksimal 50 karakter.
3. Deskripsi toko maksimal 500 karakter.
4. Perubahan informasi toko harus segera terlihat oleh pelanggan.

## Variasi Teknologi dan Data
1. Validasi formulir menggunakan Zod.
2. Pembaruan database menggunakan Prisma.
3. Analitik toko menggunakan agregasi data dari pesanan dan produk.
4. Dashboard interaktif menggunakan komponen client-side React.

## Frekuensi Kejadian
Sering - Store Owner secara rutin memperbarui informasi toko dan melihat analitik.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur tema dan kustomisasi visual toko.
2. Perlu ditambahkan pengaturan untuk preferensi notifikasi dan komunikasi.
3. Perlu dipertimbangkan untuk menambahkan opsi untuk menonaktifkan toko sementara.
