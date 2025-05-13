# Operation Contract: Sign In

## 1. Operation
**Operation: signIn(email, password)**

**Cross References:**
- Use Case: Sign In
- SSD: Sign In - System Sequence Diagram

**Preconditions:**
- Pengguna belum login ke sistem
- Sistem autentikasi aktif
- Pengguna memiliki akun Google yang valid

**Postconditions:**
- Pengguna diautentikasi di sistem
- Sesi baru untuk pengguna dibuat
- Status login pengguna diubah menjadi "logged in"
- Pengguna diarahkan ke halaman utama atau halaman sebelumnya
- Token autentikasi dibuat dan disimpan
- Waktu login terakhir pengguna diperbarui di database
