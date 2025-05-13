# Use Case Fully Dressed: Create Store

## Nama Use Case
Create Store

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Store Owner**: Ingin membuat toko online untuk menjual produk.
2. **Platform Skaters**: Ingin meningkatkan jumlah toko dan produk yang tersedia.
3. **Customer**: Ingin memiliki lebih banyak pilihan toko dan produk.

## Prasyarat
1. Pengguna telah masuk ke sistem (login).
2. Pengguna memiliki akun yang terverifikasi.

## Jaminan Kesuksesan
Toko baru berhasil dibuat dan terdaftar di platform, siap untuk menambahkan produk.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengakses dashboard.
2. **Sistem**: Menampilkan opsi untuk membuat toko baru.
3. **Pengguna**: Mengklik tombol "Buat Toko".
4. **Sistem**: Menampilkan formulir pembuatan toko.
5. **Pengguna**: Mengisi nama toko.
6. **Pengguna**: Mengisi deskripsi toko (opsional).
7. **Pengguna**: Mengklik tombol "Buat".
8. **Sistem**: Memvalidasi informasi toko.
9. **Sistem**: Membuat data toko di database.
10. **Sistem**: Mengaitkan toko dengan akun pengguna.
11. **Sistem**: Mengarahkan pengguna ke dashboard toko baru.
12. **Sistem**: Menampilkan pesan sukses dan panduan langkah selanjutnya.

## Ekstensi
1. **Langkah 8: Validasi gagal**
   * Sistem menampilkan pesan kesalahan spesifik.
   * Pengguna dapat memperbaiki input dan mencoba lagi.
2. **Langkah 9: Kegagalan membuat data toko**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menyarankan untuk mencoba lagi nanti.
3. **Langkah 5-6: Pengguna membatalkan pembuatan toko**
   * Pengguna mengklik tombol "Batal".
   * Sistem mengarahkan pengguna kembali ke halaman sebelumnya.

## Persyaratan Khusus
1. Nama toko harus unik dalam sistem.
2. Nama toko harus minimal 3 karakter dan maksimal 50 karakter.
3. Deskripsi toko maksimal 500 karakter.
4. Proses pembuatan toko harus selesai dalam waktu kurang dari 5 detik.

## Variasi Teknologi dan Data
1. Validasi formulir menggunakan library Zod.
2. Data toko disimpan dalam database Prisma.
3. Hubungan relasi antara tabel User dan Store.

## Frekuensi Kejadian
Jarang - Pengguna biasanya hanya membuat satu toko atau beberapa toko.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur verifikasi toko di masa mendatang.
2. Perlu dipertimbangkan untuk menambahkan fitur customisasi tampilan toko.
3. Sistem perlu memastikan bahwa setiap toko memiliki URL yang unik.
