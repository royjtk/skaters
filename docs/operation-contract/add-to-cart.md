# Operation Contract: Add to Cart

## 1. Operation
**Operation: addToCart(product)**

**Cross References:**
- Use Case: Add to Cart
- SSD: Add to Cart - System Sequence Diagram

**Preconditions:**
- Produk dengan ID yang ditentukan ada dan tersedia
- Halaman detail produk ditampilkan kepada pengguna
- LocalStorage tersedia di browser pengguna

**Postconditions:**
- Produk ditambahkan ke keranjang belanja di localStorage
- Jika produk sudah ada di keranjang, tidak ada tindakan tambahan yang dilakukan
- Jumlah item di ikon keranjang diperbarui
- Notifikasi sukses ditampilkan kepada pengguna
- Data keranjang disimpan di localStorage
- Produk tersedia untuk checkout nantinya
- Status UI diperbarui untuk menunjukkan bahwa produk ada di keranjang
