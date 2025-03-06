# Frontend Debugging Notes

## 📌 CSS Debugging

### **1. Masalah: CSS Tidak Mempengaruhi Elemen**
**Penyebab:**
- Selector CSS tidak cocok dengan elemen yang dimaksud.
- CSS ter-overwrite oleh style lain.
- Masalah cache browser.

**Solusi:**
✅ Gunakan `!important` jika diperlukan.  
✅ Periksa spesifisitas selector CSS.  
✅ Gunakan `Ctrl + Shift + R` untuk force reload browser.  
✅ Cek dengan **DevTools** (`F12` → Elements → Styles).
