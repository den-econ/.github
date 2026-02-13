# Berkontribusi ke DEN Economic Lab

Terima kasih sudah tertarik dengan pekerjaan kami! DEN Economic Lab fokus pada analisis ekonomi yang terbuka dan bisa direproduksi siapa saja demi kepentingan publik Indonesia. Panduan ini menjelaskan bagaimana Anda — baik dari dalam maupun luar lab — bisa ikut berkontribusi di repositori kami.

---

## Daftar Isi

- [Siapa yang Bisa Kontribusi](#siapa-yang-bisa-kontribusi)
- [Cara Berkontribusi](#cara-berkontribusi)
- [Melaporkan Kesalahan](#melaporkan-kesalahan)
- [Memberikan Saran Perbaikan](#memberikan-saran-perbaikan)
- [Submit Koreksi Kode atau Data](#submit-koreksi-kode-atau-data)
- [Masalah Replikasi](#masalah-replikasi)
- [Gaya & Standar](#gaya--standar)
- [Proses Pull Request](#proses-pull-request)
- [Kode Etik](#kode-etik)
- [Kontak](#kontak)

---

## Siapa yang Bisa Kontribusi

**Peneliti eksternal, mahasiswa, dan siapa saja** boleh:
- Melaporkan kesalahan dalam analisis kami (data, kode, atau metodologi)
- Mengajukan pertanyaan tentang metode kami lewat GitHub Discussions
- Memberikan saran perbaikan atau ide pengembangan
- Submit koreksi lewat Pull Request

**Anggota Lab** mengikuti alur kerja internal yang ada di repositori [`.github-private`](https://github.com/den-econ/.github-private) kami.

---

## Cara Berkontribusi

### 1. Mengajukan Pertanyaan
Gunakan [GitHub Discussions](https://github.com/orgs/den-econ/discussions) untuk:
- Pertanyaan mengenai metodologi
- Permintaan klarifikasi mengenai sumber data
- Diskusi umum mengenai riset kami

Tolong cek dulu diskusi yang sudah ada sebelum membuat yang baru.

### 2. Melaporkan Kesalahan
Gunakan **GitHub Issues** (lihat [Melaporkan Kesalahan](#melaporkan-kesalahan) di bawah) untuk:
- Bug dalam kode (output salah, error saat menjalankan)
- Kesalahan data (nilai salah, ada data yang hilang)
- Masalah metodologi (potensi kesalahan dalam pendekatan analisis)
- Kegagalan replikasi (tidak dapat mereplikasi hasil kami)

### 3. Submit Perbaikan
Jika Anda sudah mengidentifikasi kesalahan *dan* punya solusinya, langsung saja buka Pull Request (lihat [Proses Pull Request](#proses-pull-request)).

---

## Melaporkan Kesalahan

Buka Issue menggunakan template yang sesuai:

| Template | Untuk Apa |
|----------|---------|
| 🐛 **Kesalahan Kode** | Script error, output salah, atau hasil tidak keluar |
| 📊 **Kesalahan Data** | Nilai salah, sumber tidak cocok, data hilang |
| 🔁 **Masalah Replikasi** | Tidak dapat mereplikasi hasil dari paper kami |
| ❓ **Pertanyaan Metode** | Bukan error, hanya pertanyaan mengenai pendekatan |

Saat melaporkan, tolong sertakan:
- Repositori dan file yang mana
- Yang Anda harapkan vs. yang sebenarnya terjadi
- Sistem operasi Anda, versi Stata/R/Python
- Langkah-langkah untuk mereproduksi masalahnya

---

## Memberikan Saran Perbaikan

Kami welcome saran untuk:
- Pengembangan pada analisis yang sudah ada
- Robustness check tambahan
- Pendekatan metodologi alternatif
- Sumber data yang lebih baik

Untuk saran, lebih baik buka Discussion daripada Issue, karena ini bukan error dan lebih baik didiskusikan dulu bersama sebelum ada keputusan.

---

## Submit Koreksi Kode atau Data

Jika Anda sudah mengidentifikasi kesalahan dan punya perbaikannya:

1. **Fork** repositori-nya
2. **Buat branch** dengan nama yang jelas:
   ```
   fix/correct-cpi-deflator-2022
   fix/typo-in-regression-table-3
   ```
3. **Lakukan perubahan** — usahakan tetap minimal dan fokus ke satu masalah saja
4. **Test perubahannya** — jalankan do-files atau scripts yang relevan dan pastikan output-nya benar
5. **Buka Pull Request** — berikan referensi ke nomor Issue yang terkait

Kami berusaha review Pull Request eksternal dalam **10 hari kerja**.

---

## Masalah Replikasi

Reproduksibilitas adalah inti dari misi kami. Jika Anda tidak dapat mereplikasi hasil kami:

1. Buka **Replication Issue** menggunakan template issue
2. Beritahu kami persis paper/working paper mana yang Anda coba replikasi
3. Sebutkan tabel atau gambar mana yang tidak dapat Anda replikasi
4. Share error message atau perbedaan yang Anda temukan

Kami serius soal masalah replikasi dan akan merespons dalam **5 hari kerja**.

Jika replikasi memerlukan data yang tidak tersedia publik karena batasan lisensi, kami akan menjelaskannya di README repositori dan memberikan instruksi cara mendapatkan aksesnya.

---

## Gaya & Standar

Semua kontribusi harus mengikuti standar lab kami:

### Stata
- Do-files harus berjalan dari atas ke bawah tanpa error di sesi yang bersih
- Gunakan relative file paths — jangan pernah hardcode absolute paths
- Semua package harus dicantumkan di `00_setup.do` dengan `ssc install` atau `net install`
- Variabel harus diberi label
- Gunakan `// comments` untuk menjelaskan langkah yang tidak obvious
- File output masuk ke `/output` — jangan pernah overwrite data mentah

### R
- Ikuti [tidyverse style guide](https://style.tidyverse.org/)
- Gunakan `renv` untuk manajemen package dan commit `renv.lock`
- Semua scripts harus berjalan dari R environment yang bersih
- Gunakan `here::here()` untuk file paths — jangan gunakan `setwd()`

### Python
- Ikuti [PEP 8](https://peps.python.org/pep-0008/)
- Gunakan `requirements.txt` atau `pyproject.toml` untuk dependencies
- Gunakan relative paths di semua tempat

### Umum
- Jangan ada data sensitif, kredensial, atau API keys dalam commit apapun
- Jangan ada file data besar (>50MB) — gunakan link Harvard Dataverse atau Zenodo saja
- Commit messages harus jelas dan menjelaskan *apa* yang berubah dan *kenapa*

---

## Proses Pull Request

1. Pastikan perubahan Anda hanya untuk perbaikan atau fitur yang dijelaskan
2. Update README yang relevan jika perubahan Anda mempengaruhi cara menjalankan kode
3. Berikan referensi Issue terkait di deskripsi PR Anda
4. Anggota lab akan review PR Anda — mohon bersabar dan responsif terhadap feedback
5. Jika sudah disetujui, anggota lab dengan akses tulis akan merge

Kami berhak menolak kontribusi yang di luar scope repositori atau tidak memenuhi standar kami, tapi kami akan menjelaskan alasannya.

---

## Kode Etik

Semua interaksi di repositori DEN Economic Lab diatur oleh [Kode Etik](CODE_OF_CONDUCT.md) kami. Kami berharap semua orang bisa terlibat dengan sopan dan konstruktif. Pelecehan atau kontribusi dengan niat buruk akan berakibat dikeluarkan dari komunitas.

---

## Kontak

Untuk pertanyaan yang tidak cocok untuk Issues atau Discussions publik:

📧 **Umum**: [contact@den-econ.id](mailto:contact@den-econ.id)
🐛 **Teknis**: Buka Issue di repositori yang relevan
💬 **Diskusi**: [github.com/orgs/den-econ/discussions](https://github.com/orgs/den-econ/discussions)

---

*DEN Economic Lab — Analisis Terbuka untuk Kepentingan Publik*
