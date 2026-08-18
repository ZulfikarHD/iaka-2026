# Industrial & Kaizen Reference Framework

This reference guide outlines standard terminology, analytical models, validation frameworks, and regulatory conventions for formal industrial and Kaizen papers.

---

## 1. Domain Terminology & Glossaries

| Term / Abbreviation | Full Name / Concept | Context & Application |
|---|---|---|
| **Inschiet** | Tingkat Kerusakan Cetak (*Defect Rate*) | Persentase lembar cetak rusak terhadap total volume produksi. |
| **HCS** | Hasil Cetak Sempurna | Lembar cetak yang memenuhi standar spesifikasi mutu dan sekuriti. |
| **HCTS** | Hasil Cetak Tidak Sempurna | Lembar cacat mutu yang wajib dimusnahkan dan direkonsiliasi. |
| **PCHT** | Pita Cukai Hasil Tembakau | Dokumen sekuriti pelunasan cukai tembakau/rokok (DJBC Kemenkeu). |
| **MMEA** | Minuman Mengandung Etil Alkohol | Dokumen sekuriti pelunasan cukai minuman beralkohol. |
| **PO / OBC** | Production Order / Order Batch Code | Nomor pesanan kerja produksi resmi pada sistem ERP/SAP. |
| **LK** | Lembar Kirim / Lembar Cetak | Satuan fisik lembaran dokumen sekuriti yang diproduksi. |
| **Cost of Inaction** | Biaya Pembiaran | Nilai kerugian terakumulasi jika suatu inefisiensi tidak ditangani. |
| **Cost Avoidance** | Penghematan Biaya | Nilai biaya tambah cetak yang berhasil dihindarkan melalui Kaizen. |
| **Data Silo** | Pemisahan Sistem Data | Kondisi data lapangan dan data sistem tidak terintegrasi. |

---

## 2. The 5-Pillar Cost of Inaction Matrix

When demonstrating the risks of inaction in Chapter 1, evaluate across these 5 operational pillars:

```markdown
Tabel 1.4 Matriks Risiko Pembiaran Operasional (*Cost of Inaction*)
| Pilar Evaluasi | Bentuk Risiko Nyata Bila Dibiarkan (*Inaction*) | Tingkat Keparahan | Indikator Dampak Terukur |
| :--- | :--- | :---: | :--- |
| **1. Biaya (*Cost*)** | Akumulasi pemborosan biaya cetak ulang (*re-print*) akibat bahan baku terbuang. | **KRITIS** | Beban biaya tambah cetak & margin laba. |
| **2. Mutu (*Quality*)** | Tingkat *inschiet* berfluktuasi tidak terkendali tanpa penanganan berkesinambungan. | **TINGGI** | Angka *defect rate* & risiko cacat lolos. |
| **3. Kepatuhan (*Compliance*)** | Hilangnya audit trail fisik, ketidaksesuaian dengan standar ISO 9001:2015. | **TINGGI** | Temuan audit operasional & ketertelusuran. |
| **4. K3L (*Safety & ESG*)** | Timbulan limbah padat kertas sekuriti (tonase), kelelahan operator shift malam. | **SEDANG** | Beban pemusnahan & risiko kelelahan kerja. |
| **5. Layanan (*Service SLA*)** | Keterlambatan pengiriman ke regulator (DJBC) akibat antrean tambah cetak. | **TINGGI** | Skor kepuasan pelanggan & denda penalti SLA. |
```

---

## 3. Methodologies & Quality Tools

### A. Root Cause Analysis (Fishbone 4M/5M)
- **Man (Manusia / Operasional):** Disparitas keahlian, kelelahan shift malam, ketidakseragaman penerapan SOP.
- **Machine (Mesin & Komponen):** Penurunan performa mekanis, keausan suku cadang, *preventive maintenance* tidak sinkron.
- **Method (Metode Kerja):** Standarisasi parameter setting mesin, pelaporan lisan, ketiadaan rekam jejak digital.
- **Material (Bahan Baku & Suhu):** Sensitivitas kertas sekuriti terhadap kelembaban udara (plooi/zig-zag), variasi lot tinta.

### B. Instrument Validation (For Surveys / User Testing)
- **Uji Validitas (Pearson Product Moment):** Menguji kesahihan butir kuesioner ($r_{\text{hitung}} > r_{\text{tabel}}$).
- **Uji Reliabilitas (Cronbach's Alpha):** Menguji konsistensi butir kuesioner ($\alpha \ge 0,60$ atau $\ge 0,80$ untuk kategori Sangat Kuat).
- **WebQual 4.0 Dimensions:** Usability (Kegunaan), Information Quality (Kualitas Informasi: Relevan, Akurat, Tepat Waktu, Lengkap), dan Interaction Quality (Kualitas Interaksi).

### C. Industry 4.0 & Readiness Standards
- **INDI 4.0 (Indonesia Industry Readiness Index 4.0):** Pilar manajemen, operasi cerdas, supply chain, dan pemberdayaan SDM.
- **TKT (Tingkat Kesiapterapan Teknologi):** TKT Level 9 untuk sistem yang telah teruji dan beroperasi penuh di lingkungan nyata pabrik.

---

## 4. Regulatory & Citation Guidelines

- **Regulasi BUMN / Peruri:** PP No. 06 Tahun 2019 (Penugasan Pencetakan Dokumen Sekuriti Negara).
- **Regulasi Transformasi Digital:** Perpres No. 18 Tahun 2020 (RPJMN Industri 4.0) dan Permenperin No. 21 Tahun 2020 (Asesmen INDI 4.0).
- **Format Sitasi Akademik / Industri:**
  * Lee, J., Kao, H.A., and Yang, S. (2014). *Service Innovation and Smart Analytics for Industry 4.0 and Big Data Environment*. Procedia CIRP.
  * Barnes, S.J., and Vidgen, R.T. (2003). *Measuring Web Site Quality Improvements: A Case Study of the Forum on the Forum for the Future*. Communications of the ACM.
  * Sugiyono. (2016). *Metode Penelitian Kuantitatif, Kualitatif, dan R&D*. Bandung: Alfabeta.
