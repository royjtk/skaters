# Operation Contract: Create Store

## 1. Operation
**Operation: createStore(userId, name, description?)**

**Cross References:**
- Use Case: Create Store
- SSD: Create Store - System Sequence Diagram

**Preconditions:**
- Pengguna sudah login ke sistem
- Pengguna memiliki akun yang terverifikasi
- Nama toko belum digunakan oleh toko lain
- Nama toko memenuhi persyaratan (3-50 karakter)

**Postconditions:**
- Toko baru dibuat di database
- Toko dikaitkan dengan akun pengguna (userId)
- ID unik dibuat untuk toko
- Nama dan deskripsi toko disimpan
- Stempel waktu pembuatan toko disimpan
- URL slug untuk toko dibuat berdasarkan nama
- Pengguna diarahkan ke dashboard toko baru
- Status pengguna diperbarui sebagai "store owner"
- Toko diatur sebagai "aktif" dalam database
