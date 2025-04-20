
# 🚗 Prompt Deep Research: Road Trip Bogor ke Jawa Tengah (3–5 Hari, 4 Orang Dewasa, Budget Rp 5–10 Juta)

Saya ingin merencanakan **perjalanan wisata darat selama 3–5 hari** dari **Bogor ke berbagai kota di Jawa Tengah**, menggunakan **mobil pribadi** melalui **jalan tol Trans Jawa**, bersama **4 orang dewasa**, dengan **total budget antara Rp 5 juta hingga Rp 10 juta**.

---

## 🔧 Teknologi Pendukung untuk Riset (MCP Server)

Dalam proses riset ini, **AI diperbolehkan menggunakan MCP server atau plugin tertentu** untuk mengakses **informasi real-time**. Gunakan:

- **`zcaceres/fetch-mcp`** untuk:
  - Melakukan **crawling/scraping harga penginapan** dari situs **Traveloka**, **Agoda**, dan **Tiket.com**
  - Mengambil **link pemesanan langsung** untuk tiap penginapan yang direkomendasikan

- **Google Maps MCP** untuk:
  - Melihat **review penginapan dan tempat kuliner**
  - Mengambil **foto lokasi** (penginapan, tempat makan, wisata)
  - Menghasilkan **pin lokasi Google Maps** untuk semua destinasi dan tempat penting
  - Menyusun **rute perjalanan dengan pin** yang bisa ditampilkan di output HTML

> 💡 **Gunakan placeholder berikut untuk tanggal perjalanan agar mudah diganti saat riset:**
> - `{{tanggal_berangkat}}`: Tanggal mulai perjalanan dari Bogor
> - `{{tanggal_pulang}}`: Tanggal pulang dari Jawa Tengah ke Bogor
> - `{{tanggal_check_in}}`: Tanggal check in di masing-masing penginapan yang direkomendasikan
> - `{{tanggal_check_out}}`: Tanggal check out dari masing-masing penginapan yang direkomendasikan

---

## 1. Rute Perjalanan
- Jalur Tol Trans Jawa dari Bogor ke Jawa Tengah
- Titik masuk dan keluar tol untuk kota-kota seperti Semarang, Solo, Magelang, dll.
- Alternatif rute jika ingin mengunjungi lebih dari 1 kota
- **Tampilkan rute interaktif dalam output static HTML dengan pin lokasi (Google Maps Embed/iframe)**

## 2. Estimasi Jarak & Waktu Tempuh
- Total jarak dan waktu tempuh
- Rekomendasi pembagian waktu berkendara per hari
- Kota transit strategis untuk istirahat/menginap

## 3. Rest Area Rekomendasi
- Lokasi rest area terbaik sepanjang tol
- Fasilitas unggulan (SPBU, toilet, kuliner, musala)
- Review singkat dan foto (jika tersedia)
- **Tampilkan pin lokasi rest area di HTML output**

## 4. Penginapan
- Rekomendasi hotel/guesthouse/homestay untuk 4 orang dewasa
- Kategori:
  - Budget (200–400 ribu)
  - Menengah (400–700 ribu)
- Lokasi strategis dekat pusat kota/wisata
- Fasilitas utama: parkir mobil, AC, Wi-Fi
- Tampilkan:
  - **Nama penginapan**
  - **Harga per malam berdasarkan tanggal `{{tanggal_check_in}}` – `{{tanggal_check_out}}`**
  - **Foto**
  - **Rating & review**
  - **Link untuk memesan di Traveloka/Agoda/Tiket.com**
  - **Google Maps pin lokasi**
- **Disarankan tampil dalam bentuk tabel dan galeri HTML interaktif**

## 5. Kuliner
- Tempat makan/kuliner khas di tiap kota tujuan
- Estimasi harga per porsi
- Foto menu andalan
- **Rating Google Maps**
- **Link lokasi (Google Maps pin)**

## 6. Estimasi Biaya Perjalanan
- Perkiraan biaya tol PP
- Konsumsi bensin (mobil pribadi, jarak total)
- Biaya makan 3x sehari/orang
- Akomodasi (3–5 malam)
- Opsional: tiket wisata, parkir, jajan
- Simulasi total untuk budget Rp 5 juta dan Rp 10 juta
- **Data biaya dalam bentuk tabel dan file CSV**

## 7. Tips Berkendara Jarak Jauh
- Persiapan kendaraan (servis, ban, oli, dll.)
- Rotasi sopir (jika ada)
- Waktu terbaik untuk berangkat dan kembali
- Tips menghindari kelelahan dan macet

## 8. Navigasi & Info Real-Time
- Aplikasi bantu perjalanan: Google Maps, Waze, Travoy, dll.
- Cara cek info tol, cuaca, dan rest area secara langsung

---

## Format Output:

1. **Folder Laporan Hasil Riset**:
   - Semua hasil riset dikumpulkan dalam satu folder yang terstruktur rapi, terdiri dari beberapa file dengan format sebagai berikut:

     - **Static HTML**:
       - Menyajikan semua informasi dalam bentuk panduan interaktif
       - Galeri penginapan & kuliner
       - Rute perjalanan dengan **Google Maps Embed**
       - Pin lokasi semua titik penting (penginapan, kuliner, rest area)

     - **CSV**:
       - Tabel penginapan lengkap dengan harga, link booking, dan lokasi
       - Daftar kuliner + estimasi harga dan lokasi
       - Estimasi biaya

     - **PDF**:
       - Panduan cetak untuk dibawa selama perjalanan

2. **Nama Folder**: Semua file riset dikumpulkan dalam satu folder dengan nama yang sesuai, misalnya `riset_road_trip_bogor_jateng_{{tanggal_berangkat}}–{{tanggal_pulang}}`