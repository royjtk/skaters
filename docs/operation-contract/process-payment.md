# Operation Contract: Process Payment

## 1. Operation
**Operation: processPayment(orderId, amount, paymentMethod)**

**Cross References:**
- Use Case: Process Payment
- SSD: Process Payment - System Sequence Diagram

**Preconditions:**
- Pesanan dengan ID yang ditentukan ada di database
- Jumlah pembayaran valid dan sesuai dengan total pesanan
- Metode pembayaran valid dan tersedia
- Koneksi dengan gateway pembayaran (Midtrans) aktif

**Postconditions:**
- Permintaan pembayaran dikirim ke gateway Midtrans
- Status pembayaran diperbarui berdasarkan respons gateway
- Jika pembayaran berhasil:
  - Status pesanan diperbarui menjadi "dibayar" (paid)
  - Faktur dihasilkan
  - Notifikasi pembayaran berhasil dikirim ke pelanggan
  - Notifikasi pesanan baru dikirim ke Store Owner
- Jika pembayaran gagal:
  - Status pesanan diperbarui menjadi "gagal bayar" (payment failed)
  - Notifikasi kegagalan dikirim ke pelanggan
  - Log transaksi mencatat kegagalan dan alasannya
- Transaksi dicatat di log sistem
- Hubungan antara pesanan dan transaksi pembayaran dibuat di database
