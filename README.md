# SiPeka - Sistem Pelaporan Kebersihan

Aplikasi ini merupakan sistem layanan publik berbasis digital yang bertujuan untuk membantu masyarakat dan petugas dalam pengelolaan sampah, khususnya dalam pelaporan titik sampah liar, penjadwalan pengangkutan, dan pelaporan berkala. Sistem ini juga dilengkapi fitur inovatif seperti gamifikasi kebersihan, forum komunitas warga, edukasi kebersihan, .

---

## Fitur Utama

### Fitur Dasar (Final)
1. **Notifikasi Jadwal Pengangkutan Sampah**
   - Mengirim pengingat otomatis sesuai jadwal pengangkutan di wilayah RT/RW pengguna.
2. **Pelaporan Titik Sampah Liar**
   - Pengguna dapat mengunggah foto, lokasi, dan deskripsi titik sampah liar.
3. **Laporan Berkala**
   - Menampilkan statistik bulanan terkait laporan sampah untuk warga dan petugas.

---

## Fitur Inovatif (Pengembangan Tambahan)
1. **Gamifikasi Kebersihan**
   - Warga aktif mendapat poin, level, dan badge sebagai penghargaan.
   - Ada sistem ranking RT bersih.
2. **Jadwal Edukasi & Kegiatan Bersih-Bersih**
   - Kalender gotong royong atau edukasi kebersihan yang bisa dilihat warga.
3. **Fitur Komunitas / Forum Warga**
   - Forum diskusi dan kolaborasi antarwarga.
4. **Integrasi dengan Petugas Lapangan (Admin Panel)**
   - Admin dapat menerima, memverifikasi, dan merespons laporan dengan cepat.
---

## ▶ Cara Menjalankan Aplikasi

1. Pastikan Java Development Kit (JDK) sudah terinstal di sistem.
2. Clone repositori ini:

   
   git clone https://github.com/izzasyathra/SiPeka.git
   
3. Buka project di IDE (misalnya IntelliJ atau NetBeans).
4. Jalankan file utama:

   
   Main.java
   

   File ini merupakan titik masuk aplikasi dan akan membuka antarmuka utama (GUI).

---

## 🗂 Struktur Kode


SiPeka/
├── Main.java                     # Entry point aplikasi
├── README.md
├── .gitignore

├── controller/                   # Logika bisnis & alur program
│   ├── PengendaliAdmin.java
│   ├── PengendaliForum.java
│   ├── PengendaliLaporan.java
│   ├── PengendaliStatistik.java
│   ├── PengendaliJadwal.java
│   ├── PengendaliEdukasi.java
│   ├── PengendaliGamifikasi.java
│   ├── LayananNotifikasi.java
│   ├── PenyimpananData.java
│   └── FormatTanggal.java

├── model/                        # Representasi data/objek
│   ├── Pengguna.java
│   ├── LaporanSampah.java
│   ├── JadwalPengangkutan.java
│   ├── StatistikLaporan.java
│   ├── ForumDiskusi.java
│   ├── Gamifikasi.java
│   ├── AcaraEdukasi.java
│   ├── StatusLaporan.java
│   └── RTRanking.java

├── tampilan/                     # Antarmuka pengguna (GUI)
│   ├── MenuUtama.java
│   ├── PanelAdmin.java
│   ├── ForumWarga.java
│   ├── FormLaporanSampah.java
│   ├── PeringkatRT.java
│   ├── DaftarLaporan.java
│   ├── GamifikasiView.java
│   ├── NotifikasiJadwal.java
│   ├── KalenderEdukasi.java
│   └── StatistikBulanan.java


---

## 💡 Penerapan Pilar OOP

### 1. Encapsulation

Setiap class model seperti Pengguna, LaporanSampah, dan StatistikLaporan membungkus data dalam atribut privat dan menyediakan akses melalui method. Ini menjaga keamanan dan integritas data.

### 2. Inheritance

Struktur class mendukung pewarisan sifat dari class umum seperti Pengguna, yang dapat dikembangkan menjadi class seperti Admin atau Warga untuk peran yang berbeda.

### 3. Polymorphism

Beberapa class GUI seperti MenuUtama, PanelAdmin, dan ForumWarga memiliki method yang sama namun menampilkan hasil atau tampilan yang disesuaikan dengan pengguna masing-masing.

### 4. Abstraction

Fungsi kompleks seperti penyimpanan data (PenyimpananData.java) dan layanan notifikasi (LayananNotifikasi.java) disederhanakan melalui interface method yang mudah digunakan tanpa perlu memahami logika internalnya.
