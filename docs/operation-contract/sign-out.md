# Operation Contract: Sign Out

## 1. Operation
**Operation: signOut()**

**Cross References:**
- Use Case: Sign Out
- SSD: Sign Out - System Sequence Diagram

**Preconditions:**
- Pengguna sudah login ke sistem
- Sesi aktif ada untuk pengguna

**Postconditions:**
- Sesi pengguna diinvalidasi
- Token autentikasi dihapus
- Cookie autentikasi dihapus dari browser
- Konteks pengguna dihapus dari aplikasi
- Pengguna diarahkan ke halaman utama atau login
- Status pengguna di aplikasi diubah menjadi "logged out"
