# STRUKTUR LENGKAP DOKUMEN INOVASI & KAIZEN IAKA 2026
## DSS SIRINE 4.0: Decision Support System Terintegrasi Berbasis Granularitas Data Mesin & Kondisi Operasional untuk Mereduksi Inschiet Cetak Pita Cukai

---

## 📌 RINGKASAN EKSEKUTIF (EXECUTIVE SUMMARY / THE PITCH DECK SNAPSHOT)
> **Pitch Takeaway:** Transformasi operasional unit cetak pita cukai dari sistem pencatatan manual berbasis buku folio menjadi Decision Support System (DSS) berbasis data presisi real-time yang memangkas inschiet dari **4,61% ke 3,33%** dan mengamankan efisiensi biaya sebesar **Rp 6,82 Miliar/tahun** dengan payback period seketika (0 bulan).

* **Identitas Proyek Inovasi:**
  * **Judul Inovasi:** DSS SIRINE 4.0 (Decision Support System Unit Cetak Pita Cukai)
  * **Kategori:** Kaizen / Inovasi Proses & Digitalisasi Operasional Pabrik
  * **Unit Kerja:** Unit Cetak Pita Cukai – Perum Peruri
  * **Fasilitator:** [Nama & Jabatan minimal Kepala Departemen]
* **Highlight Hero Metrics:**
  * **Baseline Inschiet (2025):** `4,61%` (Puncak Q4: `5,11%` | Volume Order: `177.636.930 Lembar Cetak`)
  * **Realisasi Akhir (Q2 2026):** `3,33%` (**Penurunan: -1,28 pp / -27,8%**)
  * **Net Financial Impact:** **Efisiensi ~Rp 6,82 Miliar / Tahun** (Cost Avoidance Tambah Cetak)
  * **Payback Period:** **0 Bulan (Seketika)** – *100% In-house Development (Zero License Fee)*
  * **ESG Impact:** Reduksi limbah padat kertas sekuriti sebanyak **2.273.752 lembar / tahun**

---

# BAB 1: LATAR BELAKANG DAN MASALAH

## 1.1 Kondisi Eksisting & Urgensi Operasional Unit Cetak
> **Tujuan:** Membangun konteks operasional pabrik dan urgensi perlindungan produk sekuriti negara.
* Profil operasional Unit Cetak Pita Cukai (6 mesin cetak: Komori 1–4, Ryobi 1–2, 3 shift kerja 24 jam).
* Sifat kritis produk: Pita Cukai Hasil Tembakau (PCHT) & Minuman Mengandung Etil Alkohol (MMEA) dengan standar sekuriti tinggi dan SLA ketat DJBC.
* Keterbatasan eksisting: Kuantitas dicatat manual di buku folio, sementara data kualitas dari SAP/Verifikasi hanya agregat global tanpa atribusi mesin & shift.

## 1.2 Data Awal Pemicu Inovasi & Baseline Inschiet 2025
> **Tujuan:** Menyajikan data awal terverifikasi (angka, satuan, periode, sumber data).
* Total Volume Produksi PCHT 2025: `177.636.930 Lembar Cetak` (Sumber: SAP Production Order & PPIC 2025).
* Data Historis Baseline Inschiet 2025 (Sumber: Verifikasi Mutu Pita Cukai & SAP):
  * Kuartal 1 2025: `4,72%`
  * Kuartal 2 2025: `3,97%`
  * Kuartal 3 2025: `4,64%`
  * Kuartal 4 2025: `5,11%` (Puncak lonjakan desain baru)
  * **Rata-rata Baseline Inschiet 2025: 4,61%**
* **Slot Visual:** `[VISUAL 1.1: Bar Chart Inschiet Cetak per Kuartal 2025 vs Garis Rata-rata 4,61%]` *(Asset: extracted_images/image1.png / image2.png)*

## 1.3 Identifikasi Masalah Utama (The Blind Spot Pasca-SIRINE 3.5 (2024))
> **Tujuan:** Mendefinisikan masalah operasional spesifik yang belum terjawab.
* Keberhasilan SIRINE 3.5 (2024): Memetakan breakdown jenis kerusakan (inschiet turun ke 4,06% di akhir 2024).
* Munculnya Titik Buta 2025:
  * Data jenis kerusakan ada, namun tidak diketahui **mesin mana** yang menjadi penyumbang utama.
  * Tidak diketahui apakah inschiet dipicu oleh **kondisi fisik mesin** atau **kondisi operasional tim/shift**.
  * Akibatnya: *Maintenance* dilakukan bergilir ke semua mesin secara acak, memperpanjang *downtime*, dan pemborosan biaya komponen.

## 1.4 Skala Dampak Finansial & Risiko Pembiaran (Cost of Inaction)
> **Tujuan:** Mengonversi persentase inschiet ke angka rupiah nyata bila kondisi dibiarkan.
* Asumsi Biaya Tambah Cetak: `Rp 3.000 / lembar cetak` (Kertas sekuriti, tinta khusus, jam kerja, depresiasi mesin).
* Kertas Kerja Kerugian Eksisting (Baseline 4,61%):
  $$\text{Lembar Rusak Tahunan} = 177.636.930 \times 4,61\% = 8.189.062 \text{ lembar}$$
  $$\text{Nilai Kerugian Inschiet} = 8.189.062 \times \text{Rp } 3.000 = \mathbf{\text{Rp } 24,56 \text{ Miliar / tahun}}$$
* Nilai Penghematan Tiap 1% Penurunan Inschiet = `1.776.369 lembar` $\times$ Rp 3.000 = **Rp 5,329 Miliar / tahun**.
* **Slot Visual:** `[VISUAL 1.2: Diagram Skema Alur Dampak Finansial Kerugian vs Potensi Penghematan per 1%]` *(Asset: extracted_images/image3.png)*
* Dampak bila dibiarkan: Akumulasi biaya jutaan lembar tambah cetak, risiko penalti/komplain DJBC, dan evaluasi kerja operator yang bias.

---

# BAB 2: ANALISIS PENYEBAB (ROOT CAUSE ANALYSIS)

## 2.1 Metode Analisis Diagram Tulang Ikan (Fishbone 4M)
> **Tujuan:** Menunjukkan dekonstruksi faktor penyebab masalah inschiet secara komprehensif.
* Pemilihan metode Fishbone Diagram untuk membedah interaksi kompleks operasional pabrik cetak.
* **Slot Visual:** `[VISUAL 2.1: Diagram Fishbone 4M Faktor Inschiet Cetak Pita Cukai]` *(Asset: extracted_images/image4.png)*

## 2.2 Dekonstruksi Variabel Penyebab (Man, Machine, Method, Material)
> **Tujuan:** Menjelaskan detail permasalahan pada setiap cabang tulang ikan.
* **Man (Faktor Manusia/Operasional):** Disparitas kelelahan dan kewaspadaan operator antar shift (terutama shift malam); pemahaman SOP penanganan troubleshooting belum seragam.
* **Machine (Kondisi Mesin Cetak):** Penurunan performa komponen mekanis seiring umur mesin; jadwal *preventive maintenance* belum sinkron dengan data kerusakan aktual mesin terkait.
* **Method (Metode Kerja & Prosedur):** Standarisasi setting awal parameter mesin belum terdokumentasi rapi; alur pelaporan kendala masih manual/lisan; belum ada basis data riwayat error.
* **Material (Bahan Baku & Lingkungan):** Sensitivitas kertas sekuriti terhadap fluktuasi suhu/kelembaban ruang simpan (memicu plooi, zig-zag); variasi lot bahan baku dari supplier.

## 2.3 Temuan Fakta Lapangan & Bukti "Data Silo"
> **Tujuan:** Menampilkan bukti empiris pemisahan data yang menjadi penghalang diagnosa supervisor.
* Data SAP (Production Order): Format mentah CSV sulit dianalisis cepat oleh operator di lapangan (*Asset: image10.png*).
* Data Verifikasi (HCTS): Hanya mencatat agregat cacat tanpa rekam jejak mesin dan shift pencetak.
* Data Lapangan: Tercatat di buku folio fisik yang rentan hilang dan tidak dapat diagregasi secara analitis.

## 2.4 Penetapan Akar Masalah Utama (Core Root Cause)
> **Tujuan:** Merumuskan *single root cause* yang menjadi target intervensi solusi.
* **Akar Masalah Utama:** *Ketiadaan sistem diagnostik terpadu yang menghubungkan data jenis kerusakan dengan data penugasan operasional (mesin, shift, operator, dan nomor PO) secara real-time.*

---

# BAB 3: GAGASAN & MEKANISME SOLUSI (THE PROPOSED SOLUTION)

## 3.1 Konsep Solusi & Arsitektur Sistem Dua Lapisan (Two-Tier Architecture)
> **Tujuan:** Menjelaskan konsep solusi terstruktur dalam mentransformasi data menjadi keputusan preskriptif.
* Evolusi dari SIRINE 3.5 (2024) (Menjawab: *Jenis kerusakan apa?*) menuju DSS SIRINE 4.0 (Menjawab: *Mesin mana? Kondisi operasional mana? Tindakan apa?*).
* **Slot Visual:** `[VISUAL 3.1: Diagram Evolusi Konsep SIRINE 3.5 (2024) vs DSS SIRINE 2026]` *(Asset: extracted_images/image5.png)*
* Arsitektur Dua Lapisan:
  * **Lapisan 1 (Pengumpulan Data Digital):** Form Konfirmasi PO Cetak + Jadwal & Template Gilir Operator.
  * **Lapisan 2 (Analisis & Visualisasi Preskriptif):** Engine pengolah data SAP + HCTS menjadi dashboard aksi supervisor dan monitoring lapangan.
* **Slot Visual:** `[VISUAL 3.2: Diagram Arsitektur Dua Lapisan DSS SIRINE 4.0]` *(Asset: extracted_images/image6.png)*

## 3.2 Breakdown 6 Modul Fitur Unggulan DSS SIRINE 4.0
> **Tujuan:** Menjelaskan fungsi dan mekanisme kerja dari setiap modul aplikasi secara mendalam.
* **Fitur 1 – Form Entry Konfirmasi PO Cetak:** Input digital per PO dengan *autofill* spesifikasi produk dari SAP dan nama operator dari jadwal mingguan (*Asset: image7.png*).
* **Fitur 2 – Jadwal Operator & Template Tim:** Pengaturan grid mingguan mesin $\times$ shift dengan fitur rotasi otomatis dan kustomisasi per sel (*Asset: image8.png, image9.png*).
* **Fitur 3 – Dashboard Produksi Mesin Cetak:** Transformasi data mentah SAP menjadi grafik kuantitas (LK) dan persentase inschiet per unit mesin (*Asset: image11.png – image15.png*).
* **Fitur 4 – Dashboard Produksi Unit Cetak:** Analisis komparatif kuantitas dan % rusak per kondisi operasional tim/shift dengan hak akses berjenjang (*traceability*).
* **Fitur 5 – Modul Audit Jenis Kerusakan Tiap Mesin:** Diagram Pareto kerusakan spesifik mesin (Noda 42,34%, Zig-zag 20,18%, Blobor 13,54%) untuk panduan teknisi maintenance (*Asset: image16.png, image17.png*).
* **Fitur 6 – Floor-Level Real-Time Andon Display:** Layar informasi real-time di area kerja cetak (auto-refresh 60 detik) untuk monitoring langsung progress order dan peringatan jatuh tempo (*Asset: image18.png – image21.png*).

## 3.3 Mekanisme Hubungan Sebab-Akibat (Menyerang Akar Masalah Bab 2)
> **Tujuan:** Membuktikan bagaimana fitur-fitur solusi secara presisi melenyapkan 4 cabang penyebab Fishbone.
* Mengatasi **Man & Method**: Visibilitas data per tim/shift memungkinkan coaching yang objektif dan standardisasi SOP serah terima gilir.
* Mengatasi **Machine**: Teknisi maintenance menerima instruksi servis berbasis data Pareto kerusakan mesin spesifik sebelum membongkar mesin.
* Mengatasi **Material**: Deteksi dini lonjakan cacat bahan baku (*plooi/zig-zag*) per nomor PO untuk eskalasi ke bagian QC dan gudang.

---

# BAB 4: KEUNGGULAN, KEBARUAN & ALUR PROSES KERJA

## 4.1 Unsur Kebaruan & Matriks Kapabilitas
> **Tujuan:** Membuktikan diferensiasi dan lompatan kapabilitas dibanding cara lama dan praktik unit lain.
* **Tabel Matriks Kapabilitas Komparatif:**
  | Parameter Kapabilitas | Cara Lama (Pra-2024) | SIRINE 3.5 (2024) | DSS SIRINE 4.0 (2026) |
  | :--- | :---: | :---: | :---: |
  | Identifikasi Cacat Dominan Unit | Manual / Lisan | ✅ Agregat Unit | ✅ Granular |
  | Pemetaan Mesin Inschiet Tertinggi | ❌ Tidak Ada | ❌ Tidak Ada | ✅ **Real-Time per Mesin** |
  | Pareto Cacat Spesifik per Mesin | ❌ Tidak Ada | ❌ Tidak Ada | ✅ **Detail per Komponen** |
  | Pelacakan Volume (LK) per Tim & Shift | Buku Folio | ❌ Tidak Ada | ✅ **Digital & Tervalidasi** |
  | Diagnosa: Kendala Mesin vs Tim/Shift | ❌ Dugaan / Asumsi | ❌ Tidak Ada | ✅ **Terbukti Terpisah** |
  | Rekam Jejak Transaksi per Lembar PO | ❌ Hilang | ❌ Tidak Ada | ✅ **Full Audit Traceability** |

## 4.2 Alur Proses Kerja Sebelum vs Sesudah Implementasi
> **Tujuan:** Menggambarkan perubahan alur kerja operasional dan kecepatan pengambilan keputusan.
* **Slot Visual Before:** `[VISUAL 4.1: Flowchart Alur Kerja Sebelum Implementasi SIRINE 4.0]` *(Asset: extracted_images/image22.png)*
* **Slot Visual After:** `[VISUAL 4.2: Flowchart Alur Kerja Preskriptif Sesudah DSS SIRINE 4.0]` *(Asset: extracted_images/image23.png)*

## 4.3 Standar & SOP yang Ditingkatkan (Kaizen Framework)
> **Tujuan:** Menunjukkan penguatan tata kelola dan eliminasi proses kerja manual yang tidak bernilai tambah.
* Eliminasi proses rekap manual buku folio yang memakan waktu $\pm 45$ menit per hari.
* Standardisasi integrasi data: PO selesai $\rightarrow$ Konfirmasi Digital $\rightarrow$ Agregasi Otomatis Dashboard.

## 4.4 Target Perbaikan Kuantitatif & Estimasi Dampak MVP
> **Tujuan:** Menetapkan target terukur fase awal sebagai acuan evaluasi keberhasilan.
* Target Penurunan Inschiet Fase 1: Dari baseline `4,61%` menjadi `< 4,00%` (-0,61 pp).
* Target Efisiensi Waktu Troubleshooting: Mengurangi waktu diagnosa kerusakan mesin sebesar $\ge 50\%$.

---

# BAB 5: RENCANA & DESAIN UJI COBA (MVP EXECUTION PLAN)

## 5.1 Ruang Lingkup Pengujian (Lini Mesin, Shift, Periode)
> **Tujuan:** Menetapkan batas-batas uji coba Minimum Viable Product (MVP) secara terukur.
* Lokasi Uji Coba: Lini Cetak Pita Cukai, Gedung Produksi Perum Peruri Karawang.
* Unit Mesin yang Diuji: 6 Mesin Utama (Komori 1, Komori 2, Komori 3, Komori 4, Ryobi 1, Ryobi 2).
* Waktu Operasional: 3 Shift Kerja (Pagi: 07.00–15.00, Sore: 15.00–23.00, Malam: 23.00–07.00).

## 5.2 Struktur Tim Uji Coba, Peran PIC & Calon Fasilitator
> **Tujuan:** Memenuhi syarat fasilitator minimal Kepala Departemen dan mendefinisikan akuntabilitas peran.
* **Calon Fasilitator:** Kepala Departemen Khazanah dan Verifikasi Strategic Business Unit High Security Solution / Kepala Seksi Cetak Pita Cukai.
* **Struktur Pelaksana Lapangan:**
  * PIC Kelompok: Operator bertugas yang menginput data konfirmasi PO harian.
  * Kepala Kelompok: Verifikator kelengkapan input dan validitas data per shift.
  * Kepala Unit Cetak: Reviewer dashboard analitis dan eksekutor arahan harian.

## 5.3 Alokasi Sumber Daya & Desain Minimum Viable Product (MVP)
> **Tujuan:** Menunjukkan efisiensi sumber daya dan arsitektur pengujian yang *lean*.
* Sumber Daya Perangkat: PC/Tablet terminal input yang sudah tersedia di lini produksi.
* Infrastruktur Server: Web server internal Perum Peruri (tanpa biaya sewa cloud eksternal).

## 5.4 Jadwal & Roadmap Pelaksanaan (Gantt Chart Okt 2025 – Jun 2026)
> **Tujuan:** Menyajikan jadwal pelaksanaan bertahap dari deploy hingga evaluasi akhir.
* Tahap 1: Persiapan & Deploy Sistem (Okt – Des 2025).
* Tahap 2: Masa Adaptasi & Pendampingan Input (Jan – Mar 2026).
* Tahap 3: Tindak Lanjut Maintenance Presisi & Coaching (Apr – Jun 2026).
* **Slot Visual:** `[VISUAL 5.1: Gantt Chart Roadmap Implementasi DSS SIRINE 2026]` *(Asset: extracted_images/image24.png)*

---

# BAB 6: PELAKSANAAN IMPLEMENTASI, KENDALA & VALIDASI HASIL

## 6.1 Catatan Pelaksanaan Lapangan & Log Aktivitas Bertanggal
> **Tujuan:** Membuktikan bahwa solusi benar-benar dijalankan di lapangan dengan data mentah yang dapat diolah.
* Sosialisasi dan go-live fitur Konfirmasi PO Cetak kepada seluruh PIC kelompok.
* Pendampingan intensif pengisian data pada minggu-minggu pertama penerapan.
* Pemanfaatan dashboard mingguan oleh Kepala Unit Cetak dalam *daily production briefing*.

## 6.2 Kendala Operasional Lapangan & Tindakan Problem Solving
> **Tujuan:** Menunjukkan ketangguhan tim dalam memitigasi hambatan teknis dan kultural.
* **Kendala 1 (Resistensi Operator):** Operator merasa input data adalah beban tambahan di sela kerja fisik.
  * *Problem Solving:* Implementasi fitur *autofill* spesifikasi produk dari SAP dan *shortcut* simpan cepat (Ctrl+S), memangkas waktu input menjadi < 30 detik.
* **Kendala 2 (Inkonsistensi Data Entry Awal Q1):** Beberapa PO terlambat diinput sehingga data dashboard tertunda.
  * *Problem Solving:* Menjadikan verifikasi kelengkapan data input sebagai syarat resmi serah terima shift (*handover checklist*).

## 6.3 Data Hasil Validasi Before vs After (Tervalidasi & Jumlah Sampel n)
> **Tujuan:** Menyajikan tabel Before vs After lengkap dengan sampel ($n$), selisih poin, dan grafik tren.
* **Tabel Validasi Kinerja Inschiet:**
  | Periode | Status / Fase | Volume Produksi ($n$) | Inschiet (%) | $\Delta$ vs Baseline (pp) | % Perubahan |
  | :--- | :--- | :---: | :---: | :---: | :---: |
  | **2025 (Baseline)** | Kondisi Eksisting | 177.636.930 lb | **4,61%** | — | — |
  | **Q1 2026** | Masa Adaptasi Data | $\pm 44,4$ Juta lb | **4,34%** | -0,27 pp | -5,9% |
  | **Q2 2026** | Full Data-Driven Action | $\pm 44,4$ Juta lb | **3,33%** | **-1,28 pp** | **-27,8%** |
* **Slot Visual:** `[VISUAL 6.1: Bar Chart Tren Penurunan Inschiet 2025 s.d. Q2 2026]` *(Asset: extracted_images/image25.png)*

## 6.4 Evaluasi Realisasi terhadap Target Fase 1
> **Tujuan:** Menunjukkan bahwa realisasi melampaui target awal yang ditetapkan.
* Target Fase 1: Inschiet `< 4,00%` (-0,61 pp).
* Realisasi Q2 2026: Inschiet mencapai `3,33%` (-1,28 pp), melampaui target sebesar **210% dari target penurunan**.

---

# BAB 7: DAMPAK FINANSIAL & KERTAS KERJA TERBUKA (BUSINESS IMPACT)

## 7.1 Kertas Kerja Dampak Finansial Terbuka (Open Financial Model & Formula)
> **Tujuan:** Menyajikan kertas kerja finansial terbuka yang rumusnya dapat diverifikasi langsung oleh juri.
* Formula Perhitungan Cost Avoidance / Penghematan Tahunan:
  $$\text{Volume Tahunan (Order PCHT 2025)} = 177.636.930 \text{ Lembar Cetak}$$
  $$\text{Baseline Inschiet 2025} = 4,61\% \rightarrow \text{Lembar Rusak Eksisting} = 8.189.062 \text{ lembar}$$
  $$\text{Realisasi Inschiet Q2 2026} = 3,33\% \rightarrow \text{Proyeksi Lembar Rusak Baru} = 5.915.310 \text{ lembar}$$
  $$\text{Total Reduksi Lembar Rusak} = 8.189.062 - 5.915.310 = \mathbf{2.273.752 \text{ Lembar / Tahun}}$$
  $$\text{Estimasi Biaya Tambah Cetak} = \text{Rp } 3.000 / \text{lembar}$$

## 7.2 Perhitungan Cost Avoidance & Efisiensi Biaya Tambah Cetak
> **Tujuan:** Menghitung nilai bersih penghematan biaya produksi tahunan.
* Kalkulasi Total Penghematan Finansial:
  $$\text{Financial Value (Cost Avoidance)} = 2.273.752 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 6.821.256.000 \text{ / Tahun}}$$
* **Ringkasan Nilai Penghematan:** Efisiensi sebesar **~Rp 6,82 Miliar per tahun** berhasil diamankan bagi perusahaan.

## 7.3 Analisis Investasi Bersih (Net Value) & Payback Period (In-House Advantage)
> **Tujuan:** Membuktikan efisiensi biaya investasi pengembangan sistem.
* Biaya Investasi Pengembangan (CAPEX): `Rp 0` (Dikembangkan 100% *in-house* oleh staf internal Peruri).
* Biaya Lisensi Perangkat Lunak (OPEX): `Rp 0` (Memanfaatkan infrastruktur server internal).
* **Net Value Creation:** **Rp 6.821.256.000 / Tahun**.
* **Payback Period:** **0 Bulan (Immediate / Seketika)**.

---

# BAB 8: DAMPAK NON-FINANSIAL (MUTU, PEOPLE, CUSTOMER, ESG IMPACT)

## 8.1 Dampak Mutu & Kepuasan Pelanggan (DJBC Impact)
> **Tujuan:** Menguraikan peningkatan kualitas produk sekuriti dan keandalan pasokan.
* Mereduksi risiko lolosnya lembar cacat mutu (*HCTS*) ke tahap khazanah dan verifikasi.
* Menjamin pemenuhan pesanan pita cukai tepat waktu sesuai pesanan pabrik rokok dan Bea Cukai.

## 8.2 Dampak Budaya Kerja & Kedisiplinan Karyawan (People & Traceability)
> **Tujuan:** Menjelaskan transformasi budaya kerja berbasis data dan keadilan evaluasi kerja.
* Transformasi dari catatan buku folio yang rawan hilang menjadi rekam jejak digital yang 100% *auditable*.
* Terciptanya transparansi performa kerja: Evaluasi dan *coaching* dilakukan secara objektif berbasis data performa per tim, bukan asumsi subjektif.
* **Slot Visual:** `[VISUAL 8.1: Diagram Alur Transformasi Kedisiplinan Sebelum vs Sesudah]` *(Asset: extracted_images/image26.png, image27.png)*

## 8.3 Dampak Lingkungan & Keberlanjutan (ESG / Waste Reduction)
> **Tujuan:** Menghitung kontribusi nyata terhadap kelestarian lingkungan dan pengurangan limbah.
* Pengurangan limbah padat kertas sekuriti sebanyak **2.273.752 lembar per tahun** (setara dengan $\pm 18$ Ton kertas sekuriti).
* Penghematan konsumsi bahan kimia tinta cetak dan energi listrik mesin produksi.

## 8.4 Keselarasan dengan Strategi Perusahaan & Skor INDI 4.0
> **Tujuan:** Menghubungkan capaian inovasi dengan indikator transformasi digital nasional BUMN.
* Selaras dengan target peningkatan skor INDI 4.0 Perum Peruri pada pilar *Smart Operation*, *Real-time Data Integration*, dan *Workforce Digital Empowerment*.

---

# BAB 9: STANDARISASI & KEBERLANJUTAN SISTEM (SUSTAINABILITY & INSTITUTIONALIZATION)

## 9.1 Pengesahan & Registrasi Dokumen Standar Baru (SOP & IK)
> **Tujuan:** Mengunci metode kerja baru agar terikat secara legal dalam tata kelola operasional perusahaan.
* Penerbitan Instruksi Kerja (IK) Baru: *IK Pengisian Konfirmasi PO Cetak Digital* (No. Dokumen: `IK-PPC-2026-001`).
* Pembaruan Standar Operasional: *SOP Tindakan Perbaikan Mesin Berbasis Pareto SIRINE* (No. Dokumen: `SOP-PPC-2026-004`).

## 9.2 Berita Acara Penutupan Resmi Sistem Lama (Buku Folio Manual)
> **Tujuan:** Memastikan sistem lama tidak lagi digunakan (*no duplicate work*).
* Penarikan seluruh buku folio pencatatan fisik dan penerbitan instruksi kerja peralihan 100% digital per 1 Januari 2026.

## 9.3 Matriks Program Transfer Knowledge & Pelatihan Mandiri
> **Tujuan:** Membuktikan kesiapan pengguna lapangan dalam mengoperasikan sistem secara mandiri.
* **Matriks Pelaksanaan Transfer Knowledge:**
  * Pelatihan Form Entry & Jadwal Shift: Seluruh PIC & Kepala Kelompok (3 shift).
  * Sosialisasi Dashboard Analisis & Intervensi: Kepala Unit Cetak & Kepala Seksi Produksi.
* Ketersediaan modul *In-App Guidance* interaktif di dalam aplikasi SIRINE tanpa ketergantungan dokumen fisik.

## 9.4 Mekanisme Audit Keberlanjutan & Kontrol Periodik
> **Tujuan:** Menjaga integritas data secara berkesinambungan.
* Audit kelengkapan data harian oleh Kepala Kelompok pada setiap akhir shift.
* Audit mingguan konsistensi data SAP vs SIRINE oleh Supervisor Unit Cetak.

---

# BAB 10: TANTANGAN, MITIGASI & PEMBELAJARAN (LESSON LEARNED)

## 10.1 Tantangan Utama Selama Siklus Proyek Inovasi
> **Tujuan:** Menyampaikan rintangan nyata yang dihadapi selama implementasi.
* **Tantangan Kultural:** Kebiasaan mencatat manual yang telah berlangsung bertahun-tahun dan kekhawatiran data digunakan untuk menghakimi operator.
* **Tantangan Waktu Adaptasi (Lag Effect):** Hasil penurunan inschiet pada kuartal pertama (Q1) belum signifikan (-5,9%) karena data belum sepenuhnya matang.

## 10.2 Strategi Mitigasi Terhadap Aspek Teknis & Kultural
> **Tujuan:** Menjelaskan strategi cerdas yang diambil untuk menyelesaikan tantangan.
* Pendekatan *User-Centric UX*: Menyederhanakan formulir input dengan *autofill* cerdas agar sistem mempermudah kerja operator, bukan menambah beban.
* Sosialisasi Transparansi: Menegaskan bahwa data digunakan untuk *support & coaching* (pendampingan), bukan mencari kesalahan individu.

## 10.3 Key Takeaways & Kaizen Wisdom
> **Tujuan:** Merangkum prinsip-prinsip pembelajaran penting bagi replikasi di unit lain.
* *Data is an Enabler, Action Creates Value:* Nilai tertinggi sistem bukan pada tampilan dashboard, melainkan pada ketepatan tindakan korektif yang diambil supervisor.
* *Granular Data Unlocks Root Causes:* Setiap level granularitas data baru akan membuka lapisan masalah yang lebih dalam dan solusi yang lebih tepat sasaran.

---

# BAB 11: KESIMPULAN & RENCANA PENGEMBANGAN LANJUTAN (ROADMAP)

## 11.1 Kesimpulan Eksekutif Proyek
> **Tujuan:** Memberikan pernyataan penutup yang kuat, ringkas, dan meyakinkan dewan juri.
* DSS SIRINE 4.0 sukses menutup titik buta operasional Unit Cetak Pita Cukai dengan menghubungkan data kerusakan secara presisi ke mesin dan kondisi operasional.
* Berhasil mereduksi inschiet dari **4,61% menjadi 3,33%** (turun 1,28 pp / -27,8%), menghasilkan potensi penghematan tahunan sebesar **Rp 6,82 Miliar** dengan nol biaya investasi lisensi.

## 11.2 Roadmap Jangka Pendek: Rapor Scoring Kinerja Operator (Grade A–E)
> **Tujuan:** Menjelaskan rencana peningkatan terdekat berbasis data yang sudah terkumpul.
* Pengembangan modul evaluasi komposit berkala berbasis parameter: kuantitas lembar cetak (LK), persentase kerusakan, dan kedisiplinan input $\rightarrow$ menghasilkan pemeringkatan objektif Grade A–E untuk dasar program *reward & coaching*.

## 11.3 Roadmap Jangka Menengah: Integrasi Maintenance Log Book
> **Tujuan:** Menutup siklus data antara deteksi kerusakan dan histori perbaikan fisik mesin.
* Menghubungkan dashboard SIRINE dengan sistem pencatatan servis teknisi untuk memvalidasi efektivitas setiap tindakan perbaikan mesin secara otomatis.

## 11.4 Potensi Replikasi Skala Penuh ke Unit Dokumen Sekuriti Lainnya
> **Tujuan:** Menunjukkan nilai strategis jangka panjang bagi Perum Peruri.
* Replikasi arsitektur sistem (Konfirmasi PO + Jadwal Digital + Dashboard Granular) ke unit produksi dokumen sekuriti lainnya: **Khazanah, Meterai, Paspor, dan Uang Kertas**.
