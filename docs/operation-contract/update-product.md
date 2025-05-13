# Operation Contract: Update Product

## 1. Operation
**Operation: updateProduct(productId, storeId, updatedData, imageChanges)**

**Cross References:**
- Use Case: Update Product
- SSD: Update Product - System Sequence Diagram

**Preconditions:**
- Store Owner telah login ke sistem
- Produk dengan ID yang ditentukan ada dalam database
- Produk milik toko yang dimiliki oleh Store Owner
- Data produk yang diperbarui valid

**Postconditions:**
- Informasi produk diperbarui dalam database
- Jika nama produk diubah, slug produk juga diperbarui
- Jika ada gambar baru, gambar tersebut diunggah ke penyimpanan
- URL gambar baru disimpan dan dikaitkan dengan produk
- Jika ada gambar yang dihapus, gambar tersebut dihapus dari penyimpanan
- Keterkaitan gambar yang dihapus dengan produk dihapus dari database
- Stempel waktu pembaruan produk diperbarui
- Kategori produk diperbarui jika diubah
- Stok produk diperbarui jika diubah
- Store Owner diarahkan kembali ke daftar produk atau detail produk
- Notifikasi sukses ditampilkan
