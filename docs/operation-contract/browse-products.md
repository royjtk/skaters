# Operation Contract: Browse Products

## 1. Operation
**Operation: browseProducts(categoryId?, page?, limit?)**

**Cross References:**
- Use Case: Browse Products
- SSD: Browse Products - System Sequence Diagram

**Preconditions:**
- Sistem database aktif dan dapat diakses
- Produk tersedia di database
- Kategori produk telah disiapkan di sistem

**Postconditions:**
- Daftar produk diambil dari database sesuai parameter (kategori, halaman, batas)
- Produk ditampilkan kepada pengguna dalam antarmuka yang sesuai
- Jika pengguna mencapai akhir halaman, produk tambahan dimuat (infinite scroll)
- Jumlah produk yang ditampilkan sesuai dengan parameter limit (default: 8 produk)
- Urutan produk ditampilkan sesuai dengan urutan yang ditentukan (biasanya dari terbaru)
- Jika parameter kategori diberikan, hanya produk dalam kategori tersebut yang ditampilkan
