# Use Case Fully Dressed: Add to Cart

## Nama Use Case
Add to Cart

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin menambahkan produk ke keranjang belanja untuk nantinya dibeli.
2. **Store Owner**: Ingin produk mereka dapat ditambahkan ke keranjang belanja.
3. **Sistem**: Menyediakan pengalaman belanja yang lancar dan dapat diandalkan.

## Prasyarat
1. Pengguna harus berada di halaman detail produk.
2. Produk tersebut harus tersedia (tidak habis stok).

## Jaminan Kesuksesan
Produk berhasil ditambahkan ke keranjang belanja pengguna, dan pengguna menerima konfirmasi tentang penambahan tersebut.

## Skenario Utama Keberhasilan
1. **Pengguna**: Melihat halaman detail produk.
2. **Sistem**: Menampilkan informasi produk termasuk nama, gambar, deskripsi, harga, dan tombol "Tambahkan ke Keranjang".
3. **Pengguna**: Mengklik tombol "Tambahkan ke Keranjang".
4. **Sistem**: Menambahkan produk ke localStorage pengguna.
5. **Sistem**: Memperbarui tampilan ikon keranjang dengan jumlah item.
6. **Sistem**: Menampilkan notifikasi bahwa produk berhasil ditambahkan.
7. **Pengguna**: Dapat melanjutkan melihat produk lain atau melihat keranjang belanja.

## Ekstensi
1. **Langkah 3: Produk sudah ada di keranjang**
   * Sistem tidak menambahkan produk baru, tetapi menampilkan notifikasi bahwa produk sudah ada di keranjang.
2. **Langkah 4: Gagal menambahkan ke localStorage**
   * Sistem menampilkan pesan kesalahan.
   * Menyarankan pengguna untuk memeriksa pengaturan browser.
3. **Langkah 3: Produk tidak tersedia (habis stok)**
   * Sistem menampilkan pesan bahwa produk tidak tersedia.
   * Tombol "Tambahkan ke Keranjang" dinonaktifkan.

## Persyaratan Khusus
1. Proses penambahan ke keranjang harus instan (kurang dari 1 detik).
2. Notifikasi harus terlihat jelas tetapi tidak mengganggu pengalaman pengguna.
3. Sistem harus mampu mengelola berbagai ukuran keranjang belanja.

## Variasi Teknologi dan Data
1. Data keranjang disimpan di localStorage browser.
2. Menggunakan Zustand untuk manajemen state.
3. Menggunakan animasi untuk meningkatkan pengalaman pengguna.

## Frekuensi Kejadian
Sangat sering - Setiap pengguna akan menambahkan beberapa produk ke keranjang belanja ketika berbelanja.

## Lain-lain
1. Keranjang belanja harus tetap ada bahkan setelah pengguna menutup browser.
2. Sistem harus memastikan konsistensi antara data produk yang ditampilkan dan yang disimpan di keranjang.
3. Desain tombol "Tambahkan ke Keranjang" harus mengikuti prinsip-prinsip UI/UX yang baik.
