# Operation Contract: Generate Invoice

## 1. Operation
**Operation: generateInvoice(orderId)**

**Cross References:**
- Use Case: Generate Invoice
- SSD: Generate Invoice - System Sequence Diagram

**Preconditions:**
- Pesanan dengan ID yang ditentukan ada di database
- Pembayaran untuk pesanan telah berhasil
- Detail pesanan lengkap (item, harga, pelanggan, toko)

**Postconditions:**
- Data faktur diambil dari database (pesanan, item, pelanggan, toko)
- Dokumen faktur dibuat dengan format yang tepat
- Nomor faktur unik dibuat dan ditetapkan
- Perhitungan pajak dan total dilakukan dengan benar
- Faktur disimpan di database dan dikaitkan dengan pesanan
- File PDF faktur dibuat
- PDF faktur dikirim ke email pelanggan
- Link untuk mengunduh faktur tersedia di halaman detail pesanan
- Status faktur diatur ke "issued" di database
- Stempel waktu penerbitan faktur disimpan
