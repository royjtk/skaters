# Use Case Fully Dressed: View Product Details

## Nama Use Case
View Product Details

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin melihat informasi detail produk sebelum memutuskan untuk membeli.
2. **Store Owner**: Ingin produknya ditampilkan dengan baik dengan semua informasi yang relevan.
3. **Platform Skaters**: Ingin menyediakan tampilan produk yang informatif dan menarik.

## Prasyarat
1. Produk tersedia di database.
2. Gambar produk dan informasi terkait telah diunggah.

## Jaminan Kesuksesan
Pengguna dapat melihat informasi detail produk dengan lengkap dan jelas, serta memiliki opsi untuk melakukan tindakan lanjutan seperti menambahkan ke keranjang.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengklik kartu produk dari halaman produk.
2. **Sistem**: Mengambil detail produk dari database.
3. **Sistem**: Mengambil gambar produk.
4. **Sistem**: Mengambil informasi toko.
5. **Sistem**: Mengambil produk terkait.
6. **Sistem**: Menampilkan halaman detail produk dengan informasi lengkap.
7. **Pengguna**: Melihat informasi produk (nama, harga, deskripsi, dll).
8. **Pengguna**: Melihat galeri gambar produk.
9. **Pengguna**: Memilih gambar berbeda untuk dilihat.
10. **Sistem**: Menampilkan gambar yang dipilih sebagai gambar utama.
11. **Pengguna**: Melihat informasi toko penjual.
12. **Sistem**: Menampilkan detail toko.
13. **Pengguna**: Melihat produk terkait.
14. **Sistem**: Menampilkan daftar produk terkait.

## Ekstensi
1. **Langkah 2: Produk tidak ditemukan**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menyarankan produk alternatif atau mengarahkan kembali ke halaman produk.
2. **Langkah 3-5: Gagal mengambil data terkait**
   * Sistem menampilkan apa yang tersedia dan menunjukkan indikator loading untuk data yang belum dimuat.
   * Sistem mencoba mengambil data kembali setelah interval tertentu.
3. **Langkah 8: Tidak ada gambar produk**
   * Sistem menampilkan gambar placeholder.
4. **Langkah 13: Tidak ada produk terkait**
   * Sistem menyembunyikan bagian produk terkait.

## Persyaratan Khusus
1. Galeri gambar harus mendukung zoom dan navigasi.
2. Halaman detail produk harus responsif di semua ukuran layar.
3. Waktu loading halaman tidak boleh lebih dari 2 detik.
4. Informasi harga harus selalu terlihat bahkan saat menggulir halaman.

## Variasi Teknologi dan Data
1. Menggunakan Next.js untuk mengambil dan menampilkan data produk.
2. Galeri gambar menggunakan komponen interaktif.
3. Caching data produk untuk pemuatan yang lebih cepat.
4. Menggunakan optimasi gambar untuk kecepatan loading.

## Frekuensi Kejadian
Sangat sering - Ini adalah langkah penting dalam alur pembelian.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur ulasan produk dan rating.
2. Perlu ditambahkan fitur pembagian produk ke media sosial.
3. Sistem perlu melacak produk yang paling sering dilihat untuk analitik.
