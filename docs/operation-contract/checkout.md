# Operation Contract: Checkout

## 1. Operation
**Operation: initiateCheckout(items)**

**Cross References:**
- Use Case: Checkout
- SSD: Checkout - System Sequence Diagram

**Preconditions:**
- Pengguna sudah login ke sistem
- Keranjang belanja memiliki minimal satu item
- Item di keranjang valid dan tersedia

**Postconditions:**
- Halaman checkout ditampilkan
- Item keranjang divalidasi (ketersediaan, harga)
- Formulir informasi pengiriman ditampilkan
- Total harga dan detail dihitung dan ditampilkan

## 2. Operation
**Operation: submitOrder(shippingDetails, paymentMethod)**

**Cross References:**
- Use Case: Checkout
- SSD: Checkout - System Sequence Diagram

**Preconditions:**
- Pengguna sudah berada di halaman checkout
- Informasi pengiriman telah diisi dengan benar
- Metode pembayaran telah dipilih

**Postconditions:**
- Pesanan baru dibuat di database
- Item pesanan dibuat untuk setiap produk
- Pembayaran diproses melalui Midtrans
- Stok produk diperbarui sesuai dengan kuantitas yang dibeli
- Keranjang belanja dikosongkan
- Faktur dihasilkan untuk pesanan
- Konfirmasi pesanan ditampilkan kepada pengguna
- Email konfirmasi dikirim ke pengguna
- Status pesanan diatur sebagai "pending" atau "paid" tergantung status pembayaran
