# 🎵 Les Musik Privat — Presensi Siswa (Google Apps Script)

**Buka aplikasi:** https://jomrcl3-afk.github.io/musiclessonbyjoshua/

Aplikasi web presensi les musik privat berbasis Google Sheets, dengan gaya claymorphism biru muda.

## Fitur
- **Presensi** per periode (4x atau 8x pertemuan), materi dan catatan tiap pertemuan
- **Data siswa**: nama, instrumen, level, orang tua, WhatsApp, jadwal, durasi, biaya, foto, link dokumentasi
- **Penilaian** skala 1–5 dengan laporan yang bisa dicetak / PDF / kirim WhatsApp
- **Invoice** orang tua per periode (terbitkan, tandai lunas, PDF / gambar, kirim WhatsApp)
- **Link orang tua** (hanya baca, khusus satu anak, tanpa sandi)
- Satu sandi untuk pengajar, tanpa admin

## File
| File | Isi |
|---|---|
| `kode/Kode.gs` | Kode server Apps Script |
| `kode/Index.html` | Tampilan aplikasi (di Apps Script beri nama `Index`) |
| `index.html` | Halaman link pendek GitHub Pages, yang membuka aplikasi |

## Cara memasang
1. Buat Google Sheet baru → **Ekstensi → Apps Script**.
2. Ganti isi `Code.gs` dengan isi `Kode.gs`.
3. Tambah file HTML bernama `Index`, isi dengan `Index.html`.
4. Di baris atas `Kode.gs`, ganti `SANDI` dan `NAMA_LES`.
5. Jalankan fungsi `setup` sekali, lalu izinkan akses.
6. **Terapkan → Deployment baru → Aplikasi web** (Jalankan sebagai: Saya · Akses: Siapa saja).

Untuk memperbarui: ganti kodenya, jalankan `setup`, lalu **Kelola deployment → Edit → Versi baru** agar link tetap sama.

> ⚠️ Jangan unggah sandi asli ke GitHub. Biarkan `SANDI = 'GANTI-SANDI-INI'` di repositori, dan isi sandi asli hanya di Apps Script.

## Link pendek (GitHub Pages)
1. Di `index.html`, isi `APP` dengan URL aplikasi web (berakhiran `/exec`).
2. **Settings → Pages → Deploy from a branch → main / (root) → Save**.
3. Link aplikasi: `https://jomrcl3-afk.github.io/musiclessonbyjoshua/`
4. Isi `BASE_URL` di Apps Script dengan link itu supaya link orang tua ikut pendek.

> Aplikasinya tetap berjalan dan menyimpan data di Google Apps Script & Google Sheet. GitHub Pages hanya memberi link pendek.
