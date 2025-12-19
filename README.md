# Analisis Pengaruh Literasi Digital dan Akses Internet terhadap Partisipasi Pendidikan di Indonesia Tahun 2022

## Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis pengaruh literasi digital dan akses internet terhadap tingkat partisipasi pendidikan di Indonesia pada tahun 2022. Analisis dilakukan pada tingkat provinsi dengan mengombinasikan beberapa indikator digital dan pendidikan untuk membentuk Indeks Kesiapan Digital Pendidikan.

Hasil analisis diharapkan dapat memberikan gambaran kondisi kesiapan digital pendidikan antar provinsi serta mengidentifikasi wilayah yang masih memerlukan perhatian dalam pengembangan infrastruktur dan literasi digital.

---

## Deskripsi Data
Dataset yang digunakan dalam penelitian ini merupakan data sekunder yang bersumber dari:
- **Indeks Literasi Digital**:

  Sumber: Kementerian Komunikasi dan Informatika (Kominfo) bekerja sama dengan Siberkreasi

  Menggambarkan kemampuan masyarakat dalam mengakses dan memanfaatkan teknologi digital.
- **Data Akses Internet**:

  Sumber: Badan Pusat Statistik (BPS)

  Persentase penduduk yang memiliki akses terhadap internet.
- **Angka Partisipasi Sekolah (APS)**:

  Sumber: Open Data Jawa Barat

  Data partisipasi pendidikan menurut kelompok umur (7–12 tahun, 13–15 tahun, dan 16–18 tahun).

Data dikumpulkan pada tingkat provinsi di Indonesia dan telah melalui proses pembersihan, standarisasi nama provinsi, serta penggabungan antar dataset.

---

## Deskripsi Variabel

| Nama Variabel | Deskripsi |
|--------------|----------|
| Provinsi | Nama provinsi di Indonesia |
| Indeks Literasi Digital (skala 1–5) | Tingkat kemampuan masyarakat dalam mengakses, memahami, dan memanfaatkan teknologi digital |
| Persentase Akses Internet (%) | Persentase penduduk yang memiliki akses internet |
| APS 7–12 Tahun (%) | Persentase penduduk usia 7–12 tahun yang masih bersekolah |
| APS 13–15 Tahun (%) | Persentase penduduk usia 13–15 tahun yang masih bersekolah |
| APS 16–18 Tahun (%) | Persentase penduduk usia 16–18 tahun yang masih bersekolah |
| APS Rata-rata (%) | Rata-rata Angka Partisipasi Sekolah dari tiga kelompok umur |
| lit_z (z-score) | Skor baku Indeks Literasi Digital |
| net_z (z-score) | Skor baku Persentase Akses Internet |
| Indeks Kesiapan Digital Pendidikan (rata-rata z-score) | Indeks komposit berbasis rata-rata skor baku literasi digital dan akses internet |
| Kategori_Litdig | Kategori tingkat literasi digital |
| Kategori_Internet | Kategori tingkat akses internet |
| Status_Kinerja | Kategori kesiapan digital pendidikan |
| Kategori_APS | Kategori tingkat partisipasi sekolah |

---

## Klasifikasi Kategori

### 🔹 Status Kinerja Kesiapan Digital Pendidikan (`Status_Kinerja`)

####  Aturan Klasifikasi (z-score)
Klasifikasi Status Kinerja dilakukan berdasarkan nilai Indeks Kesiapan Digital Pendidikan berbasis z-score:
- **Tertinggal**  : z-score < -1  
- **Berkembang**  : -1 ≤ z-score < 0  
- **Maju**        : 0 ≤ z-score < 1  
- **Sangat Maju** : z-score ≥ 1  

####  Interpretasi
- **Tertinggal**: Kesiapan digital pendidikan jauh di bawah rata-rata nasional.
- **Berkembang**: Kesiapan digital pendidikan masih berada di bawah rata-rata nasional.
- **Maju**: Kesiapan digital pendidikan berada di atas rata-rata nasional.
- **Sangat Maju**: Kesiapan digital pendidikan jauh di atas rata-rata nasional.

---

### 🔹 Kategori Literasi Digital (`Kategori_Litdig`)

####  Aturan Klasifikasi
- **Rendah** : 0 ≤ nilai < 3,45  
- **Sedang** : 3,45 ≤ nilai < 3,52  
- **Baik**   : 3,52 ≤ nilai < 3,59  
- **Tinggi** : nilai ≥ 3,59  

####  Interpretasi
- **Rendah**: Kemampuan literasi digital masyarakat masih terbatas.
- **Sedang**: Pemanfaatan teknologi digital mulai berkembang.
- **Baik**: Kemampuan literasi digital relatif baik dan merata.
- **Tinggi**: Kemampuan literasi digital sangat baik.

---

### 🔹 Kategori Akses Internet (`Kategori_Internet`)

####  Aturan Klasifikasi
- **Rendah** : 0 ≤ nilai < 82,95  
- **Sedang** : 82,95 ≤ nilai < 86,61  
- **Baik**   : 86,61 ≤ nilai < 88,68  
- **Tinggi** : nilai ≥ 88,68  

####  Interpretasi
- **Rendah**: Akses internet masih terbatas.
- **Sedang**: Akses internet berada pada tingkat menengah.
- **Baik**: Akses internet relatif baik dan merata.
- **Tinggi**: Akses internet sangat tinggi dengan dukungan infrastruktur yang baik.

---

### 🔹 Kategori Angka Partisipasi Sekolah (`Kategori_APS`)

####  Aturan Klasifikasi (Kuartil)
- **Rendah** : nilai < Q1  
- **Sedang** : Q1 ≤ nilai < Q2  
- **Baik**   : Q2 ≤ nilai < Q3  
- **Tinggi** : nilai ≥ Q3

####  Interpretasi
- **Rendah**: Tingkat partisipasi sekolah masih rendah.
- **Sedang**: Tingkat partisipasi sekolah berada pada tingkat menengah.
- **Baik**: Tingkat partisipasi sekolah relatif baik.
- **Tinggi**: Tingkat partisipasi sekolah sangat tinggi.

Pendekatan ini mengikuti prinsip *Exploratory Data Analysis* (Tukey, 1977).
