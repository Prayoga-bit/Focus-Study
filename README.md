# Focus Study Extension 🎯📚

Ekstensi Chrome yang membantu meningkatkan produktivitas belajar dengan fitur pemblokiran website, Pomodoro timer berbasis AI, dan tracking statistik belajar.

## 📋 Daftar Isi

- [Fitur Utama](#-fitur-utama)
- [Instalasi](#-instalasi)
- [Cara Penggunaan](#-cara-penggunaan)
- [Teknologi](#-teknologi)
- [Screenshot](#-screenshot)
- [Kontribusi](#-kontribusi)
- [Lisensi](#-lisensi)

## ✨ Fitur Utama

### 1. 🚫 Block Website

Fitur untuk memblokir akses ke website-website yang mengganggu selama waktu belajar.

**Cara Kerja:**
- Simpan domain website yang ingin diblokir
- Website akan otomatis terblokir saat **Study Time** aktif
- Website dapat diakses kembali saat **Rest Time**
- Pemblokiran otomatis aktif kembali saat Study Time berikutnya dimulai

**Contoh Website yang Dapat Diblokir:**
- Media sosial (Facebook, Instagram, Twitter)
- Platform hiburan (YouTube, Netflix, TikTok)
- Game online
- Website lainnya yang mengganggu fokus belajar

### 2. ⏱️ Pomodoro Timer dengan ML Model

Timer Pomodoro yang dilengkapi dengan teknologi Machine Learning untuk memantau aktivitas belajar Anda.

**Fitur Timer:**
- Set durasi **Study Time** dan **Rest Time** sesuai kebutuhan
- Alarm otomatis berbunyi saat memasuki waktu Study dan Rest
- Notifikasi desktop untuk mengingatkan pergantian sesi

**Fitur AI/ML (Opsional):**

📱 **Block Phone Detection**
- Centang fitur "Block Phone" untuk mengaktifkan deteksi
- Model ML akan otomatis dimuat dan menggunakan kamera
- Saat **ponsel terdeteksi** di kamera → Study time **bertambah 1 menit** (penalti)
- Membantu Anda tetap fokus dan menghindari distraksi dari ponsel

👤 **Presence Detection**
- Model ML mendeteksi kehadiran Anda di depan kamera
- Saat **Anda tidak terdeteksi** → Study time **otomatis pause**
- Saat **Anda muncul kembali** → Study time **otomatis berlanjut**
- Memastikan waktu belajar yang tercatat adalah waktu efektif

### 3. 📊 Study Stats

Pantau progress dan statistik belajar Anda secara real-time.

**Informasi yang Ditampilkan:**
- Total waktu belajar harian
- Total waktu belajar mingguan
- Total waktu belajar bulanan
- Grafik progress belajar
- 🔥 **Streak Icon** - Menampilkan berapa hari berturut-turut Anda konsisten belajar

### 4. 💬 Feedback System

Berikan masukan dan saran untuk pengembangan aplikasi.

**Cara Kerja:**
- Form feedback terintegrasi dalam extension
- Data feedback tersimpan di **Firebase Database**
- Membantu developer meningkatkan kualitas aplikasi

## 📥 Instalasi

### Metode 1: Install dari Chrome Web Store
1. Kunjungi [Focus Study Extension di Chrome Web Store](#) *(link akan ditambahkan)*
2. Klik tombol **"Add to Chrome"**
3. Konfirmasi instalasi dengan klik **"Add Extension"**

### Metode 2: Install Manual (Development Mode)

1. **Clone repository ini:**
```bash
git clone https://github.com/Prayoga-bit/Focus-Study.git
cd Focus-Study
```

2. **Buka Chrome dan akses Extension Management:**
   - Ketik `chrome://extensions/` di address bar
   - Atau klik menu ⋮ → More Tools → Extensions

3. **Aktifkan Developer Mode:**
   - Toggle switch "Developer mode" di pojok kanan atas

4. **Load Extension:**
   - Klik tombol **"Load unpacked"**
   - Pilih folder `Focus Study/chrome-mv3` dari repository yang telah di-clone
   - Extension akan muncul di daftar extension Anda

5. **Pin Extension (Opsional):**
   - Klik icon puzzle 🧩 di toolbar Chrome
   - Klik pin 📌 di samping Focus Study Extension

## 🚀 Cara Penggunaan

### Setup Awal

1. **Klik icon Focus Study Extension** di toolbar Chrome
2. Anda akan melihat popup dengan beberapa tab/menu

### Menggunakan Block Website

1. Buka tab **"Block Website"**
2. Masukkan domain website yang ingin diblokir (contoh: `facebook.com`, `youtube.com`)
3. Klik tombol **"Add"** atau **"Save"**
4. Website akan terblokir otomatis saat Study Time aktif
5. Untuk menghapus, klik tombol **"Delete"** atau **"Remove"** di samping domain

### Menggunakan Pomodoro Timer

**Basic Setup:**
1. Buka tab **"Timer"** atau **"Pomodoro"**
2. Set durasi Study Time (contoh: 25 menit)
3. Set durasi Rest Time (contoh: 5 menit)
4. Klik tombol **"Start"** untuk memulai sesi belajar

**Mengaktifkan ML Features:**
1. Centang opsi **"Block Phone"** untuk deteksi ponsel
2. Centang opsi **"Presence Detection"** untuk deteksi kehadiran
3. Extension akan meminta izin akses kamera
4. Klik **"Allow"** untuk memberikan izin
5. Model ML akan dimuat secara otomatis
6. Mulai sesi belajar Anda!

**Tips:**
- Pastikan pencahayaan ruangan cukup untuk deteksi optimal
- Posisikan kamera menghadap area belajar Anda
- Jauhkan ponsel dari jangkauan kamera agar tidak terdeteksi

### Melihat Study Stats

1. Buka tab **"Stats"** atau **"Statistics"**
2. Lihat total waktu belajar Anda
3. Perhatikan **Streak Icon** 🔥 untuk melihat konsistensi belajar
4. Gunakan statistik untuk memotivasi diri meningkatkan produktivitas

### Memberikan Feedback

1. Buka tab **"Feedback"**
2. Tulis masukan, saran, atau laporan bug
3. Klik tombol **"Submit"** atau **"Send"**
4. Feedback Anda akan tersimpan dan membantu pengembangan aplikasi

## 🛠️ Teknologi

Extension ini dibangun menggunakan:

- **Manifest V3** - Chrome Extension API terbaru
- **JavaScript** - Logika aplikasi
- **HTML/CSS** - User Interface
- **TensorFlow.js / ML5.js** - Machine Learning untuk deteksi objek dan presence
- **Firebase** - Backend untuk menyimpan feedback dan statistik
- **Chrome APIs**:
  - `chrome.storage` - Menyimpan data lokal
  - `chrome.alarms` - Timer dan notifikasi
  - `chrome.notifications` - Notifikasi desktop
  - `chrome.webRequest` - Blocking website
  - `getUserMedia()` - Akses kamera untuk ML

## 📸 Screenshot

*Screenshot akan ditambahkan di sini*

## 🤝 Kontribusi

Kontribusi selalu diterima! Jika Anda ingin berkontribusi:

1. Fork repository ini
2. Buat branch baru (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan Anda (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

## 📝 Lisensi

Distributed under the MIT License. See `LICENSE` file for more information.

## 📧 Kontak

Prayoga - [@Prayoga-bit](https://github.com/Prayoga-bit)

Project Link: [https://github.com/Prayoga-bit/Focus-Study](https://github.com/Prayoga-bit/Focus-Study)

---

**⭐ Jika extension ini membantu produktivitas belajar Anda, jangan lupa berikan bintang di GitHub!**

## 🙏 Acknowledgments

- Inspirasi dari Teknik Pomodoro oleh Francesco Cirillo
- TensorFlow.js team untuk ML framework
- Chrome Extension documentation
- Semua kontributor yang telah membantu project ini

---

**Made with ❤️ for better study productivity**
