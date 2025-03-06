# Frontend Debugging Notes

## 📌 WordPress CSS Debugging

### **1. Masalah: Perubahan CSS Tidak Muncul di WordPress**
**Penyebab:**
- Cache browser atau plugin caching masih menyimpan versi lama CSS.
- File CSS tidak di-load dengan benar oleh tema atau plugin.
- WordPress tidak mengenali perubahan karena versi CSS tidak diperbarui.

**Solusi:**
✅ Bersihkan cache browser atau plugin caching seperti **WP Super Cache** atau **W3 Total Cache**.  
✅ Periksa apakah file CSS dimuat di dalam tema WordPress (`functions.php`):
```php
function custom_enqueue_styles() {
    wp_enqueue_style('custom-style', get_stylesheet_uri(), array(), filemtime(get_template_directory() . '/style.css'));
}
add_action('wp_enqueue_scripts', 'custom_enqueue_styles');
```
✅ Pastikan perubahan muncul dengan menambahkan query string versi:
```html
<link rel="stylesheet" href="style.css?v=123">
```
✅ Gunakan **Inspect Element** (`F12`) untuk melihat apakah file CSS dimuat dengan benar.
