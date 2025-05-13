# Operation Contract: Add Product

## 1. Operation
**Operation: addProduct(storeId, productData, images)**

**Cross References:**
- Use Case: Add Product
- SSD: Add Product - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Toko dengan ID yang ditentukan ada dan dimiliki oleh Store Owner
- Data produk valid (nama, deskripsi, harga, kategori, dll.)
- Minimal satu gambar disediakan untuk produk

**Postconditions:**
- Produk baru dibuat di database dengan ID unik
- Produk dikaitkan dengan toko yang ditentukan
- Gambar produk diunggah ke penyimpanan
- URL gambar disimpan dan dikaitkan dengan produk
- Slug produk dibuat berdasarkan nama produk
- Stempel waktu pembuatan produk disimpan
- Kategori produk diatur sesuai input
- Stok produk diinisialisasi sesuai input
- Produk ditambahkan ke daftar produk toko
- Store Owner diarahkan kembali ke daftar produk
- Notifikasi sukses ditampilkan
