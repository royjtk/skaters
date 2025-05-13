# Operation Contract: Manage Cart Items

## 1. Operation
**Operation: updateCartItem(productId, quantity)**

**Cross References:**
- Use Case: Manage Cart Items
- SSD: Manage Cart Items - System Sequence Diagram

**Preconditions:**
- Produk dengan ID yang ditentukan ada di keranjang pengguna
- LocalStorage tersedia dan berisi data keranjang
- Kuantitas baru valid (bilangan bulat positif)

**Postconditions:**
- Kuantitas produk di keranjang diperbarui
- Total harga keranjang dihitung ulang
- Data keranjang diperbarui di localStorage
- Tampilan keranjang diperbarui dengan kuantitas dan total baru
- Jika kuantitas diatur ke 0, item dihapus dari keranjang

## 2. Operation
**Operation: removeCartItem(productId)**

**Cross References:**
- Use Case: Manage Cart Items
- SSD: Manage Cart Items - System Sequence Diagram

**Preconditions:**
- Produk dengan ID yang ditentukan ada di keranjang pengguna
- LocalStorage tersedia dan berisi data keranjang

**Postconditions:**
- Item dihapus dari keranjang belanja
- Total harga keranjang dihitung ulang
- Data keranjang diperbarui di localStorage
- Tampilan keranjang diperbarui tanpa item yang dihapus
- Jumlah item di ikon keranjang diperbarui
- Jika keranjang menjadi kosong, pesan "Keranjang Kosong" ditampilkan
