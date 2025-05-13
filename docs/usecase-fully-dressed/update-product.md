# Use Case Fully Dressed: Update Product

## Nama Use Case
Update Product

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Store Owner**: Ingin memperbarui informasi produk yang ada.
2. **Customer**: Ingin melihat informasi produk yang akurat dan terbaru.
3. **Platform Skaters**: Ingin memastikan produk memiliki informasi yang valid dan terkini.

## Prasyarat
1. Store Owner telah login ke sistem.
2. Store Owner memiliki toko aktif.
3. Produk yang akan diperbarui sudah ada dalam sistem.

## Jaminan Kesuksesan
Produk berhasil diperbarui dengan informasi terbaru dan perubahan terlihat oleh pelanggan.

## Skenario Utama Keberhasilan
1. **Store Owner**: Membuka dashboard toko.
2. **Sistem**: Memverifikasi kepemilikan toko.
3. **Sistem**: Mengambil daftar produk toko.
4. **Sistem**: Menampilkan daftar produk kepada Store Owner.
5. **Store Owner**: Memilih produk untuk diedit.
6. **Sistem**: Mengambil detail produk.
7. **Sistem**: Mengambil gambar produk.
8. **Sistem**: Mengambil daftar kategori.
9. **Sistem**: Menampilkan formulir edit produk.
10. **Store Owner**: Memperbarui informasi produk.
11. **Store Owner**: Memperbarui gambar produk (menambah/menghapus).
12. **Store Owner**: Mengirimkan perubahan.
13. **Sistem**: Memvalidasi informasi yang diperbarui.
14. **Sistem**: Memperbarui data produk di database.
15. **Sistem**: Menangani perubahan gambar.
16. **Sistem**: Menampilkan pesan sukses.
17. **Sistem**: Mengarahkan kembali ke daftar produk.

## Ekstensi
1. **Langkah 13: Validasi gagal**
   * Sistem menampilkan pesan kesalahan pada field yang tidak valid.
   * Store Owner dapat memperbaiki input dan mencoba lagi.
2. **Langkah 15: Gagal mengunggah gambar baru**
   * Sistem mencatat kesalahan.
   * Sistem menampilkan pesan kesalahan.
   * Sistem tetap menyimpan perubahan lain pada produk.
3. **Langkah 15: Gagal menghapus gambar**
   * Sistem mencatat kesalahan.
   * Sistem menampilkan pesan kesalahan.
   * Sistem menandai gambar untuk penghapusan di masa mendatang.

## Persyaratan Khusus
1. Formulir edit harus menampilkan data produk yang ada sebagai nilai awal.
2. Preview gambar harus tersedia untuk gambar yang diunggah.
3. Sistem harus mempertahankan slug produk kecuali nama diubah.
4. Perubahan harus diterapkan dalam waktu kurang dari 5 detik.

## Variasi Teknologi dan Data
1. Validasi formulir menggunakan Zod.
2. Pengunggahan gambar menggunakan Uploadthing.
3. Penghapusan gambar lama menggunakan service deleteFiles.
4. Pembaruan database menggunakan Prisma Client.

## Frekuensi Kejadian
Sering - Store Owner secara rutin memperbarui produk mereka untuk menjaga informasi tetap akurat.

## Lain-lain
1. Sistem perlu mencatat riwayat perubahan produk untuk audit.
2. Perlu dipertimbangkan untuk menambahkan fitur publikasi terjadwal untuk pembaruan.
3. Store Owner perlu memiliki opsi untuk melihat versi produk sebelumnya dan mengembalikan perubahan jika perlu.
