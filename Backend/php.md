# Backend Debugging Notes

## 📌 PHP Debugging

### **1. Masalah: Halaman Blank atau Error 500**
**Penyebab:**
- PHP error reporting tidak aktif.
- File `.htaccess` memiliki kesalahan.

**Solusi:**
✅ Aktifkan error reporting:
```php
ini_set('display_errors', 1);
error_reporting(E_ALL);
```
✅ Periksa error log:
```sh
tail -f /var/log/apache2/error.log # Untuk Apache
tail -f /var/log/nginx/error.log # Untuk Nginx
```
✅ Periksa `.htaccess` untuk sintaks yang salah.

🔥 **Jika ada masalah lain, tambahkan ke dalam file ini!** 🚀
