# Operation Contract: Sign Up

## 1. Operation
**Operation: signUp(email, name, password)**

**Cross References:**
- Use Case: Sign Up
- SSD: Sign Up - System Sequence Diagram

**Preconditions:**
- Pengguna belum memiliki akun di sistem
- Sistem pendaftaran aktif
- Pengguna memiliki akun Google yang valid

**Postconditions:**
- Akun baru dibuat untuk pengguna
- Data profil pengguna disimpan di database
- Tabel User memiliki entri baru dengan informasi pengguna
- Sesi autentikasi dibuat
- Pengguna diarahkan ke halaman onboarding atau halaman utama
- Status pengguna diatur sebagai "active"
