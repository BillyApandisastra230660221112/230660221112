# Tugas 1 PAB — Identifikasi Kebutuhan Aplikasi Bergerak

**Nama:** Billy apandisastra 
**NIM:** 230660221112
**Domain:** Perpustakaan Kampus

## 1. Deskripsi Sistem

Sistem Informasi Perpustakaan Kampus merupakan aplikasi mobile yang digunakan oleh mahasiswa dan petugas perpustakaan untuk mendukung proses pencarian dan peminjaman buku. Mahasiswa dapat melihat daftar buku, mencari buku berdasarkan judul atau kategori, melihat detail serta ketersediaan buku, sedangkan petugas bertugas mengelola data buku dan informasi peminjaman melalui sistem backend. Permasalahan yang dihadapi adalah mahasiswa kesulitan mengetahui informasi dan ketersediaan buku secara cepat sehingga masih perlu datang langsung ke perpustakaan atau menghubungi petugas untuk memperoleh informasi tersebut. Aplikasi mobile digunakan karena dapat diakses dalam konteks bergerak sehingga mahasiswa dapat mencari informasi buku kapan saja melalui perangkat yang dibawa, serta menggunakan interaksi sentuh dan sesi penggunaan singkat untuk melakukan pencarian dan melihat informasi buku secara praktis.

## 2. Diagram Arsitektur

Alur komunikasi sistem adalah:

**Aplikasi Mobile → HTTP Request → Backend SI → Database → HTTP Response → Aplikasi Mobile**

File:
- `diagram.png`
- `diagram.mmd`

## 3. Tabel Kebutuhan

| No. | Permintaan | Pengguna | Karakteristik Mobile yang Terkait | Fitur Aplikasi | Materi Pemenuh |
|---:|---|---|---|---|---|
| 1 | Pengguna dapat masuk ke aplikasi dengan akun | Mahasiswa | Sesi penggunaan singkat, interaksi sentuh | Halaman login, input NIM/email dan kata sandi, validasi | UI/UX, form & validasi, REST API |
| 2 | Pengguna dapat melihat daftar buku | Mahasiswa | Konteks bergerak, layar kecil | Halaman daftar buku, kartu buku, navigasi | UI/UX, navigasi, REST API |
| 3 | Pengguna dapat mencari dan memfilter buku | Mahasiswa | Sesi penggunaan singkat, layar kecil | Search bar, filter kategori, hasil pencarian | UI/UX, interaksi input, REST API |
| 4 | Pengguna dapat melihat detail dan ketersediaan buku | Mahasiswa | Konteks bergerak, sesi penggunaan singkat | Halaman detail buku, status tersedia/dipinjam | Navigasi, REST API |
| 5 | Pengguna dapat mengajukan peminjaman buku | Mahasiswa | Interaksi sentuh, konteks bergerak | Tombol pinjam, form/konfirmasi peminjaman, validasi | Form & validasi, REST API |
| 6 | Pengguna dapat melihat riwayat peminjaman | Mahasiswa | Sesi penggunaan singkat, layar kecil | Halaman riwayat, status peminjaman | Navigasi, data lokal/cache bila diperlukan, REST API |
| 7 | Data buku, pengguna, dan peminjaman dikelola oleh petugas | Petugas | Tidak menjadi fungsi utama aplikasi mobile mahasiswa | Pengelolaan database, CRUD, aturan peminjaman | **Di luar lingkup aplikasi mobile (backend SI)** |

**Catatan:** Panduan tugas meminta minimal 6 kebutuhan dan juga meminta setidaknya satu kebutuhan yang dinyatakan di luar lingkup aplikasi mobile, yaitu kebutuhan backend SI.

### Catatan tentang kolom "Materi Pemenuh"

File panduan yang tersedia tidak menyertakan isi `TIMELINE.md` atau pembagian minggu secara rinci. Karena itu, nomor minggu tidak dibuat-buat. Kolom di atas menggunakan materi PAB yang relevan; setelah `TIMELINE.md` dari kelas tersedia, bagian ini perlu disesuaikan dengan nomor minggu yang sebenarnya.

## 4. Bukti Environment Siap

Simpan tiga screenshot berikut:

1. `flutter-doctor/sebelum.png` — hasil `flutter doctor -v` sebelum perbaikan dan masih memiliki tanda `✗`.
2. `flutter-doctor/sesudah.png` — hasil `flutter doctor -v` setelah perbaikan.
3. `aplikasi.png` — aplikasi counter Flutter berjalan pada web, emulator, atau perangkat fisik.

### Cara mengambil bukti

Jalankan:

```bash
flutter doctor -v
```

Simpan screenshot hasil pertama sebagai `flutter-doctor/sebelum.png`.

Setelah environment diperbaiki, jalankan kembali:

```bash
flutter doctor -v
```

Simpan screenshot hasil kedua sebagai `flutter-doctor/sesudah.png`.

Untuk bukti aplikasi, jalankan project Flutter pada target yang tersedia, kemudian screenshot aplikasi counter yang sedang berjalan dan simpan sebagai:

```text
aplikasi.png
```

## 5. Refleksi

Fitur perangkat yang paling relevan untuk aplikasi perpustakaan adalah kamera karena dapat digunakan untuk memindai barcode atau kode buku sehingga proses identifikasi buku dapat dilakukan dengan lebih cepat. Penggunaan kamera sesuai dengan konteks aplikasi bergerak karena pengguna dapat menggunakan perangkat yang dibawanya untuk melakukan pemindaian tanpa harus mengetik kode buku secara manual. Fitur tersebut dapat dikembangkan pada tahap implementasi fitur perangkat setelah fungsi dasar aplikasi, navigasi, data, dan REST API tersedia.

## 6. Struktur Folder Pengumpulan

```text
tugas-1/<nim>-<nama>/
├── README.md
├── diagram.png
├── diagram.mmd
├── flutter-doctor/
│   ├── sebelum.png
│   └── sesudah.png
└── aplikasi.png
```

## 7. Checklist Sebelum Pengumpulan

- [ ] Nama dan NIM sudah diisi.
- [ ] Deskripsi sistem menyebutkan minimal 2 karakteristik mobile.
- [ ] Diagram menunjukkan HTTP Request dan HTTP Response.
- [ ] Diagram PNG dan file sumber `.mmd` tersedia.
- [ ] Tabel memiliki minimal 6 kebutuhan.
- [ ] Semua kolom tabel terisi.
- [ ] Ada kebutuhan yang dinyatakan di luar lingkup aplikasi mobile/backend.
- [ ] `flutter-doctor/sebelum.png` tersedia.
- [ ] `flutter-doctor/sesudah.png` tersedia.
- [ ] `aplikasi.png` tersedia.
- [ ] Refleksi terdiri tepat 3 kalimat.
- [ ] Jika TIMELINE.md kelas tersedia, kolom materi pemenuh sudah disesuaikan dengan minggu yang benar.
