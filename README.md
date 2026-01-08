# 🚀 RFID Audit System: Integrated Stock Opname Solution

Solusi automasi Stock Opname terintegrasi yang menjembatani perangkat keras **Handheld RFID** dengan **n8n Automation Engine** untuk akurasi data aset hingga 100%.

## ✨ Fitur Utama
* **Multi-Format Support:** Mendukung ekspor data `.xls` (APPCenter), `.csv` (Chainway), dan `.xlsx` (Master).
* **Dual-Audit Logic:** Pilihan mode audit berbasis **ASCII (Asset_ID)** atau **HEX (EPC_Refer)**.
* **Automatic Reconciliation:** Logika pembersihan karakter kotor (*null characters*) dan penentuan status **FOUND/MISSING** secara otomatis.
* **Scalable Engine:** Mampu memproses ribuan aset dalam hitungan detik menggunakan n8n.

## 🛠️ Cara Deploy (Self-Hosting)

### 1. Konfigurasi n8n
* Pastikan Anda memiliki instance n8n (Docker/Desktop/Cloud).
* Impor file `RFID AUDIT SYSTEM (ASCII).json & RFID AUDIT SYSTEM (HEX).json` dari folder `n8n-workflows/`.
* Salin **Production Webhook URL** dari node `INPUT_TRIGGER`.

### 2. Konfigurasi Dashboard Web
* Buka file `public/rfidsystemaudit-ascii.html` dan `rfidsystemaudit-hex.html`.
* Cari bagian `fetch('YOUR_WEBHOOK_URL_HERE', ...)` dan ganti dengan URL Webhook n8n Anda.
* Host folder `public/` menggunakan Nginx, Apache, atau GitHub Pages.

### 3. Persiapan Database
* Gunakan file di folder `samples/Master_Aset.xlsx` sebagai referensi struktur database.
* Pastikan nama kolom sesuai (`Asset_ID` dan `EPC_Refer`).

## 📖 Panduan Operasional
Dokumentasi lengkap mengenai cara penggunaan sistem dapat dilihat di [Dokumen Panduan Operasional (PDF)](./docs/Panduan-Operasional-System-Audit-Terintegrasi-ID.pdf).

## 👨‍💻 Kontributor
* **Alindra Setya Ardana** - *Presales Engineer & Solution Architect*.