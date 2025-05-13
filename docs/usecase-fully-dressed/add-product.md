# Use Case Fully Dressed: Add Product

## Nama Use Case
Add Product

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Store Owner**: Ingin menambahkan produk ke tokonya untuk dijual.
2. **Platform Skaters**: Ingin meningkatkan jumlah dan variasi produk yang tersedia.
3. **Customer**: Ingin memiliki lebih banyak pilihan produk untuk dibeli.

## Prasyarat
1. Store Owner telah masuk ke sistem (login).
2. Store Owner telah membuat toko.
3. Toko dalam keadaan aktif.

## Jaminan Kesuksesan
Produk baru berhasil ditambahkan ke toko dan tersedia untuk dibeli oleh pelanggan.

## Skenario Utama Keberhasilan
1. **Store Owner**: Mengakses dashboard toko.
2. **Sistem**: Memverifikasi kepemilikan toko.
3. **Sistem**: Menampilkan dashboard toko.
4. **Store Owner**: Mengklik tombol "Tambah Produk".
5. **Sistem**: Mengambil data kategori.
6. **Sistem**: Menampilkan formulir penambahan produk.
7. **Store Owner**: Mengisi nama produk.
8. **Store Owner**: Mengisi deskripsi produk.
9. **Store Owner**: Menetapkan harga produk.
10. **Store Owner**: Memilih kategori produk.
11. **Store Owner**: Menetapkan jumlah stok.
12. **Store Owner**: Mengunggah gambar produk.
13. **Store Owner**: Mengklik tombol "Simpan".
14. **Sistem**: Memvalidasi informasi produk.
15. **Sistem**: Mengunggah gambar ke penyimpanan.
16. **Sistem**: Membuat data produk di database.
17. **Sistem**: Mengaitkan gambar dengan produk.
18. **Sistem**: Menampilkan pesan sukses.
19. **Sistem**: Kembali ke daftar produk dengan produk baru ditampilkan.

## Ekstensi
1. **Langkah 14: Validasi gagal**
   * Sistem menampilkan pesan kesalahan pada field yang tidak valid.
   * Store Owner dapat memperbaiki input dan mencoba lagi.
2. **Langkah 15: Pengunggahan gambar gagal**
   * Sistem menampilkan pesan kesalahan.
   * Store Owner dapat mencoba mengunggah gambar lain.
3. **Langkah 16: Kegagalan menyimpan data produk**
   * Sistem menampilkan pesan kesalahan.
   * Sistem membersihkan gambar yang sudah diunggah.
   * Store Owner dapat mencoba lagi nanti.

## Persyaratan Khusus
1. Nama produk harus unik dalam toko.
2. Gambar produk harus dalam format yang didukung (JPEG, PNG, WebP).
3. Ukuran gambar tidak boleh melebihi 5MB per gambar.
4. Produk harus memiliki setidaknya satu gambar.
5. Harga produk harus lebih besar dari 0.

## Variasi Teknologi dan Data
1. Validasi formulir menggunakan library Zod.
2. Pengunggahan gambar menggunakan Uploadthing.
3. Penyimpanan data produk dalam database Prisma.
4. Relasi antara tabel Product, Store, Category, dan Image.

## Frekuensi Kejadian
Sering - Store Owner akan sering menambahkan produk baru ke toko mereka.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur duplikasi produk untuk memudahkan penambahan produk serupa.
2. Perlu ditambahkan fitur preview produk sebelum dipublikasikan.
3. Perlu dipertimbangkan untuk menambahkan fitur penjadwalan publikasi produk.
