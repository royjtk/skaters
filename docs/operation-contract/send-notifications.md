# Operation Contract: Send Notifications

## 1. Operation
**Operation: sendOrderConfirmation(orderId, userId, email)**

**Cross References:**
- Use Case: Send Notifications
- SSD: Send Notifications - System Sequence Diagram

**Preconditions:**
- Pesanan dengan ID yang ditentukan telah dibuat
- Data pesanan lengkap dan valid
- Email pengguna valid dan tersedia

**Postconditions:**
- Template konfirmasi pesanan diambil dan diisi dengan data pesanan
- Email konfirmasi dikirim ke alamat pengguna
- Notifikasi dicatat dalam database sebagai "terkirim"
- Status pemberitahuan pesanan diperbarui
- Email berisi detail pesanan, jumlah total, dan langkah selanjutnya

## 2. Operation
**Operation: sendStatusUpdate(orderId, userId, email, newStatus)**

**Cross References:**
- Use Case: Send Notifications
- SSD: Send Notifications - System Sequence Diagram

**Preconditions:**
- Pesanan dengan ID yang ditentukan ada dalam database
- Status pesanan telah berubah
- Email pengguna valid dan tersedia

**Postconditions:**
- Template pembaruan status diambil dan diisi dengan data pesanan dan status baru
- Email pembaruan status dikirim ke alamat pengguna
- Notifikasi dicatat dalam database sebagai "terkirim"
- Status pemberitahuan pesanan diperbarui
- Email berisi informasi status baru dan tindakan yang mungkin diperlukan

## 3. Operation
**Operation: sendPaymentConfirmation(orderId, userId, email, paymentDetails)**

**Cross References:**
- Use Case: Send Notifications
- SSD: Send Notifications - System Sequence Diagram

**Preconditions:**
- Pesanan dengan ID yang ditentukan ada dalam database
- Pembayaran untuk pesanan telah berhasil diproses
- Detail pembayaran tersedia
- Email pengguna valid dan tersedia

**Postconditions:**
- Template konfirmasi pembayaran diambil dan diisi dengan data pembayaran
- Email konfirmasi pembayaran dikirim ke alamat pengguna
- Notifikasi dicatat dalam database sebagai "terkirim"
- Status pemberitahuan pembayaran diperbarui
- Email berisi detail pembayaran, tanggal, dan rincian pesanan terkait
