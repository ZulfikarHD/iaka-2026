# DOKUMEN INOVASI & KAIZEN IAKA 2026
## DSS SIRINE 4.0: Decision Support System Terintegrasi Berbasis Granularitas Data Mesin & Kondisi Operasional untuk Mereduksi Inschiet Cetak Pita Cukai

---

## 📌 RINGKASAN EKSEKUTIF (EXECUTIVE SUMMARY)
> **Pitch Takeaway:** Transformasi operasional unit cetak dari sistem pencatatan manual berbasis buku folio menjadi ekosistem data terintegrasi real-time yang memangkas inschiet dan mengamankan potensi efisiensi miliaran rupiah.

* **Identitas Proyek:**
  * **Judul Inovasi:** DSS SIRINE 4.0 (Decision Support System Unit Cetak Pita Cukai)
  * **Kategori:** Kaizen / Inovasi Proses & Digitalisasi Operasional
  * **Unit Kerja:** Unit Cetak Pita Cukai – Perum Peruri
  * **Fasilitator:** [Nama & Jabatan minimal Kepala Departemen]
* **Highlight Hero Metrics:**
  * **Baseline Inschiet (2025):** `4,61%` (Puncak Q4: `5,11%`)
  * **Realisasi Akhir (Q2 2026):** `3,33%` (**Penurunan: -1,28 pp / -27,8%**)
  * **Net Financial Impact:** **Efisiensi ~Rp 6,82 Miliar / Tahun** (Cost Avoidance)
  * **Payback Period:** **0 Bulan (Seketika)** – *100% In-house Development*

---

# BAB 1: LATAR BELAKANG DAN MASALAH

## 1.1 Latar Belakang (Operational Context & Baseline Data)
> **Tujuan:** Membangun urgensi operasional dan menyajikan data awal terverifikasi (angka, satuan, periode, sumber data).

* **Kondisi Eksisting Unit Cetak Pita Cukai:**
  * Skala operasional (6 lini mesin: Komori 1–4, Ryobi 1–2, 3 shift kerja harian).
  * Kuantitas produksi: Pencatatan manual menggunakan buku folio dan rekap manual kepala kelompok.
  * Kualitas produksi: Laporan inschiet SAP/Verifikasi bersifat global per unit tanpa rincian mesin & shift.
* **Urgensi bagi Perusahaan:**
  * Perlindungan bahan baku bernilai tinggi (kertas sekuriti & tinta khusus).
  * Pemenuhan SLA dan ketepatan pengiriman pesanan Pita Cukai Hasil Tembakau (PCHT) & MMEA ke Bea Cukai.
* **Data Awal Pemicu Inovasi:**
  * Total Volume Produksi PCHT 2025: `177.636.930 Lembar Cetak` (Sumber: SAP / PPIC 2025).
  * Fluktuasi Baseline Inschiet 2025:
    * Kuartal 1: `4,72%`
    * Kuartal 2: `3,97%`
    * Kuartal 3: `4,64%`
    * Kuartal 4: `5,11%` (Puncak lonjakan)
    * **Rata-rata Baseline 2025: 4,61%**
* **Slot Visual / Grafik:**
  * `[VISUAL: Bar Chart Inschiet Cetak per Kuartal 2025 vs Garis Rata-rata 4,61%]` *(Asset: image1.png / image2.png)*

## 1.2 Masalah Operasional & Skala Dampak Finansial (The Blind Spot & Financial Exposure)
> **Tujuan:** Menyatakan masalah operasional terukur dan membuktikan risiko finansial jika masalah dibiarkan.

* **Identifikasi Masalah (The Blind Spot Pasca-SIRINE 3.5 (2024)):**
  * SIRINE 3.5 (2024) berhasil memetakan *jenis kerusakan* (inschiet turun ke 4,06% di akhir 2024).
  * Memasuki 2025 timbul titik buta baru: *Tidak dapat diketahui mesin mana dan kondisi operasional shift/tim mana yang menjadi sumber masalah utama.*
  * Pemeriksaan mesin dilakukan secara bergilir tanpa prioritas data, memperpanjang *downtime* dan membiarkan mesin bermasalah tetap beroperasi.
* **Kertas Kerja Skala Dampak Finansial:**
  * Asumsi Biaya Tambah Cetak: `Rp 3.000 / lembar` (Bahan baku, tinta sekuriti, jam kerja, overhead mesin).
  * Total Lembar Rusak Eksisting (4,61%): `8.189.062 lembar/tahun` $\approx$ **Rp 24,56 Miliar/tahun**.
  * Valuasi Tiap 1% Inschiet: `1.776.369 lembar/tahun` $\approx$ **Rp 5,329 Miliar/tahun**.
* **Slot Visual / Skema:**
  * `[VISUAL: Diagram Alur Skala Dampak Finansial & Potensi Penghematan per 1% Inschiet]` *(Asset: image3.png)*
* **Dampak Risiko Jika Kondisi Dibiarkan:**
  * **Biaya:** Akumulasi kerugian tambah cetak miliaran rupiah per tahun.
  * **Mutu & Kepatuhan:** Risiko komplain cacat mutu dan penolakan produk oleh Bea Cukai.
  * **People:** Evaluasi performa operator subjektif dan rawan *human error* tanpa basis data valid.

---

# BAB 2: ANALISIS PENYEBAB

## 2.1 Analisis Akar Masalah (Metode Fishbone 4M)
> **Tujuan:** Menunjukkan dekonstruksi akar penyebab masalah menggunakan Fishbone Diagram.

* **Pemetaan 4 Kategori Penyebab (Man, Machine, Method, Material):**
  * **Man (Faktor Manusia/Operasional):** Disparitas kelelahan/kewaspadaan antar shift (terutama shift malam); pemahaman SOP penanganan masalah belum seragam.
  * **Machine (Kondisi Mesin Cetak):** Penurunan performa komponen mesin lama; jadwal *preventive maintenance* belum sinkron dengan riwayat kerusakan aktual.
  * **Method (Metode Kerja & Prosedur):** Standarisasi setting awal mesin belum seragam; pelaporan troubleshooting masih lisan/manual; ketiadaan referensi digital error berulang.
  * **Material (Bahan Baku & Lingkungan):** Sensitivitas kertas sekuriti terhadap suhu/kelembaban gudang (memicu plooi, zig-zag); kestabilan bahan baku supplier.
* **Slot Visual / Diagram:**
  * `[VISUAL: Diagram Fishbone 4M Faktor Inschiet Cetak Pita Cukai]` *(Asset: image4.png)*

## 2.2 Akar Masalah Utama (The Systemic Root Cause)
> **Tujuan:** Menyimpulkan *core bottleneck* sistemik yang harus diselesaikan oleh inovasi.

* **Temuan Akar Masalah Sistemik:**
  * Terisolasinya data produksi SAP, data verifikasi mutu, dan data penugasan fisik (buku folio).
  * Manajemen tidak memiliki instrumen diagnostik terpadu untuk membedakan secara objektif: *apakah lonjakan inschiet disebabkan oleh degradasi teknis mesin (Machine) atau faktor variasi operasional tim/shift (Man & Method).*

---

# BAB 3 - BAB 4: SOLUSI DAN KEBARUAN

## 3.1 Konsep & Mekanisme Kerja DSS SIRINE 4.0
> **Tujuan:** Menjelaskan mekanisme solusi dalam mengatasi akar masalah secara sistematis (sebab-akibat).

* **Konsep Arsitektur 2 Lapisan (Two-Tier Architecture):**
  * **Lapisan 1 (Data Capture & Entry):** Konfirmasi PO Digital + Manajemen Jadwal & Template Gilir Operator.
  * **Lapisan 2 (Analytics & Prescriptive Decision):** Engine pemrosesan data mentah SAP + Verifikasi HCTS menjadi visualisasi granular per mesin, per shift, dan per jenis kerusakan.
* **Slot Visual / Arsitektur:**
  * `[VISUAL: Diagram Evolusi SIRINE 3.5 (2024) ke DSS SIRINE 2026]` *(Asset: image5.png)*
  * `[VISUAL: Diagram Arsitektur Sistem 2 Lapisan & Aliran Data]` *(Asset: image6.png)*

## 3.2 Breakdown 6 Modul Fitur Unggulan
* **Fitur 1 – Form Entry Konfirmasi PO Cetak:** Digitalisasi input per PO dengan *autofill* spesifikasi produk & nama tim gilir *(Asset: image7.png)*.
* **Fitur 2 – Jadwal & Template Operator Cetak:** Pengaturan grid mingguan mesin $\times$ shift dan rotasi otomatis *(Asset: image8.png, image9.png)*.
* **Fitur 3 – Dashboard Produksi Mesin Cetak:** Konversi data mentah SAP (*`image10.png`*) menjadi metrik kuantitas & inschiet per lini mesin *(Asset: image11.png – image15.png)*.
* **Fitur 4 – Dashboard Produksi Unit Cetak:** Evaluasi volume LK dan persentase cacat per tim/shift (*traceability*).
* **Fitur 5 – Modul Audit Jenis Kerusakan Tiap Mesin:** Pareto jenis kerusakan HCTS spesifik per mesin *(Asset: image16.png, image17.png)*.
* **Fitur 6 – Floor-Level Real-Time Andon Display:** Layar informasi real-time di lantai produksi (auto-refresh 60 detik) untuk monitoring langsung *(Asset: image18.png – image21.png)*.

## 3.3 Unsur Kebaruan & Nilai Tambah (Matriks Kapabilitas)
> **Tujuan:** Menampilkan keunggulan komparatif solusi dibanding cara kerja sebelumnya.

* **Tabel Matriks Kapabilitas:**
  * Perbandingan 6 parameter kapabilitas: Pra-2024 vs SIRINE 3.5 (2024) vs DSS SIRINE 4.0 (2026).

## 3.4 Alur Proses Kerja: Before $\rightarrow$ After
* **Slot Visual / Alur Kerja:**
  * `[VISUAL: Flowchart Alur Kerja Sebelum Implementasi SIRINE 4.0]` *(Asset: image22.png)*
  * `[VISUAL: Flowchart Alur Kerja Sesudah Implementasi DSS SIRINE 4.0]` *(Asset: image23.png)*

## 3.5 Target Perbaikan & Rencana MVP
* **Target Kuantitatif Fase 1:** Menurunkan inschiet dari baseline `4,61%` ke target `< 4,00%` (-0,61 pp).
* **Calon Fasilitator Proyek:** Kepala Departemen Khazanah dan Verifikasi Strategic Business Unit High Security Solution.

---

# BAB 5 - BAB 6: IMPLEMENTASI DAN VALIDASI

## 5.1 Lingkup Uji Coba & Timeline Eksekusi (Roadmap)
> **Tujuan:** Menjelaskan parameter pengujian nyata (lokasi, mesin, shift, PIC, durasi).

* **Ruang Lingkup Uji:** 6 Mesin Cetak (Komori 1–4, Ryobi 1–2), 3 Shift Kerja, Unit Cetak Pita Cukai Perum Peruri.
* **Matriks Peran & Tanggung Jawab PIC:**
  * PIC Kelompok: Input transaksi per PO via form digital.
  * Kepala Kelompok: Verifikasi kelengkapan data di akhir shift.
  * Kepala Unit / Supervisor: Eksekutor keputusan maintenance & coaching harian/mingguan.
* **Slot Visual / Roadmap:**
  * `[VISUAL: Gantt Chart Roadmap Implementasi DSS SIRINE 2026 (Okt 2025 – Jun 2026)]` *(Asset: image24.png)*

## 5.2 Kendala Lapangan & Problem Solving
* **Tantangan 1 (Resistensi Input Data):** Beban kerja fisik operator $\rightarrow$ *Mitigasi:* Fitur *auto-fill* otomatis & *quick-save shortcut* (Ctrl+S).
* **Tantangan 2 (Lag Adaptasi Data Q1):** Disiplin input belum merata $\rightarrow$ *Mitigasi:* Standardisasi prosedur serah terima shift oleh Kepala Kelompok.

## 5.3 Data Validasi Before vs After
> **Tujuan:** Menyajikan tabel Before vs After tervalidasi dengan jumlah sampel ($n$) dan grafik tren.

* **Tabel Perbandingan Kinerja Kuartalan:**
  * Baseline 2025: `4,61%` ($n = 177,63$ Juta lembar)
  * Realisasi Q1 2026: `4,34%` ($\Delta = -0,27\text{ pp} / -5,9\%$) *(Masa Adaptasi)*
  * Realisasi Q2 2026: `3,33%` ($\mathbf{\Delta = -1,28\text{ pp} / -27,8\%}$) *(Full Data-Driven Action)*
* **Slot Visual / Grafik Validasi:**
  * `[VISUAL: Bar Chart Tren Inschiet 2025 s.d. Q2 2026]` *(Asset: image25.png)*

---

# BAB 7 - BAB 8: DAMPAK BISNIS (BUSINESS & MULTI-DIMENSIONAL IMPACT)

## 7.1 Kertas Kerja Dampak Finansial Terbuka (Financial ROI Model)
> **Tujuan:** Perhitungan matematis transparan mengenai *Cost Avoidance* dan *Payback Period*.

* **Formula & Perhitungan Penghematan Tahunan:**
  $$\text{Volume Tahunan} = 177.636.930 \text{ Lembar Cetak}$$
  $$\text{Reduksi Inschiet (Baseline 4,61\%} \rightarrow \text{Q2 3,33\%)} = 1,28 \text{ pp}$$
  $$\text{Pengurangan Lembar Rusak} = 177.636.930 \times 1,28\% = \mathbf{2.273.752 \text{ Lembar / Tahun}}$$
  $$\text{Valuasi Efisiensi (Cost Avoidance)} = 2.273.752 \times \text{Rp } 3.000 = \mathbf{\text{Rp } 6.821.256.000 \text{ / Tahun}}$$
* **Kalkulasi Net Benefit & Payback Period:**
  * Biaya Pengembangan (CAPEX): `Rp 0` *(100% In-house Peruri)*.
  * Biaya Lisensi Vendor (OPEX): `Rp 0`.
  * **Net Value Creation:** **~Rp 6,82 Miliar / Tahun**.
  * **Payback Period:** **Seketika (0 Bulan)**.

## 7.2 Dampak Non-Finansial (Mutu, People, ESG)
* **Mutu & Kepuasan Pelanggan (DJBC):** Menekan risiko lembar cacat lolos dan memastikan keandalan pasokan pita cukai nasional.
* **Kedisiplinan & Budaya Data (People Impact):**
  * Rekam jejak digital per PO 100% *auditable* menggantikan buku folio manual.
  * Evaluasi berbasis fakta objektif yang mengeliminasi friksi antar-shift.
  * `[VISUAL: Diagram Transformasi Kedisiplinan Sebelum vs Sesudah]` *(Asset: image26.png, image27.png)*
* **ESG / Keberlanjutan Lingkungan:**
  * Penyelamatan bahan baku kertas sekuriti sebanyak **2,27 Juta lembar limbah padat per tahun**.
  * Pengurangan emisi operasional dan pemakaian bahan kimia tinta.

## 7.3 Keselarasan Strategis & Potensi Replikasi
* **Dukungan Terhadap Skor INDI 4.0:** Mewujudkan pilar *Smart Factory*, *Traceability*, dan *Data-Driven Decision*.
* **Roadmap Replikasi Antar Unit:** Arsitektur sistem siap direplikasi ke lini **Khazanah, Meterai, Paspor, dan Uang Kertas**.

---

# BAB 9: SUSTAINABILITY (KEBERLANJUTAN SISTEM)

## 9.1 Standardisasi Dokumen & Prosedur Resmi (SOP / IK)
> **Tujuan:** Mengunci cara kerja baru agar menjadi standar baku institusi.

* **Penerbitan & Registrasi Dokumen Baru:**
  * *IK Pengisian Konfirmasi PO Cetak Harian* (No. Dokumen: `IK-PPC-2026-XXX`).
  * *SOP Pemeliharaan Mesin Terfokus Berbasis Analisis Pareto SIRINE*.
* **Penutupan Resmi Sistem Lama:** Penghentian total formulir fisik dan buku folio rekap per 1 Januari 2026.

## 9.2 Transfer Knowledge & Audit Keberlanjutan
* **Matriks Pelatihan Pengguna:**
  * Sosialisasi Entry Data: Seluruh Operator & PIC Kelompok.
  * Training Pengambilan Keputusan Dashboard: Kepala Unit & Kepala Seksi.
* **Fitur *In-App Guidance*:** Panduan interaktif langsung di dalam aplikasi SIRINE tanpa perlu dokumen cetak eksternal.
* **Mekanisme Audit Periodik:** Audit integritas input data mingguan oleh Supervisor.

---

# BAB 10 - BAB 11: LESSON LEARNED DAN KESIMPULAN

## 10.1 Lesson Learned & Strategi Mitigasi
* **Pelajaran 1:** Digitalisasi lapangan harus mengutamakan kemudahan pengguna (*User Experience First*) agar adopsi berjalan mulus.
* **Pelajaran 2:** Perubahan budaya membutuhkan masa adaptasi (*Inkubasi Q1* menghasilkan lompatan di *Q2*).
* **Pelajaran 3:** Data adalah *enabler*, kunci keberhasilan ada pada keberanian eksekusi tindakan korektif manajemen di lapangan.

## 10.2 Rekomendasi Rencana Pengembangan Lanjutan
* **Prioritas Tinggi (Short-Term):** *Rapor Kinerja Operator/Tim* (Sistem scoring komposit kuantitas LK, % inschiet, dan konsistensi input $\rightarrow$ Grade A–E).
* **Prioritas Sedang (Medium-Term):** Integrasi otomatis dengan *Maintenance Log Book* teknisi pemeliharaan.
* **Prioritas Replikasi (Long-Term):** Penerapan arsitektur ke Unit Produksi Meterai & Paspor.

## 10.3 Kesimpulan Akhir (Executive Closing Statement)
* DSS SIRINE 4.0 sukses mentransformasi manajemen Unit Cetak Pita Cukai menjadi entitas berbasis presisi data.
* Mampu menjawab tuntas dilema *Machine vs Operational Condition*, mereduksi inschiet dari **4,61% menjadi 3,33%**, dan mengamankan penghematan biaya produksi sebesar **Rp 6,82 Miliar per tahun**.
