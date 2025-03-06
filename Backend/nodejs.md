# Backend Debugging Notes

## 📌 Node.js Debugging

### **1. Masalah: Server Tidak Mau Berjalan**
**Penyebab:**
- Port sudah digunakan oleh proses lain.
- Kesalahan dalam kode atau sintaks.
- Modul tidak terinstall.

**Solusi:**
✅ Periksa log error dengan `console.log(err)` atau gunakan debugger bawaan:  
```sh
node --inspect index.js
```
✅ Matikan proses yang memakai port:
```sh
npx kill-port 3000
```
✅ Pastikan semua modul sudah terinstall:
```sh
npm install
```

🔥 **Jika ada masalah lain, tambahkan ke dalam file ini!** 🚀
