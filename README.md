# Aplikasi Keuangan Pribadi

Aplikasi mobile untuk manajemen keuangan pribadi dengan fitur pengeluaran, tabungan, dan investasi. Dibangun menggunakan Flutter.

## Fitur Utama

### 1. Halaman Login
- Input email dan password dengan validasi
- Tombol login
- Link "Lupa Password"
- Link "Daftar" untuk registrasi pengguna baru
- UI modern dengan gradient hijau (tema keuangan)

### 2. Dashboard Utama
- **Kalender/Agenda**: Menampilkan kalender dengan highlight tanggal yang memiliki transaksi
- **Summary Cards**: Ringkasan total pengeluaran, tabungan, dan investasi
- **Menu Cepat**: Shortcut untuk menambah pengeluaran, tabungan, atau investasi
- **Daftar Transaksi**: Menampilkan transaksi berdasarkan tanggal yang dipilih di kalender
- Informasi singkat tentang transaksi yang akan datang

### 3. Detail Transaksi
- Informasi lengkap tentang transaksi (waktu, lokasi, deskripsi)
- Opsi untuk **Edit** transaksi
- Opsi untuk **Hapus** transaksi dengan konfirmasi
- Toggle untuk **Reminder/Notifikasi** transaksi
- UI yang informatif dengan warna sesuai jenis transaksi

## Tema Keuangan

Aplikasi menggunakan skema warna yang sesuai dengan tema keuangan:
- **Hijau** (#2E7D32): Warna utama, melambangkan keuangan yang sehat
- **Merah** (#D32F2F): Untuk pengeluaran
- **Biru** (#1976D2): Untuk tabungan
- **Orange** (#FF9800): Untuk investasi

## Struktur Proyek

```
lib/
├── main.dart                    # Entry point aplikasi
├── models/
│   └── transaction_model.dart   # Model data transaksi
├── screens/
│   ├── login_page.dart          # Halaman login
│   ├── dashboard_page.dart      # Dashboard utama
│   └── transaction_detail_page.dart  # Detail transaksi
└── theme/
    └── app_theme.dart           # Tema dan styling aplikasi
```

## Cara Menjalankan

### Prasyarat

1. **Install Flutter SDK** (jika belum terinstall):
   - Download dari: https://flutter.dev/docs/get-started/install/windows
   - Extract dan tambahkan ke PATH environment variable
   - Verifikasi instalasi dengan menjalankan:
     ```bash
     flutter doctor
     ```

2. **Setup Emulator/Device**:
   - **Android Emulator**: Install Android Studio dan buat AVD (Android Virtual Device)
   - **Web Browser**: Flutter mendukung web, bisa langsung dijalankan di browser
   - **Physical Device**: Aktifkan USB Debugging untuk Android atau hubungkan iPhone

### Langkah-langkah Menjalankan

1. **Buka Terminal/PowerShell** di folder project:
   ```bash
   cd C:\Users\iSAN\Documents\PWeb
   ```

2. **Install Dependencies**:
   ```bash
   flutter pub get
   ```
   Perintah ini akan mengunduh semua package yang diperlukan (google_fonts, table_calendar, intl, dll)

3. **Cek Device yang Tersedia**:
   ```bash
   flutter devices
   ```
   Akan menampilkan daftar emulator/device yang tersedia

4. **Jalankan Aplikasi**:

   **Opsi 1: Jalankan di Web Browser** (Paling Mudah):
   ```bash
   flutter run -d chrome
   ```
   atau
   ```bash
   flutter run -d edge
   ```

   **Opsi 2: Jalankan di Android Emulator**:
   ```bash
   flutter run
   ```
   (Pastikan emulator sudah berjalan terlebih dahulu)

   **Opsi 3: Jalankan di Device Tertentu**:
   ```bash
   flutter run -d <device-id>
   ```
   (Gunakan device-id dari hasil `flutter devices`)

5. **Hot Reload**: 
   - Tekan `r` di terminal untuk hot reload
   - Tekan `R` untuk hot restart
   - Tekan `q` untuk quit

### Troubleshooting

- **Error "Flutter not found"**: Pastikan Flutter sudah ditambahkan ke PATH
- **Error "No devices found"**: 
  - Untuk web: Jalankan `flutter run -d chrome`
  - Untuk Android: Buka Android Studio > Tools > Device Manager > Start emulator
- **Error dependencies**: Jalankan `flutter clean` lalu `flutter pub get`

## Dependencies

- `google_fonts`: Untuk font Poppins yang modern
- `table_calendar`: Untuk kalender interaktif
- `intl`: Untuk format tanggal dan mata uang Indonesia

## Catatan

- Aplikasi ini adalah UI design, beberapa fitur seperti edit, tambah transaksi, dan backend masih dalam tahap pengembangan
- Data transaksi saat ini menggunakan data contoh (mock data)
- Untuk produksi, perlu integrasi dengan database dan backend API

