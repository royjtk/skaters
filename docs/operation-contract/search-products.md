# Operation Contract: Search Products

## 1. Operation
**Operation: searchProducts(query)**

**Cross References:**
- Use Case: Search Products
- SSD: Search Products - System Sequence Diagram

**Preconditions:**
- Sistem database aktif dan dapat diakses
- Produk tersedia di database
- Query pencarian tidak kosong

**Postconditions:**
- Produk yang cocok dengan kriteria pencarian diambil dari database
- Hasil pencarian dikelompokkan berdasarkan kategori
- Hasil pencarian ditampilkan kepada pengguna
- Jika tidak ada hasil, pesan "tidak ditemukan" ditampilkan
- Pencarian menghasilkan maksimum 10 hasil per kategori
- Hasil diurutkan berdasarkan tanggal pembuatan (terbaru lebih dahulu)
- URL tidak berubah (pencarian dilakukan tanpa perubahan halaman)
- Jika pengguna memperbaiki query, hasil pencarian diperbarui secara real-time
