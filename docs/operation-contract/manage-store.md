# Operation Contract: Manage Store

## 1. Operation
**Operation: updateStore(storeId, updatedData)**

**Cross References:**
- Use Case: Manage Store
- SSD: Manage Store - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Toko dengan ID yang ditentukan ada dalam database
- Toko dimiliki oleh Store Owner yang sedang login
- Data toko yang diperbarui valid (nama, deskripsi, dll.)

**Postconditions:**
- Informasi toko diperbarui dalam database
- Jika nama toko diubah, nama tersebut diverifikasi agar tetap unik
- Stempel waktu pembaruan toko diperbarui
- Store Owner diarahkan kembali ke dashboard toko
- Notifikasi sukses ditampilkan
- Perubahan informasi toko terlihat oleh pelanggan

## 2. Operation
**Operation: viewStoreAnalytics(storeId, period?)**

**Cross References:**
- Use Case: Manage Store
- SSD: Manage Store - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Toko dengan ID yang ditentukan ada dalam database
- Toko dimiliki oleh Store Owner yang sedang login

**Postconditions:**
- Data analitik toko diambil dari database (pesanan, produk, pengunjung)
- Statistik penjualan dihitung berdasarkan periode yang ditentukan
- Produk paling populer diidentifikasi dan ditampilkan
- Grafik dan visualisasi analitik dibuat dan ditampilkan
- Dashboard analitik ditampilkan kepada Store Owner
- Data diorganisir berdasarkan periode waktu yang ditentukan
