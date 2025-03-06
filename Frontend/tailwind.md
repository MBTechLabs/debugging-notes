# Frontend Debugging Notes

## 📌 Tailwind CSS Debugging

### **1. Masalah: Tailwind Tidak Berfungsi**
**Penyebab:**
- Tailwind tidak terinstall atau belum dikonfigurasi dengan benar.
- Kelas Tailwind tidak dikenali karena `purge` di Tailwind.

**Solusi:**
✅ Pastikan Tailwind sudah terinstall dengan perintah:
```sh
npm install tailwindcss postcss autoprefixer
```
✅ Konfigurasi `tailwind.config.js` agar tidak memfilter class yang tidak digunakan:
```js
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
✅ Pastikan menggunakan kelas secara dinamis (tidak dalam string yang dibangun secara dinamis di JavaScript).
