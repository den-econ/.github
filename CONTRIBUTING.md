# Berkontribusi ke DEN Economic Lab

Terima kasih sudah tertarik dengan pekerjaan kami! DEN Economic Lab fokus pada analisis ekonomi yang terbuka dan bisa direproduksi siapa saja demi kepentingan publik Indonesia. Panduan ini menjelaskan bagaimana kalian — baik dari dalam maupun luar lab — bisa ikut berkontribusi di repositori kami.

---

## Daftar Isi

- [Siapa yang Bisa Kontribusi](#siapa-yang-bisa-kontribusi)
- [Cara Berkontribusi](#cara-berkontribusi)
- [Melaporkan Kesalahan](#melaporkan-kesalahan)
- [Kasih Saran Perbaikan](#kasih-saran-perbaikan)
- [Submit Koreksi Kode atau Data](#submit-koreksi-kode-atau-data)
- [Masalah Replikasi](#masalah-replikasi)
- [Gaya & Standar](#gaya--standar)
- [Proses Pull Request](#proses-pull-request)
- [Kode Etik](#kode-etik)
- [Kontak](#kontak)

---

## Siapa yang Bisa Kontribusi

**Peneliti eksternal, mahasiswa, dan siapa aja** boleh:
- Lapor kesalahan dalam analisis kami (data, kode, atau metodologi)
- Tanya-tanya soal metode kami lewat GitHub Discussions
- Kasih saran perbaikan atau ide pengembangan
- Submit koreksi lewat Pull Request

**Anggota Lab** ikut alur kerja internal yang ada di repositori [`.github-private`](https://github.com/den-econ/.github-private) kami.

---

## Cara Berkontribusi

### 1. Tanya-tanya
Pakai [GitHub Discussions](https://github.com/orgs/den-econ/discussions) untuk:
- Nanya soal metodologi
- Minta klarifikasi tentang sumber data
- Diskusi umum tentang riset kami

Tolong cek dulu diskusi yang udah ada sebelum bikin yang baru ya.

### 2. Lapor Kesalahan
Pakai **GitHub Issues** (lihat [Melaporkan Kesalahan](#melaporkan-kesalahan) di bawah) untuk:
- Bug dalam kode (output salah, error pas dijalanin)
- Kesalahan data (nilai salah, ada data yang hilang)
- Masalah metodologi (kayaknya ada yang salah dalam pendekatan analisis)
- Gagal replikasi (nggak bisa reproduce hasil kami)

### 3. Submit Perbaikan
Kalau kamu udah nemu kesalahan *dan* punya solusinya, langsung aja buka Pull Request (lihat [Proses Pull Request](#proses-pull-request)).

---

## Melaporkan Kesalahan

Buka Issue pakai template yang sesuai:

| Template | Untuk Apa |
|----------|---------|
| 🐛 **Kesalahan Kode** | Script error, output salah, atau hasilnya nggak keluar |
| 📊 **Kesalahan Data** | Nilai salah, sumber nggak cocok, data hilang |
| 🔁 **Masalah Replikasi** | Nggak bisa reproduce hasil dari paper kami |
| ❓ **Pertanyaan Metode** | Bukan error, cuma mau nanya tentang pendekatan |

Pas laporan, tolong sertakan:
- Repositori dan file yang mana
- Yang kamu harapkan vs. yang sebenarnya terjadi
- Sistem operasi kamu, versi Stata/R/Python
- Langkah-langkah buat reproduce masalahnya

---

## Kasih Saran Perbaikan

Kami welcome saran untuk:
- Pengembangan analisis yang udah ada
- Robustness check tambahan
- Pendekatan metodologi alternatif
- Sumber data yang lebih baik

Buat saran, lebih baik buka Discussion daripada Issue ya, karena ini bukan error dan lebih enak didiskusiin dulu bareng-bareng sebelum ada keputusan.

---

## Submit Koreksi Kode atau Data

Kalau kamu udah nemu kesalahan dan punya perbaikannya:

1. **Fork** repositori-nya
2. **Bikin branch** dengan nama yang jelas:
   ```
   fix/correct-cpi-deflator-2022
   fix/typo-in-regression-table-3
   ```
3. **Lakukan perubahan** — usahakan tetep minimal dan fokus ke satu masalah aja
4. **Test perubahannya** — jalanin do-files atau scripts yang relevan dan pastiin output-nya bener
5. **Buka Pull Request** — kasih referensi ke nomor Issue yang terkait

Kami usahain review Pull Request eksternal dalam **10 hari kerja**.

---

## Masalah Replikasi

Reproduksibilitas itu inti dari misi kami. Kalau kamu nggak bisa replikasi hasil kami:

1. Buka **Replication Issue** pakai template issue
2. Kasih tau persis paper/working paper mana yang kamu coba replikasi
3. Sebutin tabel atau gambar mana yang nggak bisa kamu reproduce
4. Share error message atau perbedaan yang kamu temuin

Kami serius soal masalah replikasi dan bakal respons dalam **5 hari kerja**.

Kalau replikasi butuh data yang nggak tersedia publik karena batasan lisensi, kami bakal jelasin di README repositori dan kasih instruksi cara dapetin aksesnya.

---

## Gaya & Standar

Semua kontribusi harus ikutin standar lab kami:

### Stata
- Do-files harus jalan dari atas ke bawah tanpa error di sesi yang bersih
- Pakai relative file paths — jangan pernah hardcode absolute paths
- Semua package harus dicantumkan di `00_setup.do` dengan `ssc install` atau `net install`
- Variabel harus dikasih label
- Pakai `// comments` buat jelasin langkah yang nggak obvious
- File output masuk ke `/output` — jangan pernah overwrite data mentah

### R
- Ikutin [tidyverse style guide](https://style.tidyverse.org/)
- Pakai `renv` untuk manajemen package dan commit `renv.lock`
- Semua scripts harus jalan dari R environment yang bersih
- Pakai `here::here()` untuk file paths — jangan pake `setwd()`

### Python
- Ikutin [PEP 8](https://peps.python.org/pep-0008/)
- Pakai `requirements.txt` atau `pyproject.toml` untuk dependencies
- Pakai relative paths di semua tempat

### Umum
- Jangan ada data sensitif, kredensial, atau API keys dalam commit apapun
- Jangan ada file data gede (>50MB) — pakai link Harvard Dataverse atau Zenodo aja
- Commit messages harus jelas dan jelasin *apa* yang berubah dan *kenapa*

---

## Proses Pull Request

1. Pastiin perubahanmu cuma untuk perbaikan atau fitur yang dijelaskan
2. Update README yang relevan kalau perubahanmu ngaruh ke cara jalanin kode
3. Kasih referensi Issue terkait di deskripsi PR-mu
4. Anggota lab bakal review PR-mu — sabar ya dan responsif ke feedback
5. Kalau udah disetujui, anggota lab dengan akses tulis bakal merge

Kami berhak nolak kontribusi yang di luar scope repositori atau nggak memenuhi standar kami, tapi kami bakal jelasin alasannya kok.

---

## Kode Etik

Semua interaksi di repositori DEN Economic Lab diatur sama [Kode Etik](CODE_OF_CONDUCT.md) kami. Kami harap semua orang bisa terlibat dengan sopan dan konstruktif. Pelecehan atau kontribusi dengan niat buruk bakal berakibat dikeluarin dari komunitas.

---

## Kontak

Buat pertanyaan yang nggak cocok untuk Issues atau Discussions publik:

📧 **Umum**: [contact@den-econ.id](mailto:contact@den-econ.id)
🐛 **Teknis**: Buka Issue di repositori yang relevan
💬 **Diskusi**: [github.com/orgs/den-econ/discussions](https://github.com/orgs/den-econ/discussions)

---

*DEN Economic Lab — Analisis Terbuka untuk Kepentingan Publik*
