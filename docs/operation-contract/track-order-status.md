# Operation Contract: Track Order Status

## 1. Operation
**Operation: trackOrderStatus(orderId)**

**Cross References:**
- Use Case: Track Order Status
- SSD: Track Order Status - System Sequence Diagram

**Preconditions:**
- Pengguna sudah login ke sistem
- Pesanan dengan ID yang ditentukan ada di database
- Pengguna adalah pemilik pesanan tersebut atau Store Owner terkait
- Status pesanan telah diperbarui dalam database

**Postconditions:**
- Detail pesanan diambil dari database
- Riwayat status pesanan diambil dan ditampilkan secara kronologis
- Status terkini ditampilkan dengan indikator visual yang jelas
- Detail pesanan ditampilkan (item, jumlah, harga, alamat pengiriman)
- Jika ada pembaruan status, status terbaru ditampilkan
- Sistem siap untuk memuat pembaruan status real-time jika tersedia
- Jika pesanan dalam proses pengiriman, informasi pengiriman ditampilkan
- Riwayat status mencakup stempel waktu untuk setiap perubahan status
