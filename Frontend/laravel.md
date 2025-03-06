# Frontend Debugging Notes

## 📌 Laravel CSS Debugging

### **1. Masalah: CSS Tidak Terdeteksi di Laravel**
**Penyebab:**
- Laravel Mix tidak mengompilasi CSS.
- Path file CSS salah.

**Solusi:**
✅ Jalankan perintah berikut untuk mengompilasi CSS:
```sh
npm run dev
```
✅ Pastikan link CSS ada di `resources/views/layouts/app.blade.php`:
```html
<link href="{{ asset('css/app.css') }}" rel="stylesheet">
```
✅ Gunakan perintah berikut jika ada masalah dengan cache:
```sh
php artisan cache:clear
php artisan view:clear
php artisan config:clear
```

