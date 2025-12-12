# 🌍 SIG Kebencanaan - Sistem Informasi Geografis Bencana Real-Time

[![Status](https://img.shields.io/badge/Status-Active-success)](https://github.com)
[![API](https://img.shields.io/badge/API-BMKG-blue)](https://data.bmkg.go.id)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

Sistem Informasi Geografis (SIG) untuk pemantauan bencana alam terkini di Indonesia dengan data real-time dari **BMKG (Badan Meteorologi, Klimatologi, dan Geofisika)**.

## 📋 Deskripsi

Aplikasi web interaktif yang menampilkan informasi gempa bumi terkini di Indonesia secara real-time. Data diambil langsung dari API resmi BMKG tanpa memerlukan backend server. Aplikasi ini dilengkapi dengan peta interaktif, filter bencana, detail informasi, dan fitur berbagi ke media sosial.

## ✨ Fitur Utama

### 🔴 Data Real-Time
- ✅ Integrasi langsung dengan API BMKG
- ✅ Auto-refresh setiap 5 menit
- ✅ Refresh manual dengan satu klik
- ✅ Fallback data jika API offline
- ✅ Notifikasi status loading & update

### 🗺️ Peta Interaktif
- ✅ Peta Indonesia berbasis Leaflet.js
- ✅ Custom marker untuk setiap gempa
- ✅ Marker berwarna berdasarkan magnitude
- ✅ Popup detail saat marker diklik
- ✅ Zoom in/out controls
- ✅ Fullscreen mode
- ✅ Geolocation (temukan lokasi Anda)

### 📊 Statistik & Visualisasi
- ✅ Total bencana dilaporkan
- ✅ Jumlah bencana aktif
- ✅ Estimasi orang terdampak
- ✅ Waktu update terakhir
- ✅ Animasi counter untuk statistik

### 🎯 Filter & Pencarian
- ✅ Filter berdasarkan jenis bencana
- ✅ Filter gempa viral/trending
- ✅ Sorting berdasarkan magnitude
- ✅ List view dengan detail lengkap

### 📱 Responsive Design
- ✅ Desktop (1200px+)
- ✅ Tablet (768px - 1199px)
- ✅ Mobile (480px - 767px)
- ✅ Small Mobile (<480px)
- ✅ Touch-friendly interface

### 🎨 UI/UX Modern
- ✅ Glass morphism effect
- ✅ Smooth animations
- ✅ Gradient backgrounds
- ✅ Hover effects
- ✅ Loading states
- ✅ Toast notifications

### 🔗 Social Sharing
- ✅ WhatsApp
- ✅ Instagram
- ✅ TikTok
- ✅ LinkedIn
- ✅ Facebook
- ✅ Twitter

## 🚀 Teknologi yang Digunakan

### Frontend
- **HTML5** - Struktur aplikasi
- **CSS3** - Styling dengan variabel & animasi modern
- **JavaScript (Vanilla)** - Logic & API integration
- **Leaflet.js** - Library peta interaktif
- **Font Awesome** - Icon library
- **Google Fonts (Poppins)** - Typography

### API & Data Source
- **BMKG API** - Data gempa real-time
  - Endpoint: `https://data.bmkg.go.id/DataMKG/TEWS/gempaterkini.json`
  - Endpoint: `https://data.bmkg.go.id/DataMKG/TEWS/autogempa.json`

## 📦 Instalasi & Penggunaan

### Prasyarat
Tidak ada prasyarat khusus! Aplikasi ini adalah **static web app** yang bisa langsung dibuka di browser.

### Cara Menjalankan

1. **Clone repository**
   ```bash
   git clone https://github.com/yourusername/natural-disasters.git
   cd natural-disasters
   ```

2. **Buka file HTML**
   - Double-click file `index.html`, atau
   - Gunakan Live Server di VS Code, atau
   - Buka melalui browser: `file:///path/to/index.html`

3. **Deploy (Optional)**
   
   Deploy ke platform hosting gratis:
   
   **GitHub Pages:**
   ```bash
   # Push ke GitHub
   git add .
   git commit -m "Initial commit"
   git push origin main
   
   # Enable GitHub Pages di Settings > Pages > Source: main branch
   ```
   
   **Netlify:**
   - Drag & drop folder ke netlify.com/drop
   - Atau connect dengan GitHub repository
   
   **Vercel:**
   ```bash
   npm i -g vercel
   vercel
   ```

## 📂 Struktur Project

```
natural-disasters/
│
├── index.html          # Main HTML file (All-in-one)
├── README.md          # Dokumentasi project
└── .gitignore         # Git ignore file (optional)
```

**Note:** Semua CSS dan JavaScript sudah embedded dalam `index.html` untuk kemudahan deployment.

## 🎯 Cara Menggunakan Aplikasi

### 1. Melihat Data Gempa
- Buka aplikasi di browser
- Data gempa akan otomatis dimuat dari BMKG
- Lihat marker di peta untuk lokasi gempa

### 2. Filter Bencana
- Klik tombol filter di atas peta (Semua, Gempa Bumi, dll)
- List di sidebar akan difilter sesuai pilihan

### 3. Detail Gempa
- Klik marker di peta untuk popup ringkas
- Klik "Detail Lengkap" untuk modal detail
- Atau klik item di sidebar untuk fokus ke lokasi

### 4. Refresh Data
- Klik tombol "Perbarui Data" di header
- Atau tunggu auto-refresh setiap 5 menit

### 5. Kontrol Peta
- **Zoom In/Out:** Tombol + / - di kanan atas peta
- **Lokasi Saya:** Tombol GPS untuk geolocation
- **Fullscreen:** Tombol expand untuk mode layar penuh

### 6. Berbagi Informasi
- Scroll ke bagian "Bagikan Informasi"
- Klik icon social media untuk share

## 📊 Data yang Ditampilkan

Setiap gempa menampilkan informasi:
- **Magnitude** (Skala Richter)
- **Lokasi/Wilayah** kejadian
- **Koordinat** (Latitude, Longitude)
- **Kedalaman** gempa
- **Waktu** kejadian (tanggal & jam)
- **Potensi** tsunami
- **Status** (Aktif/Berlangsung/Selesai)
- **Severity** (Tingkat keparahan)
- **Estimasi** orang terdampak

## 🔧 Konfigurasi & Customization

### Mengubah Interval Auto-Refresh
Edit di `index.html` bagian JavaScript:
```javascript
// Default: 5 menit
setInterval(() => {
    fetchBMKGData();
}, 5 * 60 * 1000); // Ubah angka 5 sesuai kebutuhan
```

### Mengubah Warna Tema
Edit di CSS variables:
```css
:root {
    --primary: #6366f1;      /* Warna utama */
    --secondary: #8b5cf6;    /* Warna sekunder */
    --danger: #ef4444;       /* Warna bahaya */
    /* dst... */
}
```

### Menambah Sumber Data Lain
Tambahkan API endpoint di bagian JavaScript:
```javascript
const YOUR_API_URL = 'https://your-api-endpoint.com/data.json';
// Implementasikan fetch function
```

## 🐛 Troubleshooting

### Data Tidak Muncul
- ✅ Pastikan koneksi internet aktif
- ✅ Check console browser (F12) untuk error
- ✅ BMKG API mungkin sedang maintenance
- ✅ CORS issue: gunakan browser extension atau proxy

### Peta Tidak Muncul
- ✅ Check koneksi CDN Leaflet.js
- ✅ Clear browser cache
- ✅ Coba browser lain

### Geolocation Tidak Bekerja
- ✅ Izinkan akses lokasi di browser
- ✅ Gunakan HTTPS (untuk production)
- ✅ Beberapa browser memblok geolocation di `file://`

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan:

1. Fork repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## 📝 To-Do List

- [ ] Tambah data bencana lain (banjir, longsor, kebakaran)
- [ ] Integrasi API cuaca BMKG
- [ ] Notifikasi push untuk gempa besar
- [ ] Historical data & chart
- [ ] Export data ke CSV/PDF
- [ ] Multi-language support (EN/ID)
- [ ] Dark mode toggle
- [ ] PWA (Progressive Web App)
- [ ] Offline mode dengan Service Worker

## 📄 License

Project ini menggunakan **MIT License** - lihat file [LICENSE](LICENSE) untuk detail.

## 👨‍💻 Developer

Dikembangkan dengan ❤️ untuk tugas **Sistem Informasi Geografis**  
**Universitas:** [Nama Universitas]  
**Semester:** 5  
**Tahun:** 2025

## 🙏 Credits & Acknowledgments

- **BMKG** - Data gempa real-time
- **Leaflet.js** - Interactive maps
- **Font Awesome** - Icons
- **Google Fonts** - Typography
- **OpenStreetMap** - Map tiles
- **CARTO** - Basemap tiles

## 📞 Kontak

Untuk pertanyaan, saran, atau bug report:
- **Email:** your.email@example.com
- **GitHub Issues:** [Create Issue](https://github.com/yourusername/natural-disasters/issues)

## 🌟 Support

Jika project ini bermanfaat, berikan ⭐ di GitHub!

---

**⚠️ Disclaimer:** Aplikasi ini dibuat untuk tujuan edukasi. Data bersumber dari BMKG dan ditampilkan apa adanya. Untuk informasi resmi dan keputusan penting, selalu rujuk ke website resmi BMKG di [bmkg.go.id](https://www.bmkg.go.id)

**Last Updated:** December 12, 2025