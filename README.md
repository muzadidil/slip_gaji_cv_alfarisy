# Slip Gaji Karyawan

Web app pembuat slip gaji bulanan. GitHub Pages + Firebase Realtime Database + PDF (jsPDF).

## Setup (3 langkah)

1. **Isi config Firebase** — buka `index.html`, cari `firebaseConfig`, ganti dengan config project Firebase-mu (boleh pakai project yang sama dengan app tahu — data slip gaji tersimpan terpisah di node `slipgaji/`).

2. **Buat repo baru** di GitHub (misal `slipgaji`), push `index.html`, aktifkan GitHub Pages (Settings → Pages → branch main).

3. **Isi Pengaturan** — buka appnya, tab **Pengaturan**, isi nama perusahaan, alamat, kota, dan penandatangan. Lalu tab **Karyawan**, tambahkan karyawan.

## Cara pakai

Tab **Buat Slip** → pilih karyawan (gaji pokok terisi otomatis) → tambah tunjangan/potongan sesuai kebutuhan → preview langsung terlihat di kanan → klik **Simpan & Unduh PDF**. Slip tersimpan di tab **Riwayat** dan bisa diunduh ulang kapan saja.

Nomor slip otomatis: `SG/2026/VII/001` (urut per periode).

## ⚠️ Keamanan data gaji

Data gaji itu sensitif. Kalau Firebase rules-mu masih terbuka (`.read: true`), siapa pun yang tahu URL database bisa lihat gaji semua karyawan. Minimal: jangan sebarkan link appnya. Lebih aman: nanti tambahkan Firebase Auth (bisa saya bantu kalau sudah dibutuhkan).
