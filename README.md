# 🎂 Sistem Operasional Bolu 

![Version](https://img.shields.io/badge/Version-1.0%20Beta-blue)
![Status](https://img.shields.io/badge/Status-Active_Development-success)
![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20PWA-orange)

Aplikasi Web Manajemen Operasional komprehensif yang dirancang khusus untuk bisnis *bakery* (Bolu Sakinah). Sistem ini memfasilitasi manajemen pesanan, kalkulasi HPP (Harga Pokok Penjualan), pelacakan stok bahan baku, pencatatan buku kas, hingga pembuatan struk kasir/laporan PDF secara dinamis.

Dibuat menggunakan antarmuka yang sangat responsif, mendukung tampilan *Mobile-First*, dan dilengkapi fitur *Cloud Sync* secara *Real-Time*.

---

## ✨ Fitur Utama

### 🔐 Sistem Autentikasi Multi-Role
* **Role Owner:** Akses penuh ke seluruh sistem termasuk Pengaturan Master Data, Buku Kas, dan Dashboard Keuangan.
* **Role Pegawai:** Akses terbatas menggunakan PIN (hanya dapat mengakses halaman Pesanan dan Checklist/Penggunaan Bahan).
* **Manajemen Akun:** Owner dapat menambah/menghapus akun pegawai serta mereset PIN pegawai.

### 📦 Manajemen Pesanan Pelanggan
* Pencatatan pesanan dengan dukungan *multi-variant* (satu pesanan bisa terdiri dari berbagai jenis bolu).
* Tampilan UI yang responsif (berubah menjadi bentuk *card* di perangkat *mobile* agar tidak terpotong).
* Perhitungan otomatis konversi total pesanan menjadi satuan Loyang, Pak, dan Kresek.

### 🏭 Kalkulasi HPP & Stok Bahan Baku
* **Manajemen Resep Master:** Atur rasio 1 Adonan = ? Loyang = ? Pcs, serta takaran gramasi/pcs bahan baku per adonan.
* **Integrasi Stok Otomatis:** Setiap kali produksi/penggunaan bahan disimpan, stok di gudang akan terpotong secara otomatis.
* Kalkulasi biaya pembelanjaan bahan harian (HPP) berdasarkan harga *real-time* bahan baku.

### 🧾 Checklist Penggunaan Bahan (Fitur Thermal Print)
* Pegawai dapat memasukkan beberapa varian bolu sekaligus yang akan diproduksi.
* Sistem otomatis menghitung total seluruh bahan baku yang harus disiapkan.
* **Export ke PDF Thermal (58mm):** Otomatis menghasilkan laporan penggunaan bahan berupa struk kasir (ukuran lebar 58mm) yang memanjang secara dinamis sesuai jumlah varian bolu yang diinput.

### 💰 Buku Kas & Dashboard Analitik
* Dasbor pintar dengan ringkasan laba rugi harian.
* **Smart Insights & Chart:** Visualisasi tren pergerakan kas menggunakan grafik interaktif.
* Sinkronisasi Laba Kotor produksi harian ke dalam Buku Kas hanya dengan satu tombol.
* **Export Keuangan:** Laporan kas dapat diunduh ke dalam format `.CSV` (Excel) dan `.PDF`.

### ☁️ Fitur Tambahan
* **Offline Support & PWA:** Terdaftar sebagai *Progressive Web App* dan mendukung *Firestore Local Persistence* (tetap bisa digunakan meski jaringan terputus sementara).
* **Activity Log:** Rekam jejak seluruh aktivitas (CREATE, UPDATE, DELETE) di dalam sistem.

---

## 🛠️ Teknologi yang Digunakan

* **Frontend:** HTML5, CSS3 (Custom Properties, Flexbox, Grid), Vanilla JavaScript.
* **Backend / Database:** [Firebase Firestore](https://firebase.google.com/docs/firestore) (BaaS untuk *Real-time Database* & Autentikasi).
* **Library Eksternal:**
  * [jsPDF](https://parall.ax/products/jspdf) & [jsPDF-AutoTable](https://github.com/simonbengtsson/jsPDF-AutoTable) (Untuk *generate* dokumen dan struk PDF di *client-side*).
  * [Chart.js](https://www.chartjs.org/) (Untuk visualisasi grafik Buku Kas).
  * [FontAwesome 6](https://fontawesome.com/) (Untuk ikon antarmuka).
* **Font:** Plus Jakarta Sans (Google Fonts).

---
