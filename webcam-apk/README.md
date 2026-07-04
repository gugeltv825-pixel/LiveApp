# WebCam Studio (Android APK)

Aplikasi Android yang membungkus `index.html` (WebCam Studio) dalam WebView.
APK di-build otomatis oleh GitHub Actions — Anda tidak perlu menginstal apa pun.

## Cara membuat APK yang bisa di-download

1. **Buat repo baru** di GitHub (boleh private).
2. **Upload semua isi folder ini** ke repo tersebut.
   - Lewat web: buka repo → Add file → Upload files → seret semua file/folder → Commit.
   - Atau lewat git:
     ```bash
     git init
     git add .
     git commit -m "WebCam Studio APK"
     git branch -M main
     git remote add origin https://github.com/USERNAME/NAMA-REPO.git
     git push -u origin main
     ```
3. Buka tab **Actions** di repo. Workflow "Build APK" berjalan otomatis (±3–5 menit).
4. Setelah selesai (centang hijau), APK bisa diunduh dari **dua** tempat:
   - **Releases** (kanan halaman repo) → file `WebCam-Studio.apk` ← link download permanen.
   - **Actions** → run terakhir → bagian **Artifacts** → `WebCam-Studio-APK`.

## Memasang di HP
- Kirim/buka `WebCam-Studio.apk` di HP Android.
- Aktifkan "Instal dari sumber tidak dikenal" bila diminta, lalu Install.
- Saat pertama dibuka, izinkan Kamera & Mikrofon.

## Catatan
- APK ini ditandatangani dengan **debug key** (cukup untuk pemakaian pribadi).
  Untuk publish ke Play Store, perlu signing key rilis sendiri.
- Package: `com.webcam.studio` — Nama: WebCam Studio.
- Untuk build ulang tanpa mengubah kode: Actions → Build APK → **Run workflow**.
