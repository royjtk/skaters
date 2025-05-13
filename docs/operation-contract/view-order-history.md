# Operation Contract: View Order History

## 1. Operation
**Operation: viewOrderHistory(userId, page?, status?)**

**Cross References:**
- Use Case: View Order History
- SSD: View Order History - System Sequence Diagram

**Preconditions:**
- Pengguna sudah login ke sistem
- Pengguna memiliki setidaknya satu pesanan di database
- Pengguna memiliki akses ke pesanannya sendiri

**Postconditions:**
- Pesanan pengguna diambil dari database
- Pesanan ditampilkan dengan urutan terbaru lebih dahulu
- Jika parameter status diberikan, hanya pesanan dengan status tersebut yang ditampilkan
- Daftar pesanan ditampilkan dengan informasi singkat (ID, tanggal, status, total)
- Sistem siap untuk memuat pesanan tambahan jika diperlukan (pagination)
- Jika tidak ada pesanan, pesan informasi ditampilkan
- Filter status tersedia untuk memfilter pesanan berdasarkan statusnya
- Pengguna dapat mengklik pesanan untuk melihat detail lebih lanjut
