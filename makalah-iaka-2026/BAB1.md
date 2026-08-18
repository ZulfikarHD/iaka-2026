# BAB 1: LATAR BELAKANG DAN MASALAH

> ***Executive Takeaway:***  
> Unit Cetak Pita Cukai mengelola rata-rata pesanan strategis negara sebesar **160.000.000 Lembar Cetak / tahun** (dengan volume aktual tahun 2025 mencapai **177.636.930 Lembar Cetak**). Sepanjang tahun 2025, rata-rata *inschiet* (tingkat kerusakan cetak) berfluktuasi pada level **4,61%** (puncak Q4 mencapai **5,11%**), yang merepresentasikan potensi kerugian pemborosan biaya tambah cetak sebesar **Rp 22,13 Miliar / tahun** (pada volume rata-rata) hingga **Rp 24,56 Miliar / tahun** (pada volume 2025). Pasca-implementasi SIRINE 2024 yang berhasil memetakan *defect category*, muncul titik buta operasional (*operational blind spot*) sejak Januari 2025: ketiadaan data granular per mesin dan per kondisi operasional (*shift*/tim). Ketiadaan data ini mengakibatkan inspeksi perbaikan mesin yang memakan waktu hingga **lebih dari 1 *shift* per mesin** (> 8 jam *downtime*), rekapitulasi data manual yang menumpuk saat Penilaian Pegawai Kuartalan / Akhir Kontrak, serta menghambat potensi efisiensi biaya miliaran rupiah bagi perusahaan. Implementasi DSS SIRINE 4.0 pada semester pertama 2026 berhasil memangkas *inschiet* menjadi **4,34% di Q1** dan **3,33% di Q2**, mengamankan penghematan riil sebesar **Rp 2,23 Miliar dalam 6 bulan** (dengan proyeksi tahunan mencapai **Rp 6,14 – Rp 6,82 Miliar / tahun**).

---

## 1.1 Kondisi Eksisting & Urgensi Operasional Unit Cetak

### 1.1.1 Profil Operasional & Karakteristik Produk Sekuriti Negara
Unit Cetak Pita Cukai – Perum Peruri merupakan unit produksi strategis yang bertanggung jawab atas pencetakan dokumen sekuriti negara dengan tingkat pengamanan dan kerahasiaan tinggi, utamanya **Pita Cukai Hasil Tembakau (PCHT)** dan **Minuman Mengandung Etil Alkohol (MMEA)**. Produk ini berfungsi sebagai instrumen pemungutan penerimaan negara di bawah pengawasan Direktorat Jenderal Bea dan Cukai (DJBC) Kementerian Keuangan Republik Indonesia.

Operasional di lapangan memiliki karakteristik dengan kompleksitas dan standar presisi tinggi:
* **Armada Mesin Produksi:** Mengoperasikan armada mesin cetak yang terdiri dari:
  * 4 Unit Mesin *Sheet-fed Offset Komori* (KMR1, KMR2, KMR3, KMR4)
  * 2 Unit Mesin *Offset Ryobi* (RYB1, RYB2)
  * 3 Unit Mesin cetak penunjang GTO (GTO-1, GTO-2, GTO-3)
* **Pola Kerja Operasional:** Beroperasi non-stop **24 jam sehari** dengan sistem **3 *shift* kerja bergilir** (*Shift* Pagi: 07.00–15.00 WIB, *Shift* Sore: 15.00–23.00 WIB, *Shift* Malam: 23.00–07.00 WIB) yang melibatkan $\pm 42$ orang operator cetak dan kepala kelompok di lapangan.
* **Fitur Sekuriti & Regulasi Mutu:** Menerapkan spesifikasi pengamanan bertingkat (*security paper* dengan serat kasat/tak kasat mata, *security ink* berpendar UV, *guilloche pattern*, *microtext*, serta *hologram foil*). Setiap lembar cetak yang mengalami deviasi mutu dikategorikan sebagai **HCTS (Hasil Cetak Tidak Sempurna)** dan wajib melalui proses rekonsiliasi, verifikasi, serta pemusnahan berkala yang diaudit secara ketat.

| Parameter Operasional | Nilai / Spesifikasi | Satuan | Periode Berlaku | Sumber Data Terverifikasi |
| :--- | :---: | :---: | :---: | :--- |
| **Armada Mesin Cetak Operasional** | **Komori (1–4), Ryobi (1–2), GTO (1–3)** | Unit Mesin | Aktif 2025–2026 | Data Inventaris Aset Departemen Produksi |
| **Pola Kerja Lini Produksi** | **3 (Pagi, Sore, Malam)** | *Shift* / Hari | Harian 2025 | Standar Pola Kerja Unit Cetak Pita Cukai |
| **Durasi Operasional Lini** | **24** | Jam / Hari | Harian 2025 | *Standard Operating Procedure* (SOP) Unit Cetak |
| **Tenaga Kerja Lapangan** | **$\pm 42$** | Personel | Tahun 2025 | Data Penugasan Gilir Kerja Seksi Cetak |
| **Rata-Rata Order Tahunan** | **160.000.000** | Lembar Cetak | Standar Tahunan | Perencanaan Kapasitas Produksi & PPIC |
| **Volume Order Aktual 2025** | **177.636.930** | Lembar Cetak | Tahun 2025 | Modul *SAP Production Order* (T-Code: `ZPPRSIPPC0012`) |
| **Realisasi Volume Q1 2026** | **57.385.254** | Lembar Cetak | Jan – Mar 2026 | Modul *SAP Production Order* (T-Code: `ZPPRSIPPC0012`) |
| **Realisasi Volume Q2 2026** | **45.960.434** | Lembar Cetak | Apr – Jun 2026 | Modul *SAP Production Order* (T-Code: `ZPPRSIPPC0012`) |

### 1.1.2 Keterbatasan Sistem Pencatatan Eksisting (*Data Silo* & Rekapitulasi Manual)
Meskipun mencetak jutaan lembar dokumen sekuriti negara setiap hari, sistem pencatatan operasional di lapangan pada Unit Cetak Pita Cukai hingga akhir tahun 2025 masih terfragmentasi ke dalam dua sistem terpisah (*data silo*):

1. **Sisi Kuantitas & Penugasan Lapangan:**
   Pencatatan hasil cetak tiap pegawai, nomor mesin, dan nomor PO masih mengandalkan **catatan manual pada buku folio fisik**. Data ini tidak direkap harian, melainkan **hanya direkap secara insidental saat ada kebutuhan khusus**, seperti momen **Penilaian Kinerja Pegawai Kuartalan** atau **Evaluasi Akhir Masa Kontrak**. Akibatnya, pada saat momen evaluasi tersebut tiba, proses rekapitulasi data dari tumpukan buku folio menjadi sangat menyita waktu, rentan kesalahan manusia (*human error*), serta meniadakan pemantauan performa harian yang berkesinambungan.
2. **Sisi Kualitas & Cacat Cetak (SAP & Verifikasi):**
   Data kerusakan hasil cetak (*inschiet*) ditarik dari sistem SAP (T-Code: `ZPPRSIPPC0012`) atau laporan Unit Verifikasi Pita Cukai. Namun, data ini hanya menyajikan **ringkasan global total kerusakan (*general summary*) di level unit**, tanpa atribusi detail ke nomor mesin pencetak, nomor PO spesifik, maupun tim/*shift* yang bertugas saat pencetakan berlangsung.

```
+---------------------------------------------------------------------------------------------------------+
|                    KONDISI EKSISTING SISTEM PENCATATAN OPERASIONAL (DATA SILO)                          |
+----------------------------------------------------+----------------------------------------------------+
|               SISI KUANTITAS LAPANGAN              |             SISI KUALITAS (SAP / VERIFIKASI)        |
+----------------------------------------------------+----------------------------------------------------+
| * Media: Buku Folio Fisik & Kartu Mesin            | * Media: Laporan SAP (T-Code: ZPPRSIPPC0012) / Verif |
| * Sifat: Manual, tulisan tangan, rawan hilang      | * Sifat: Ringkasan global unit, format CSV mentah  |
| * Rekap: Insidental (Penilaian Kuartal / Kontrak)  | * Batasan: Tidak tahu mesin & shift pencetak       |
| * Dampak: Evaluasi harian tidak berjalan           | * Respons Tindakan: Lambat & Trial-and-Error       |
+----------------------------------------------------+----------------------------------------------------+
```

### 1.1.3 Implikasi terhadap Kinerja Operasional & Pengambilan Keputusan
Ketiadaan jembatan data antara kuantitas lapangan dan kualitas verifikasi menimbulkan dampak langsung:
* **Respons Perbaikan Mesin Terhambat:** Waktu diagnosa dan penanganan teknis membengkak karena teknisi *maintenance* harus memeriksa mesin satu per satu (*trial-and-error*) yang dapat memakan waktu hingga **lebih dari satu *shift* kerja per mesin**.
* **Evaluasi Kinerja Tertunda & Subjektif:** Kepala Kelompok dan Kepala Unit kesulitan memberikan bimbingan teknis (*coaching*) secara tepat waktu karena data kinerja tim di buku folio baru direkap berbulan-bulan kemudian saat evaluasi kuartal/kontrak.
* **Tindakan Perbaikan Tidak Tepat Sasaran:** Manajemen tidak dapat membedakan apakah kenaikan *inschiet* murni disebabkan oleh kendala teknis mesin (*Machine*) atau faktor variasi metode kerja operator antar-*shift* (*Man & Method*).

---

## 1.2 Data Awal Pemicu Inovasi & Baseline Inschiet 2025

Sesuai standar verifikasi data mutu, seluruh data baseline yang memicu inisiasi proyek inovasi ini disajikan secara transparan dengan mencantumkan angka, satuan, periode, dan sumber data resmi.

### 1.2.1 Data Volume Produksi & Baseline Inschiet Kuartalan 2025
Sepanjang tahun anggaran 2025, total pesanan cetak Pita Cukai Hasil Tembakau (PCHT) mencapai **177.636.930 Lembar Cetak** (dengan estimasi rata-rata tahunan sebesar **160.000.000 Lembar Cetak**). Rekam data historis menunjukkan fluktuasi *inschiet* yang konsisten berada di level tinggi dengan rata-rata **4,61%**.

| Parameter Data | Nilai / Angka | Satuan | Periode | Sumber Data Terverifikasi |
| :--- | :---: | :---: | :---: | :--- |
| **Rata-Rata Order Tahunan** | **160.000.000** | Lembar Cetak | Standar Tahunan | Perencanaan Kapasitas Produksi & PPIC |
| **Total Order Produksi 2025** | **177.636.930** | Lembar Cetak | Tahun 2025 | Modul *SAP Production Order* (T-Code: `ZPPRSIPPC0012`) |
| **Inschiet Kuartal 1 (Q1)** | **4,72%** | Persentase (%) | Jan – Mar 2025 | Rekap Verifikasi Mutu & SAP (`ZPPRSIPPC0012`) |
| **Inschiet Kuartal 2 (Q2)** | **3,97%** | Persentase (%) | Apr – Jun 2025 | Rekap Verifikasi Mutu & SAP (`ZPPRSIPPC0012`) |
| **Inschiet Kuartal 3 (Q3)** | **4,64%** | Persentase (%) | Jul – Sep 2025 | Rekap Verifikasi Mutu & SAP (`ZPPRSIPPC0012`) |
| **Inschiet Kuartal 4 (Q4)** | **5,11%** | Persentase (%) | Okt – Des 2025 | Rekap Verifikasi Mutu & SAP (`ZPPRSIPPC0012`) |
| **RATA-RATA BASELINE 2025** | **4,61%** | Persentase (%) | Tahun 2025 | Konsolidasi Tahunan SIRINE & SAP (`ZPPRSIPPC0012`) |
| **Durasi Trial Maintenance** | **> 1 *Shift* (> 8 Jam)** | Jam / Mesin | Tahun 2025 | *Maintenance Log* & Laporan Kerusakan Mesin |

### 1.2.2 Analisis Fluktuasi Kuartalan Baseline 2025
Fluktuasi *inschiet* sepanjang tahun 2025 memberikan dua temuan empiris utama:
1. **Kapabilitas Proses:** Pada **Q2 2025**, *inschiet* berhasil menyentuh angka **3,97%**, membuktikan bahwa proses produksi secara teknis mampu mencapai level di bawah 4,00%.
2. **Kerentanan Desain Baru:** Pada **Q4 2025**, terjadi lonjakan tajam hingga menyentuh angka **5,11%** (+1,14 pp dibanding Q2). Hal ini dipicu oleh tingginya volume pesanan desain baru pita cukai menjelang akhir tahun yang tidak didukung oleh sistem pemantauan performa mesin secara *real-time*.

![Grafik Baseline Inschiet Cetak per Kuartal 2025](../extracted_images/image1.png)
*Gambar 1.1: Grafik Distribusi Inschiet Cetak per Kuartal 2025 vs Garis Rata-rata Baseline 4,61% (Sumber: Rekap SIRINE & SAP ZPPRSIPPC0012)*

> ***Business Insight* Gambar 1.1:**  
> Garis putus-putus oranye menunjukkan rata-rata baseline tahunan sebesar **4,61%**. Lonjakan batang Q4 ke level **5,11%** menegaskan bahwa ketiadaan sistem diagnostik berbasis kondisi mesin dan *shift* di lapangan mengakibatkan lonjakan volume pesanan selalu berbanding lurus dengan pembengkakan angka lembar rusak.

### 1.2.3 Konversi Dampak Penghematan Realisasi 2026 (*Inschiet* $\rightarrow$ Lembar $\rightarrow$ Rupiah)
Dengan mengacu pada **Rata-Rata Baseline 2025 (4,61%)** sebagai titik tolak perbandingan (*benchmark*), berikut adalah konversi riil penurunan *inschiet* terhadap jumlah lembar rusak yang diselamatkan serta nilai efisiensi finansial (*cost avoidance*) pada realisasi produksi Semester 1 tahun 2026:

| Periode Realisasi | Volume Produksi ($n$) | Inschiet (%) | Penurunan vs Baseline (4,61%) | Lembar Ekspektasi Cacat (Baseline 4,61%) | Lembar Cacat Aktual Realisasi | Lembar Diselamatkan (*Defect Reduction*) | Nilai Penghematan Riil ($\times \text{Rp } 3.000$) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Q1 2026** *(Masa Adaptasi)* | **57.385.254** | **4,34%** | -0,27 pp (-5,86%) | 2.645.460 lb | 2.490.520 lb | **154.940 Lembar** | **Rp 464.820.000** *(Rp 464,82 Juta)* |
| **Q2 2026** *(Tindakan Presisi)* | **45.960.434** | **3,33%** | **-1,28 pp (-27,77%)** | 2.118.776 lb | 1.530.482 lb | **588.294 Lembar** | **Rp 1.764.882.000** *(Rp 1,76 Miliar)* |
| **TOTAL SEMESTER 1 2026** | **103.345.688** | **3,89%** *(avg)* | **-0,72 pp (-15,62%)** | 4.764.236 lb | 4.021.002 lb | **743.234 Lembar** | **Rp 2.229.702.000** *(Rp 2,23 Miliar)* |

> ***Key Financial Insight Table 1.2.3:***  
> 1. Pada **Q1 2026**, penurunan *inschiet* sebesar **0,27 pp** pada masa adaptasi sistem berhasil menyelamatkan **154.940 lembar** cetak senilai **Rp 464,82 Juta**.  
> 2. Pada **Q2 2026**, setelah implementasi penuh tindakan presisi berbasis data granular mesin & *shift*, penurunan *inschiet* melesat hingga **1,28 pp** (mencapai **3,33%**), menyelamatkan **588.294 lembar** cetak senilai **Rp 1,76 Miliar** hanya dalam satu kuartal.  
> 3. Secara akumulatif, dalam kurun waktu 6 bulan pertama implementasi (Januari – Juni 2026), inovasi ini telah mengamankan efisiensi biaya nyata sebesar **Rp 2,23 Miliar** dari **743.234 lembar** kertas sekuriti yang terselamatkan dari pemborosan.

---

## 1.3 Identifikasi Masalah Operasional: *The Operational Blind Spot*

### 1.3.1 Ruang Lingkup Masalah: Apa, Di Mana, Sejak Kapan, dan Siapa Terdampak
Untuk memenuhi standar identifikasi masalah yang terukur, ruang lingkup permasalahan didefinisikan sebagai berikut:

* **Apa yang Terjadi:** Ketidakmampuan mengidentifikasi kontribusi kerusakan cetak (*inschiet*) per mesin dan per kondisi operasional (*shift*/tim), yang mengakibatkan pemborosan biaya tambah cetak, tingginya waktu henti mesin (*downtime*) akibat perbaikan spekulatif, dan proses evaluasi kinerja yang lambat serta rentan bias.
* **Di Proses & Unit Mana:** Proses Cetak *Offset*, Unit Cetak Pita Cukai, Departemen Produksi Dokumen Sekuriti.
* **Sejak Kapan:** Teridentifikasi secara kritis sejak **Januari 2025** (pasca-penerapan SIRINE 2024 mencapai titik jenuh / *plateau effect*).
* **Pihak yang Terdampak Langsung:**
  1. *Operator Cetak Lapangan ($\pm 42$ orang):* Kesulitan mengetahui tingkat cacat hasil cetaknya secara harian dan tidak memperoleh umpan balik kinerja yang objektif.
  2. *Kepala Kelompok & Kepala Unit:* Mengalami penumpukan beban rekapitulasi data buku folio saat evaluasi berkala (Penilaian Kuartalan / Akhir Kontrak) sehingga kesulitan memberikan *coaching* yang tepat sasaran.
  3. *Teknisi Maintenance:* Kehilangan waktu kerja hingga **lebih dari 1 *shift* (> 8 jam per mesin)** karena harus memeriksa seluruh armada mesin secara bergiliran (*trial-and-error*).
  4. *Departemen PPIC & Manajemen:* Kesulitan melakukan perencanaan kapasitas produksi dan alokasi mesin yang presisi akibat tidak adanya data performa riil per mesin.
  5. *Pelanggan Utama (DJBC Kemenkeu RI):* Menghadapi potensi risiko keterlambatan pengiriman pesanan pita cukai akibat tingginya siklus cetak ulang (*re-print*).

### 1.3.2 Retrospeksi SIRINE 2024 vs Titik Buta Baru 2025 (*The Missing Link*)
Pada ajang IAKA 2024, inovasi SIRINE berhasil menurunkan *inschiet* dari **5,61%** menjadi **4,06%** (-27,63%) dengan memetakan rincian jenis kerusakan secara umum di level unit. Namun pada tahun 2025, ketersediaan data jenis kerusakan umum saja tidak lagi memadai.

```
+---------------------------------------------------------------------------------------------------------+
|                               EVOLUSI TITIK BUTA OPERASIONAL UNIT CETAK                                 |
+----------------------------------------------------+----------------------------------------------------+
|                SIRINE VERSI 2024                   |                   KONDISI 2025                     |
|            (Sudah Berhasil Terjawab)               |               (Titik Buta Baru / Gap)              |
+----------------------------------------------------+----------------------------------------------------+
| ✅ "Jenis kerusakan apa yang mendominasi unit?"     | ❌ "Pada MESIN MANA kerusakan tersebut terjadi?"    |
| (Contoh: Mengetahui bahwa cacat 'blobor' tinggi)   | ❌ "Apakah akibat FAKTOR MESIN atau KONDISI SHIFT?"|
|                                                    | ❌ "Berapa kontribusi kuantitas & cacat PER TIM?"   |
+----------------------------------------------------+----------------------------------------------------+
```

### 1.3.3 Studi Kasus Inefisiensi di Lapangan
Ketiadaan data granular menimbulkan dua skenario inefisiensi nyata:
1. **Pemeriksaan Mesin Sistem *Trial-and-Error* yang Menghabiskan Waktu *Shift*:**  
   Pada Juni 2025, data SIRINE menunjukkan cacat *"blobor"* mendominasi hasil cetak. Namun, karena tidak diketahui mesin mana yang menghasilkan cacat tersebut, teknisi memeriksa armada mesin secara bergiliran. Sumber masalah sebenarnya berada pada Mesin **Komori 3 (KMR3)**. Karena mesin lain diperiksa terlebih dahulu, teknisi menghabiskan waktu hingga **lebih dari satu *shift* kerja (> 8 jam *downtime*)**, sementara lembar rusak terus bertambah pada KMR3 sebelum sempat tertangani.
2. **Bias Diagnosa: Kendala Teknis Mesin vs Variasi *Shift* (*Man & Method*):**  
   Dengan variasi *shift* per hari, performa cetak sangat bervariasi. Ketika mesin KMR3 di *Shift* Malam menunjukkan *inschiet* 8,5%, sedangkan di *Shift* Pagi pada mesin yang sama hanya menghasilkan 2,5%, akar masalah bukan berada pada kendala teknis mesin, melainkan pada prosedur kerja, kelelahan, atau ketelitian operator di *Shift* Malam. Tanpa data granular per *shift*, teknisi keliru menyetel ulang mesin, padahal yang dibutuhkan adalah pendampingan operasional (*coaching*).

---

## 1.4 Skala Dampak Finansial & Risiko Pembiaran (*Cost of Inaction*)

### 1.4.1 Kertas Kerja Dampak Finansial Baseline 2025
Persentase *inschiet* sebesar **4,61%** menimbulkan beban finansial masif. Estimasi biaya tambah cetak internal adalah **Rp 3.000 / lembar cetak** (mencakup kertas sekuriti berserat khusus, tinta cetak sekuriti berpendar, depresiasi jam mesin, dan alokasi tenaga kerja).

Perhitungan disajikan dalam dua skenario (Rata-rata Order Tahunan vs Order Aktual 2025):

#### A. Berdasarkan Rata-Rata Order Tahunan (160.000.000 Lembar):
$$\begin{aligned}
\text{Volume Rata-Rata Order Tahunan} &= 160.000.000 \text{ Lembar Cetak} \\
\text{Baseline Inschiet (4,61\%)} &= 160.000.000 \times 4,61\% = \mathbf{7.376.000 \text{ Lembar Rusak / Tahun}} \\
\text{Nilai Kerugian Finansial Baseline} &= 7.376.000 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 22.128.000.000 \text{ / Tahun}} \\
&\approx \mathbf{\text{Rp } 22,13 \text{ Miliar / Tahun (atau Rp 1,84 Miliar / Bulan)}}
\end{aligned}$$

#### B. Berdasarkan Volume Order Aktual 2025 (177.636.930 Lembar):
$$\begin{aligned}
\text{Total Volume Order Aktual 2025} &= 177.636.930 \text{ Lembar Cetak} \\
\text{Baseline Inschiet (4,61\%)} &= 177.636.930 \times 4,61\% = \mathbf{8.189.062 \text{ Lembar Rusak / Tahun}} \\
\text{Nilai Kerugian Finansial 2025} &= 8.189.062 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 24.567.186.000 \text{ / Tahun}} \\
&\approx \mathbf{\text{Rp } 24,56 \text{ Miliar / Tahun (atau Rp 2,05 Miliar / Bulan)}}
\end{aligned}$$

### 1.4.2 Simulasi Valuasi Penghematan Tiap 1,00% Penurunan Inschiet
Setiap keberhasilan mereduksi **1,00% (100 basis poin)** *inschiet* secara langsung mengamankan efisiensi biaya (*cost avoidance*) yang signifikan:

* **Pada Rata-Rata Order Tahunan (160 Juta Lembar):**
  $$\text{Penghematan per 1,00\%} = (160.000.000 \times 1,00\%) \times \text{Rp } 3.000 = 1.600.000 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 4.800.000.000 \text{ / Tahun (Rp 4,80 Miliar)}}$$
* **Pada Volume Order 2025 (177,6 Juta Lembar):**
  $$\text{Penghematan per 1,00\%} = (177.636.930 \times 1,00\%) \times \text{Rp } 3.000 = 1.776.369 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 5.329.107.000 \text{ / Tahun (Rp 5,33 Miliar)}}$$

![Skema Dampak Finansial Kerugian dan Potensi Penghematan Inschiet](../extracted_images/image3.png)
*Gambar 1.2: Diagram Alur Skala Finansial Kerugian Inschiet Baseline 4,61% vs Potensi Penghematan Tiap 1% Penurunan (Sumber: Kertas Kerja Finansial Unit Cetak)*

> ***Business Insight* Gambar 1.2:**  
> Pada tingkat baseline 4,61%, perusahaan menanggung beban kerugian antara **Rp 22,13 Miliar s.d. Rp 24,56 Miliar/tahun**. Setiap perbaikan proses yang mampu memangkas 1% *inschiet* menghasilkan *cost avoidance* nyata sebesar **Rp 4,80 Miliar s.d. Rp 5,33 Miliar/tahun**.

### 1.4.3 Matriks Risiko Pembiaran Terintegrasi (*The 5 Pillars Cost of Inaction*)
Bila kondisi ketiadaan sistem integrasi data granular ini dibiarkan terus berlangsung tanpa intervensi inovasi, unit kerja dan perusahaan menghadapi risiko pada 5 pilar evaluasi:

| Pilar Evaluasi | Bentuk Risiko Nyata Bila Dibiarkan (*Inaction*) | Tingkat Keparahan | Indikator Dampak Terukur |
| :--- | :--- | :---: | :--- |
| **1. Biaya (*Cost*)** | Akumulasi pemborosan biaya cetak ulang (*re-print*) mencapai **Rp 22,13 – Rp 24,56 Miliar per tahun** akibat terbuangnya bahan baku berharga tinggi. | **KRITIS** | Beban biaya tambah cetak & penurunan margin laba unit. |
| **2. Mutu (*Quality*)** | Tingkat *inschiet* berfluktuasi tidak terkendali hingga **5,11%**. Ketiadaan data historis mesin membuat tindakan perbaikan kualitas tidak bertahan lama. | **TINGGI** | Angka *defect rate* tinggi dan risiko lembar cacat lolos ke proses lanjutan. |
| **3. Kepatuhan (*Compliance*)** | Pelanggaran standar akuntabilitas pelacakan (*traceability*) dokumen sekuriti negara karena pencatatan produksi manual di buku folio tidak dapat diaudit secara digital. | **TINGGI** | Temuan audit operasional internal dan ketidaksesuaian standar ISO 9001:2015. |
| **4. K3L (*Safety & ESG*)** | Tumpukan limbah padat kertas sekuriti mencapai **7,37 – 8,18 Juta lembar / tahun** ($\pm 60–65$ Ton kertas terbuang). Peningkatan kelelahan kerja operator di *Shift* Malam. | **SEDANG** | Beban pemusnahan limbah sekuriti dan potensi kecelakaan kerja akibat kelelahan. |
| **5. Layanan (*Service SLA*)** | Keterlambatan serah terima pesanan pita cukai ke DJBC akibat antrean *re-print*, yang berisiko mengganggu kelancaran pasokan pita cukai ke industri nasional. | **TINGGI** | Penurunan skor kepuasan pelanggan DJBC dan ancaman denda keterlambatan SLA. |

---

### Kesimpulan Bab 1
Berdasarkan kondisi eksisting di lapangan, data baseline terverifikasi dari SIRINE dan SAP (T-Code: `ZPPRSIPPC0012`), serta analisis risiko 5 pilar di atas, pengembangan **Decision Support System (DSS) SIRINE 4.0** menjadi kebutuhan mendesak (*operational imperative*). Bukti empiris Semester 1 2026 yang mengamankan penghematan **Rp 2,23 Miliar (743.234 lembar diselamatkan)** membuktikan efektivitas sistem dalam mengubah data granular menjadi tindakan presisi. Analisis akar penyebab masalah ini akan dibedah secara komprehensif pada Bab 2.
