# Backend Debugging Notes

## 📌 API Debugging

### **1. Masalah: CORS Error**
**Penyebab:**
- Server tidak mengizinkan cross-origin requests.

**Solusi:**
✅ Tambahkan header CORS di backend:
```php
header("Access-Control-Allow-Origin: *");
header("Access-Control-Allow-Methods: GET, POST, OPTIONS");
```
✅ Jika menggunakan Express.js:
```js
const cors = require('cors');
app.use(cors());
```
✅ Pastikan frontend dan backend berjalan di domain yang sesuai.

🔥 **Jika ada masalah lain, tambahkan ke dalam file ini!** 🚀
