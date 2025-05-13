# Use Case Fully Dressed: Track Order Status

## Nama Use Case
Track Order Status

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin mengetahui status terkini dari pesanan mereka.
2. **Store Owner**: Ingin pelanggan mendapatkan informasi yang akurat tentang status pesanan.
3. **Platform Skaters**: Ingin menyediakan transparansi dalam proses pengiriman dan pemenuhan pesanan.

## Prasyarat
1. Pengguna telah login ke akun mereka.
2. Pengguna memiliki setidaknya satu pesanan aktif.

## Jaminan Kesuksesan
Pengguna dapat melihat dan memahami status terkini dari pesanan mereka dengan informasi yang akurat dan terbaru.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengakses halaman pesanan.
2. **Sistem**: Mengautentikasi pengguna.
3. **Sistem**: Mengambil daftar pesanan pengguna.
4. **Sistem**: Menampilkan daftar pesanan.
5. **Pengguna**: Memilih pesanan tertentu untuk dilacak.
6. **Sistem**: Mengambil detail pesanan.
7. **Sistem**: Mengambil riwayat status pesanan.
8. **Sistem**: Menampilkan informasi status pesanan.
9. **Pengguna**: Melihat status terkini dan riwayat status pesanan.
10. **Pengguna**: Meminta pembaruan status (opsional).
11. **Sistem**: Memeriksa pembaruan status.
12. **Sistem**: Menampilkan status terbaru jika ada perubahan.

## Ekstensi
1. **Langkah 3: Tidak ada pesanan**
   * Sistem menampilkan pesan bahwa pengguna belum memiliki pesanan.
   * Sistem menyarankan untuk menjelajahi produk atau memberikan tautan ke halaman produk.
2. **Langkah 6-7: Gagal mengambil detail atau riwayat status**
   * Sistem menampilkan pesan kesalahan.
   * Sistem menyediakan opsi untuk mencoba lagi.
3. **Langkah 11: Tidak ada pembaruan status**
   * Sistem memberi tahu pengguna bahwa status belum berubah sejak terakhir dilihat.

## Persyaratan Khusus
1. Status pesanan harus diperbarui secara real-time atau setidaknya setiap 15 menit.
2. Tampilan status harus jelas dan mudah dipahami dengan indikator visual.
3. Sistem harus dapat menangani berbagai status pesanan (dalam proses, dikirim, selesai, dibatalkan, dll).
4. Perubahan status harus dicatat dengan stempel waktu.

## Variasi Teknologi dan Data
1. Menggunakan websocket atau polling untuk pembaruan status real-time.
2. Status pesanan disimpan dalam database dengan relasi ke pesanan.
3. Notifikasi push untuk perubahan status penting.
4. Integrasi dengan sistem pelacakan pengiriman jika diperlukan.

## Frekuensi Kejadian
Sering - Pelanggan biasanya melacak status pesanan mereka beberapa kali setelah melakukan pembelian.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan fitur notifikasi email atau SMS untuk pembaruan status.
2. Sistem perlu menyediakan informasi kontak jika pelanggan memiliki pertanyaan tentang pesanan.
3. Perlu dipertimbangkan untuk mengintegrasikan dengan peta pelacakan untuk pengiriman yang sedang berlangsung.
