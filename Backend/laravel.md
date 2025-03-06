# Backend Debugging Notes

## 📌 Laravel Debugging

### **1. Masalah: Route Tidak Ditemukan (404)**
**Penyebab:**
- Route tidak terdaftar dengan benar.
- Cache masih menyimpan versi lama.

**Solusi:**
✅ Pastikan route sudah terdaftar di `routes/web.php` atau `routes/api.php`.  
✅ Hapus cache Laravel:
```sh
php artisan route:clear
php artisan cache:clear
php artisan config:clear
```
✅ Jalankan ulang server:
```sh
php artisan serve
```

🔥 **Jika ada masalah lain, tambahkan ke dalam file ini!** 🚀
