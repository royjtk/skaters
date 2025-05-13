# Use Case Fully Dressed: Send Notifications

## Nama Use Case
Send Notifications

## Ruang Lingkup
Sistem E-Commerce Skaters

## Level
Sistem

## Aktor Utama
Sistem (Layanan Notifikasi)

## Pemangku Kepentingan dan Kepentingan
1. **Customer**: Ingin menerima pemberitahuan yang relevan tentang pesanan dan aktivitas mereka.
2. **Store Owner**: Ingin pelanggan mendapatkan informasi yang tepat waktu tentang pesanan.
3. **Platform Skaters**: Ingin menjaga komunikasi yang efektif dengan pengguna.

## Prasyarat
1. Peristiwa yang memicu notifikasi telah terjadi (misalnya, konfirmasi pesanan, perubahan status, dll).
2. Data yang diperlukan untuk notifikasi tersedia.
3. Layanan email atau kanal notifikasi lain berfungsi dengan baik.

## Jaminan Kesuksesan
Notifikasi yang relevan dan informatif berhasil dikirim ke penerima yang dituju.

## Skenario Utama Keberhasilan
1. **Sistem**: Menerima pemicu peristiwa untuk notifikasi.
2. **Sistem**: Mengambil detail peristiwa dari database.
3. **Sistem**: Mengidentifikasi jenis notifikasi yang diperlukan.
4. **Sistem**: Mengambil data yang relevan berdasarkan jenis peristiwa.

5. **Jika Konfirmasi Pesanan:**
   * **Sistem**: Mengambil detail pesanan.
   * **Sistem**: Menghasilkan template konfirmasi pesanan.
   * **Sistem**: Mengirim email konfirmasi pesanan.

6. **Jika Perubahan Status Pesanan:**
   * **Sistem**: Mengambil informasi status pesanan.
   * **Sistem**: Menghasilkan template pembaruan status.
   * **Sistem**: Mengirim email pembaruan status.

7. **Jika Konfirmasi Pembayaran:**
   * **Sistem**: Mengambil detail pembayaran.
   * **Sistem**: Menghasilkan template bukti pembayaran.
   * **Sistem**: Mengirim email konfirmasi pembayaran.

8. **Sistem**: Menerima konfirmasi pengiriman dari layanan email.
9. **Sistem**: Mencatat notifikasi dalam database.

## Ekstensi
1. **Langkah 2-4: Gagal mengambil data yang diperlukan**
   * Sistem mencatat kesalahan.
   * Sistem mengirim notifikasi dengan data minimal yang tersedia.
   * Sistem menandai untuk tindak lanjut manual jika diperlukan.
2. **Langkah 5-7: Gagal menghasilkan template**
   * Sistem menggunakan template default.
   * Sistem mencatat kesalahan untuk perbaikan template.
3. **Langkah 5-7: Gagal mengirim email**
   * Sistem mencatat kegagalan pengiriman.
   * Sistem menandai untuk percobaan ulang nanti.
   * Setelah beberapa percobaan gagal, sistem memperingatkan administrator.

## Persyaratan Khusus
1. Notifikasi email harus dikirim dalam waktu kurang dari 5 menit setelah peristiwa pemicu.
2. Template notifikasi harus responsif dan terlihat baik di semua perangkat.
3. Sistem harus mendukung personalisasi dasar (nama pengguna, detail pesanan, dll).
4. Semua notifikasi harus sesuai dengan peraturan anti-spam.

## Variasi Teknologi dan Data
1. Penggunaan layanan email untuk pengiriman email otomatis.
2. Template email dibuat menggunakan HTML yang responsif.
3. Pencatatan notifikasi menggunakan database untuk melacak riwayat komunikasi.
4. Implementasi sistem antrian untuk mengelola volume notifikasi tinggi.

## Frekuensi Kejadian
Sangat sering - Notifikasi dikirim untuk berbagai peristiwa dalam sistem.

## Lain-lain
1. Perlu dipertimbangkan untuk mengimplementasikan notifikasi push untuk aplikasi web/mobile di masa mendatang.
2. Sistem perlu memiliki mekanisme untuk pengguna mengelola preferensi notifikasi.
3. Perlu dipertimbangkan untuk menambahkan notifikasi SMS untuk peristiwa penting.
4. Sistem perlu menghormati pengaturan "opt-out" untuk jenis notifikasi tertentu.
