# Use Case Fully Dressed: Sign Up

## Nama Use Case
Sign Up

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer atau Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin mendaftar ke sistem dengan mudah dan cepat.
2. **Store Owner**: Ingin mendaftar untuk membuat toko dan menjual produk.
3. **Platform Skaters**: Ingin mendapatkan pengguna baru dan memperluas basis pengguna.
4. **Sistem**: Memerlukan informasi pengguna yang valid untuk autentikasi dan otorisasi.

## Prasyarat
1. Pengguna memiliki akses ke internet.
2. Pengguna memiliki akun Google yang valid.
3. Sistem autentikasi (OAuth provider) berfungsi dengan baik.

## Jaminan Kesuksesan
Akun baru berhasil dibuat dan pengguna dapat login ke sistem dengan kredensial mereka.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengakses halaman pendaftaran (Sign Up).
2. **Sistem**: Menampilkan opsi pendaftaran.
3. **Pengguna**: Memilih pendaftaran menggunakan Google.
4. **Sistem**: Mengarahkan pengguna ke halaman otorisasi Google.
5. **Pengguna**: Mengizinkan aplikasi untuk mengakses informasi Google.
6. **Sistem**: Menerima token OAuth.
7. **Sistem**: Memvalidasi token.
8. **Sistem**: Memeriksa apakah pengguna sudah ada di database.
9. **Sistem**: Membuat catatan pengguna baru jika belum ada.
10. **Sistem**: Menghasilkan profil pengguna.
11. **Sistem**: Membuat sesi autentikasi.
12. **Sistem**: Mengarahkan pengguna ke halaman onboarding atau halaman utama.

## Ekstensi
1. **Langkah 4-5: Pengguna membatalkan otorisasi**
   * Sistem menampilkan pesan bahwa pendaftaran dibatalkan.
   * Pengguna kembali ke halaman pendaftaran.
2. **Langkah 7: Token tidak valid**
   * Sistem menampilkan pesan kesalahan.
   * Pengguna diminta untuk mencoba lagi.
3. **Langkah 8: Pengguna sudah terdaftar**
   * Sistem memperbarui informasi autentikasi.
   * Sistem membuat sesi autentikasi.
   * Sistem mengarahkan pengguna ke halaman utama.

## Persyaratan Khusus
1. Proses pendaftaran harus selesai dalam waktu kurang dari 10 detik.
2. Sistem harus memberikan umpan balik visual selama proses pendaftaran.
3. Data pengguna yang sensitif harus dienkripsi.
4. Sistem harus menerapkan proteksi terhadap serangan pendaftaran otomatis.

## Variasi Teknologi dan Data
1. Autentikasi menggunakan Google OAuth.
2. Penyimpanan data pengguna menggunakan Prisma dan database SQL.
3. Penggunaan JWT untuk manajemen sesi.
4. Penggunaan NextAuth untuk autentikasi.

## Frekuensi Kejadian
Sering - Ini adalah entry point utama untuk pengguna baru di platform.

## Lain-lain
1. Perlu dipertimbangkan untuk menambahkan metode pendaftaran alternatif di masa mendatang.
2. Sistem perlu meminta informasi tambahan setelah pendaftaran awal (onboarding).
3. Perlu dipertimbangkan untuk menambahkan verifikasi email untuk meningkatkan keamanan.
