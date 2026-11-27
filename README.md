# Mini CRM — Customer Management Web App

Web app CRM (Customer Relationship Management) mobile-first dengan desain modern, pastel, dan ramah pengguna. Data tersimpan langsung di perangkat pengguna (browser `localStorage`) — tidak ada server, tidak ada database eksternal. Cocok untuk diterbitkan via **GitHub Pages**.

## ✨ Fitur

- **Dashboard** — ringkasan statistik (total pelanggan, pendapatan, pelanggan hot, interaksi 30 hari), pelanggan & interaksi terbaru.
- **Pelanggan** — daftar pelanggan dengan pencarian dan filter status (Semua, Tetap, Hot, Baru, Cold). Kartu pelanggan bergaya grid dengan avatar, nama, perusahaan, dan pendapatan.
- **Detail Pelanggan** — profil lengkap, aksi cepat (telepon, email, chat WhatsApp langsung), informasi detail, riwayat interaksi.
- **Interaksi** — riwayat interaksi dengan kartu berwarna (cyan, kuning, khaki, magenta), filter per pelanggan.
- **Tambah/Edit** — form modal untuk pelanggan & interaksi (CRUD lengkap).
- **Panduan** — tutorial 6 langkah penggunaan aplikasi.
- **CTA WhatsApp** — tombol mengambang + kartu CTA di halaman Panduan, langsung terhubung ke nomor **085536362553**.
- **Backup Data** — ekspor & impor data dalam format JSON (penting karena data hanya tersimpan di perangkat).
- **Responsif** — optimal di ponsel (375px), tablet, dan desktop.

## 🎨 Desain

Mengacu pada estetika dashboard CRM Salesforce: latar belakang cream hangat (`#FAFAF5`), aksen pastel (kuning `#F5E625`, cyan `#3BC8F5`, khaki `#D6C96A`, magenta `#E9A8F0`), kartu rounded dengan soft shadow, tipografi Poppins.

## 📁 File

| File | Deskripsi |
|------|-----------|
| `index.html` | Aplikasi CRM lengkap (HTML + CSS + JS dalam satu file, self-contained) |
| `.nojekyll` | Mencegah GitHub Pages memproses file dengan Jekyll |
| `README.md` | Dokumentasi ini |

## 🚀 Cara Publish ke GitHub Pages

### Langkah 1 — Buat Repository GitHub
1. Buka [github.com](https://github.com) dan login.
2. Klik **New repository**.
3. Beri nama repository (contoh: `mini-crm`).
4. Pilih **Public** (gratis untuk GitHub Pages).
5. Centang **Add a README file** (opsional).
6. Klik **Create repository**.

### Langkah 2 — Upload File
1. Di repository Anda, klik **Add file → Upload files**.
2. Drag & drop file `index.html` dan `.nojekyll` ke area upload.
3. Tulis commit message (contoh: `Initial CRM app`).
4. Klik **Commit changes**.

### Langkah 3 — Aktifkan GitHub Pages
1. Buka tab **Settings** di repository.
2. Di menu kiri, klik **Pages**.
3. Pada **Source**, pilih **Deploy from a branch**.
4. Pada **Branch**, pilih `main` (atau `master`) dan folder `/ (root)`.
5. Klik **Save**.
6. Tunggu 1–2 menit. Halaman akan menampilkan URL publik Anda, contoh:
   ```
   https://<username>.github.io/mini-crm/
   ```

### Langkah 4 — Buka Aplikasi
Buka URL tersebut di browser ponsel atau desktop. Aplikasi langsung berjalan dengan data contoh.

## 💾 Catatan Penyimpanan Data

- Semua data tersimpan di **`localStorage` browser** perangkat pengguna.
- Data **TIDAK** sinkron antar perangkat atau antar browser.
- Berganti perangkat/browser? Gunakan **Ekspor JSON** (di halaman Panduan) untuk backup, lalu **Impor JSON** di perangkat baru.
- Membersihkan cache/browser akan menghapus data — selalu buat backup berkala.

## 🔧 Kustomisasi

### Mengubah Nomor WhatsApp
Buka `index.html`, cari baris:
```javascript
const WHATSAPP_NUMBER = '6285536362553';
```
Ganti dengan nomor Anda (format internasional tanpa `+` atau `0` di depan; nomor Indonesia diawali `62`).

### Mengubah Data Contoh
Cari objek `SEED` di dalam `<script>` dan edit array `customers` serta `interactions`. Data contoh hanya dimuat saat pertama kali aplikasi dibuka (ketika `localStorage` masih kosong). Tombol **Hapus Semua Data** di halaman Panduan akan mengosongkan total semua data (pelanggan & interaksi) — data contoh tidak dimuat ulang otomatis setelah itu.

### Mengubah Warna Tema
Edit variabel CSS di bagian `:root` dalam `<style>`:
```css
--cream:#FAFAF5;
--yellow:#F5E625;
--cyan:#3BC8F5;
--khaki:#D6C96A;
--magenta:#E9A8F0;
```

## 🛠 Teknologi

- HTML5, CSS3 (custom properties, flexbox, grid)
- JavaScript murni (vanilla, tanpa framework)
- `localStorage` untuk persistensi data
- Font Poppins dari Google Fonts
- Tidak ada dependensi eksternal selain font — fully self-contained

## 📱 Kompatibilitas

Berjalan di semua browser modern (Chrome, Safari, Firefox, Edge) di ponsel, tablet, dan desktop. Dioptimalkan untuk viewport 375px (iPhone) dan responsif hingga desktop.

---

Dibuat untuk kebutuhan CRM personal/UKM. Butuh bantuan? Hubungi via tombol WhatsApp di dalam aplikasi.
