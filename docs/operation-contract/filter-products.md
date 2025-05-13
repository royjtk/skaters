# Operation Contract: Filter Products by Category

## 1. Operation
**Operation: filterProductsByCategory(categorySlug)**

**Cross References:**
- Use Case: Filter Products by Category
- SSD: Filter Products by Category - System Sequence Diagram

**Preconditions:**
- Sistem database aktif dan dapat diakses
- Kategori produk tersedia di sistem
- Produk dengan kategori tersebut ada di database

**Postconditions:**
- Parameter URL diperbarui dengan kategori yang dipilih
- Hanya produk dengan kategori yang dipilih ditampilkan
- Daftar produk diurutkan sesuai kriteria default (terbaru)
- Jumlah produk awal ditampilkan sesuai limit (default: 8 produk)
- Sistem siap untuk memuat produk tambahan jika pengguna menggulir ke bawah
- Jika tidak ada produk dalam kategori, pesan informasi ditampilkan
- Jika filter dihapus, semua produk ditampilkan kembali
- Parameter kategori dihapus dari URL jika filter dihapus
