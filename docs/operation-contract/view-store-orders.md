# Operation Contract: View Store Orders

## 1. Operation
**Operation: viewStoreOrders(storeId, status?, page?)**

**Cross References:**
- Use Case: View Store Orders
- SSD: View Store Orders - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Toko dengan ID yang ditentukan ada dalam database
- Toko dimiliki oleh Store Owner yang sedang login

**Postconditions:**
- Pesanan toko diambil dari database
- Pesanan ditampilkan dengan urutan terbaru lebih dahulu
- Jika parameter status diberikan, hanya pesanan dengan status tersebut yang ditampilkan
- Daftar pesanan ditampilkan dengan informasi singkat (ID, tanggal, status, total)
- Sistem siap untuk memuat pesanan tambahan jika diperlukan (pagination)
- Filter status tersedia untuk memfilter pesanan berdasarkan statusnya

## 2. Operation
**Operation: updateOrderStatus(orderId, storeId, newStatus)**

**Cross References:**
- Use Case: View Store Orders
- SSD: View Store Orders - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Pesanan dengan ID yang ditentukan ada dalam database
- Pesanan terkait dengan toko yang dimiliki oleh Store Owner
- Status baru valid (misalnya: "processing", "shipped", "delivered")

**Postconditions:**
- Status pesanan diperbarui dalam database
- Riwayat status pesanan dicatat dengan stempel waktu
- Notifikasi perubahan status dibuat untuk pelanggan
- Email pembaruan status dikirim ke pelanggan
- Konfirmasi pembaruan status ditampilkan ke Store Owner
- Tampilan pesanan diperbarui dengan status baru
