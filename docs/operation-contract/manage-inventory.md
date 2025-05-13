# Operation Contract: Manage Product Inventory

## 1. Operation
**Operation: updateProductInventory(productId, storeId, quantity)**

**Cross References:**
- Use Case: Manage Product Inventory
- SSD: Manage Product Inventory - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Produk dengan ID yang ditentukan ada dalam database
- Produk milik toko yang dimiliki oleh Store Owner
- Nilai kuantitas baru valid (bilangan bulat positif atau nol)

**Postconditions:**
- Jumlah stok produk diperbarui dalam database
- Jika stok diatur ke 0, status produk diperbarui menjadi "Stok Habis"
- Jika stok lebih dari 0, status ketersediaan diperbarui jika perlu
- Stempel waktu pembaruan inventaris disimpan
- Notifikasi sukses ditampilkan
- Jika stok di bawah ambang batas minimum, peringatan stok rendah ditampilkan

## 2. Operation
**Operation: toggleProductVisibility(productId, storeId, isArchived)**

**Cross References:**
- Use Case: Manage Product Inventory
- SSD: Manage Product Inventory - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Produk dengan ID yang ditentukan ada dalam database
- Produk milik toko yang dimiliki oleh Store Owner

**Postconditions:**
- Status arsip produk diubah sesuai parameter isArchived
- Jika isArchived = true, produk tidak lagi ditampilkan di toko
- Jika isArchived = false, produk ditampilkan di toko
- Status produk diperbarui dalam database
- Stempel waktu pembaruan diperbarui
- Notifikasi sukses ditampilkan
- Tampilan status produk diperbarui di dashboard
