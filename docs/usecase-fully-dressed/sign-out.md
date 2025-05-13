# Use Case Fully Dressed: Sign Out

## Nama Use Case
Sign Out

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Pengguna

## Aktor Utama
Customer atau Store Owner

## Pemangku Kepentingan dan Kepentingan
1. **Customer/Store Owner**: Ingin keluar dari sistem dengan aman dan mengakhiri sesi.
2. **Sistem**: Ingin memastikan sesi pengguna diakhiri dengan benar untuk keamanan.
3. **Platform Skaters**: Ingin menyediakan pengalaman akhir yang positif bagi pengguna.

## Prasyarat
1. Pengguna telah login ke sistem (memiliki sesi aktif).
2. Semua perubahan yang belum disimpan telah diproses atau ditangani.

## Jaminan Kesuksesan
Sesi pengguna berhasil diakhiri dan pengguna keluar dari akun dengan aman.

## Skenario Utama Keberhasilan
1. **Pengguna**: Mengklik tombol "Keluar" atau "Sign Out".
2. **Sistem**: Memvalidasi sesi pengguna.
3. **Sistem**: Menginvalidasi token sesi.
4. **Sistem**: Menghapus cookie autentikasi.
5. **Sistem**: Menghapus konteks pengguna dari aplikasi.
6. **Sistem**: Mengarahkan pengguna ke halaman utama.
7. **Sistem**: Menampilkan status bahwa pengguna telah keluar.

## Ekstensi
1. **Langkah 2: Validasi sesi gagal**
   * Sistem mencatat kesalahan.
   * Sistem tetap melanjutkan dengan menghapus cookie dan konteks pengguna.
   * Sistem menampilkan pesan bahwa pengguna telah keluar.
2. **Langkah 3-4: Gagal menginvalidasi sesi/menghapus cookie**
   * Sistem mencatat kesalahan.
   * Sistem tetap mengarahkan pengguna ke halaman utama.
   * Sistem menyarankan pengguna untuk membersihkan cache browser.

## Persyaratan Khusus
1. Proses logout harus selesai dalam waktu kurang dari 2 detik.
2. Semua token dan cookie autentikasi harus dihapus sepenuhnya.
3. Sistem harus menampilkan konfirmasi visual bahwa logout berhasil.
4. Logout harus tersedia dari semua halaman yang diakses pengguna yang masuk.

## Variasi Teknologi dan Data
1. Penggunaan NextAuth untuk mengelola sesi.
2. Penghapusan token JWT.
3. Penggunaan cookies untuk menyimpan status autentikasi.
4. Implementasi client-side state management untuk konteks pengguna.

## Frekuensi Kejadian
Sering - Pengguna secara teratur keluar dari sistem setelah menyelesaikan aktivitas.

## Lain-lain
1. Sistem perlu mempertimbangkan logout otomatis setelah periode tidak aktif tertentu.
2. Perlu dipertimbangkan untuk menambahkan konfirmasi logout untuk mencegah logout yang tidak disengaja.
3. Logout harus mengarahkan pengguna ke halaman yang sesuai berdasarkan konteks (misalnya, halaman utama atau halaman login).
