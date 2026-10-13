# Deal or Drain: Penyelamatan Batik Dewandaru

Game edukasi matematika kelas XI (materi anuitas) dengan konteks usaha Batik Dewandaru, Malang.
Berupa situs statis (HTML, CSS, JavaScript), tanpa server dan tanpa instalasi. Bisa dibuka di Windows, macOS, Android, dan iOS.

## Isi paket
- `index.html`: seluruh permainan
- `assets/img/`: gambar beranda dan dekorasi
- `assets/audio/gamelan.mp3`: backsound
- `favicon.svg`, `assets/img/icon-180.png`: ikon
- `.nojekyll`: agar GitHub Pages menyajikan berkas apa adanya

## Cara memasang di GitHub Pages (tanpa Git, lewat browser)
1. Masuk ke github.com, klik **New repository**. Beri nama, misalnya `deal-or-drain`, pilih **Public**, lalu **Create repository**.
2. Di halaman repository, klik **uploading an existing file**. Ekstrak berkas zip dari paket ini, lalu seret **semua isinya** (`index.html`, folder `assets`, `favicon.svg`, `README.md`, `.nojekyll`) ke kotak unggah. Gunakan komputer, karena unggah folder lewat ponsel belum didukung GitHub. Klik **Commit changes**.
   Pastikan `index.html` berada di tingkat paling atas repository, bukan di dalam folder lain.
3. Buka **Settings > Pages**. Pada **Build and deployment**, pilih **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, lalu **Save**.
4. Tunggu 1 sampai 3 menit. Alamat permainan:
   `https://NAMA-PENGGUNA.github.io/deal-or-drain/`
   Alamat ini tampil juga di bagian atas halaman Settings > Pages. Bagikan link itu ke siswa.

Jika berkas `.nojekyll` tidak ikut terunggah (berkas berawalan titik kadang tersembunyi), permainan tetap berjalan.

## Mengubah isi
- **Link Google Spreadsheet:** buka `index.html`, cari `SHEET_URL` di baris awal bagian konfigurasi, lalu ganti isinya. Atur berbagi spreadsheet ke "Siapa saja yang memiliki link" supaya siswa bisa membukanya.
- **Kunci jawaban pola:** `ANSWER_KEY` pada bagian konfigurasi yang sama.
- **Memperbarui permainan:** di repository, buka berkas yang ingin diganti, pilih **Upload files** (atau ikon pensil untuk mengedit), lalu commit. Perubahan tampil setelah 1 sampai 3 menit. Jika tampilan lama masih muncul, segarkan halaman dengan menahan Shift.

## Catatan penting
- **Penyimpanan jawaban:** jawaban dan kemajuan tiap tim tersimpan di peramban perangkat masing-masing (localStorage). Tidak ada server yang mengumpulkan jawaban, jadi data tidak berpindah antarperangkat. Minta siswa memakai satu perangkat untuk satu tim.
- **Backsound:** peramban melarang suara otomatis sebelum ada interaksi. Musik mulai pada ketukan atau klik pertama (misalnya tombol START).
- **Internet:** huruf (Google Fonts) dimuat dari internet. Tanpa internet, huruf diganti huruf bawaan perangkat dan tampilan tetap berfungsi.
- **Uji di komputer sendiri:** buka terminal di folder ini, jalankan `python3 -m http.server 8000`, lalu buka `http://localhost:8000`. Jika `index.html` dibuka langsung dengan klik ganda, permainan jalan tetapi pengaturan volume backsound bisa tidak berfungsi di iOS.
- **Hak cipta:** pastikan gambar dan musik yang dipakai boleh dipublikasikan secara terbuka, karena repository Public bisa diunduh siapa saja.
