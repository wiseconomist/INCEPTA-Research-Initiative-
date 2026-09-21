# INCEPTA — Website Resmi

**Institute for Economic, Climate, and Policy Technology Analysis**
_"Integrating Economics, Intelligence, and Sustainability for Better Policy."_

Website statis (HTML/CSS/JS, satu file, tanpa server) untuk lembaga riset dan konsultasi
kebijakan ekonomi, iklim, dan teknologi cerdas. Siap dipublikasikan lewat **GitHub Pages**.

## Isi repositori

| File          | Fungsi                                                            |
|---------------|------------------------------------------------------------------|
| `index.html`  | Halaman utama (semua konten & gaya ada di sini)                  |
| `404.html`    | Halaman error 404 khusus INCEPTA                                 |
| `.nojekyll`   | Menonaktifkan pemrosesan Jekyll agar file tampil apa adanya      |
| `robots.txt`  | Aturan crawler mesin pencari                                     |
| `README.md`   | Dokumen ini                                                      |

---

## Cara publish ke GitHub Pages

### Opsi A — lewat web GitHub (paling mudah, tanpa aplikasi)

1. Login ke <https://github.com> (buat akun dulu jika belum punya).
2. Klik **New repository**.
   - **Repository name:**
     - Untuk alamat `https://USERNAME.github.io/` → beri nama **`USERNAME.github.io`** (ganti USERNAME dengan username GitHub Anda).
     - Untuk alamat `https://USERNAME.github.io/incepta/` → beri nama bebas, misalnya **`incepta`**.
   - Set **Public**, lalu **Create repository**.
3. Di halaman repo, klik **Add file → Upload files**.
4. Seret semua file di folder ini (`index.html`, `404.html`, `.nojekyll`, `robots.txt`, `README.md`) ke area upload.
   - Catatan: file `.nojekyll` diawali titik. Jika tidak terlihat di file explorer, aktifkan "tampilkan file tersembunyi" saat memilih.
5. Klik **Commit changes**.
6. Buka **Settings → Pages**.
   - **Source:** pilih **Deploy from a branch**.
   - **Branch:** pilih **main** dan folder **/ (root)**, lalu **Save**.
7. Tunggu ±1–2 menit. GitHub akan menampilkan URL situs Anda di bagian atas halaman Pages.

### Opsi B — lewat Git (command line)

```bash
git init
git add .
git commit -m "INCEPTA website"
git branch -M main
git remote add origin https://github.com/USERNAME/USERNAME.github.io.git
git push -u origin main
```

Lalu aktifkan Pages di **Settings → Pages** seperti langkah 6–7 di atas.

---

## Custom domain (opsional): incepta.or.id

1. Daftarkan domain `.or.id` lewat registrar terakreditasi PANDI
   (mis. IDwebhost, Niagahoster, Rumahweb). Domain `.or.id` biasanya
   memerlukan dokumen organisasi (akta/SK).
2. Di **Settings → Pages → Custom domain**, isi `incepta.or.id` lalu **Save**
   (GitHub akan membuat file `CNAME` otomatis).
3. Di panel DNS registrar, tambahkan record:
   - `A` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - atau `CNAME` `www` → `USERNAME.github.io`
4. Aktifkan **Enforce HTTPS** setelah domain terverifikasi.

---

## Yang perlu Anda ganti sebelum go-live

- **Email**: `info@incepta.or.id` (di `index.html`, cari dan ganti).
- **Tautan sosial**: LinkedIn, Medium, ResearchGate masih `#` di bagian footer.
- **Publikasi**: 6 kartu di bagian Publikasi masih contoh — ganti judul, tahun, dan tautan.
- **Form kontak**: saat ini membuka aplikasi email pengguna (mailto). Untuk pengiriman
  otomatis, daftar gratis di <https://formspree.io>, lalu ganti
  `action="https://formspree.io/f/your-form-id"` pada tag `<form>` dengan endpoint Anda.

---

## Fitur

- Desain think-tank profesional, responsif (desktop & mobile).
- Toggle bahasa **Indonesia / Inggris** untuk seluruh konten.
- Bagian lengkap sesuai blueprint: Identitas, Visi–Misi, 3 Klaster Riset,
  Struktur Organisasi, Produk & Layanan, Jejaring, Pendanaan, Roadmap 2025–2029,
  KPI, Publikasi, dan Kontak.
- Tanpa dependensi build — cukup buka `index.html` di browser untuk pratinjau lokal.

© 2025–2026 INCEPTA. Lembaga riset independen.
