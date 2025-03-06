# Backend Debugging Notes

## 📌 Database Debugging

### **1. Masalah: Tidak Bisa Koneksi ke Database**
**Penyebab:**
- Kredensial salah.
- Database server tidak berjalan.
- Firewall atau port tertutup.

**Solusi:**
✅ Pastikan database server berjalan:
```sh
sudo systemctl status mysql  # Untuk MySQL
sudo systemctl status postgresql  # Untuk PostgreSQL
```
✅ Cek kredensial di `.env` atau config:
```env
DB_HOST=127.0.0.1
DB_DATABASE=mydatabase
DB_USERNAME=root
DB_PASSWORD=
```
✅ Pastikan firewall tidak memblokir koneksi:
```sh
sudo ufw allow 3306 # MySQL
sudo ufw allow 5432 # PostgreSQL
```

🔥 **Jika ada masalah lain, tambahkan ke dalam file ini!** 🚀
