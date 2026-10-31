# 🌱 SPARTA - Sistem Prediksi Agroklimat & Rekomendasi Tanam

![Version](https://img.shields.io/badge/Version-V.0.1.2026-0d9488?style=flat-square)
![Author](https://img.shields.io/badge/Author-N2-0f766e?style=flat-square)
![Region](https://img.shields.io/badge/Region-Wonogiri_Regency-047857?style=flat-square)

**SPARTA (Sistem Prediksi Agroklimat & Rekomendasi Tanam)** adalah aplikasi web dasbor interaktif yang dirancang untuk memantau prediksi cuaca agroklimat dan memberikan rekomendasi komoditas tanam beserta peringatan risiko di wilayah **Kabupaten Wonogiri** secara *real-time*.

---

## ✨ Fitur Utama

* **📊 Visualisasi Grafik Curah Hujan Interaktif (*Rainfall Chart*)**
  Menampilkan perbandingan prediksi curah hujan di seluruh kecamatan menggunakan grafik batang dengan kode warna otomatis berdasarkan tingkat risiko:
  * 🟢 **Aman** (Hijau)
  * 🟡 **Waspada** (Kuning/Oranye)
  * 🔴 **Bahaya** (Merah)
* **📍 Pemilihan Kecamatan Ganda (*Dual-Selection*)**
  Pengguna dapat memilih data kecamatan melalui menu *dropdown* atau dengan mengklik langsung batang grafik pada *chart*.
* **📇 Kartu Informasi Agroklimat Lengkap**
  Menyajikan metrik penting untuk pertanian di setiap kecamatan:
  * Prediksi Curah Hujan (`mm/hari`)
  * Suhu Udara (`derajat Celcius`)
  * Kelembaban Udara (`persen`)
  * Durasi Sinar Matahari (`jam`)
  * Rekomendasi Tanam spesifik
  * Indikator Status Risiko
* **⏱️ Indikator Waktu *Update Real-Time***
  Dilengkapi penunjuk waktu langsung (*live clock* zona waktu WIB) yang diperbarui setiap detik serta informasi waktu sinkronisasi terakhir dari *database* Google Sheets.
* **📱 Desain Responsif & Modern**
  Mendukung tampilan *split-screen* pada layar desktop/laptop serta fitur geser horizontal (*swipe*) pada perangkat *mobile*.

---

## 🛠️ Teknologi yang Digunakan

Proyek ini dibangun dengan arsitektur *Single-File HTML* yang ringan dan cepat menggunakan:

* **HTML5 & CSS3**: *Custom Variables*, *Flexbox*, *CSS Grid*, dan *Responsive Media Queries*.
* **JavaScript (ES6+)**: Logika pemrosesan data, manipulasi DOM, dan penunjuk waktu *real-time*.
* **[Chart.js](https://www.chartjs.org/)**: *Library* untuk merender grafik batang interaktif.
* **[PapaParse](https://www.papaparse.com/)**: *Parser* CSV cepat untuk mengambil dan mengonversi data langsung dari Google Sheets.

---

## 📋 Struktur Data (Google Sheets)

Aplikasi ini mengambil data secara dinamis dari Google Sheets menggunakan *endpoint* CSV (`gviz/tq?tqx=out:csv`):

| Nama Kolom | Deskripsi | Contoh Nilai |
| :--- | :--- | :--- |
| `Kecamatan` | Nama kecamatan di Kabupaten Wonogiri | `Wonogiri` |
| `Prediksi Curah Hujan` | Angka prediksi curah hujan harian | `12.5` |
| `Suhu` | Rata-rata suhu udara harian | `27` |
| `Kelembaban` | Persentase kelembaban udara | `80` |
| `Sinar Matahari` | Estimasi durasi penyinaran matahari | `6.5` |
| `Rekomendasi Tanam` | Jenis tanaman yang disarankan | `Padi, Jagung` |
| `Peringatan Risiko` | Status tingkat risiko (`Aman` / `Waspada` / `Bahaya`) | `Aman` |
| `Waktu Update` | Catatan waktu pembaruan data pada *sheet* | `31 Okt 2026` |

---

## 📌 Informasi Versi & Lisensi

* **Versi**: `V.0.1.2026`
* **Pengembang**: **N2** (`by N2 | V.0.1.2026`)
* **Wilayah**: Kabupaten Wonogiri, Jawa Tengah
