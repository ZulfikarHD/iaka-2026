# RISALAH LATAR BELAKANG DAN IDENTIFIKASI MASALAH
### *Transformasi Tata Kelola Pengendalian Mutu Unit Cetak Pita Cukai: Menjawab Tuntutan Pasar Global, Komitmen Tender Nasional, dan Sasaran Strategis Peruri melalui Integrasi Data Meja Mesin*

---

> ***Executive Takeaway:***  
> Menjawab dinamika pasar percetakan sekuriti global dan pemenuhan klausul tender pengadaan pita cukai nasional dari Direktorat Jenderal Bea dan Cukai (DJBC) Kementerian Keuangan RI, Perum Peruri memprioritaskan efisiensi biaya manufaktur dan keandalan mutu produk sekuriti negara. Seluruh sasaran strategis korporasi tersebut bermuara pada lini produksi berkecepatan tinggi di Unit Cetak Pita Cukai yang mengelola volume pesanan aktual sebesar **177.636.930 Lembar Cetak pada tahun 2025** (standar rata-rata **160.000.000 Lembar Cetak / tahun**). Sepanjang tahun 2025, rata-rata *inschiet* (tingkat kerusakan cetak) berfluktuasi pada level **4,61%** (dengan puncak Kuartal 4 mencapai **5,11%**), yang merepresentasikan potensi pemborosan biaya cetak sebesar **Rp 22,13 Miliar hingga Rp 24,56 Miliar / tahun**. Kendala utama yang dihadapi di lapangan adalah **pemisahan data (*data silo*)**: pencatatan kuantitas manual pada buku folio di meja mesin terisolasi dari data kualitas di sistem SAP `ZPPRSIPPC0012` yang hanya menyajikan ringkasan kerusakan global di tingkat unit. Ketiadaan data granular per mesin dan per pola gilir kerja (*shift*) ini memicu pemeriksaan teknis mesin secara spekulatif (*trial-and-error*) dengan waktu henti (*downtime*) **> 1 *shift* (> 8 jam) per mesin**, memperlambat evaluasi kinerja operator, serta mengancam ketepatan jadwal pengiriman (*Service Level Agreement*). Kondisi ini melahirkan urgensi implementasi **Decision Support System (DSS) SIRINE 4.0** untuk mengintegrasikan data lapangan secara seketika dan memangkas tingkat pemborosan cetak.

---

## 1. Lanskap Global: Dinamika Pasar & Standar Presisi Percetakan Sekuriti Tinggi (*High-Security Printing*)

Dalam era manufaktur modern, industri percetakan sekuriti tinggi (*high-security printing*) di tingkat global menghadapi tuntutan transformasi yang sangat ketat. Berdasarkan standar asosiasi percetakan sekuriti internasional seperti *Intergraf* dan panduan kepatuhan *World Customs Organization* (WCO), instrumen pengamanan fisik yang diterbitkan oleh negara wajib memiliki presisi mikroskopis yang sempurna guna menutup celah pemalsuan (*anti-counterfeiting*). Perkembangan teknologi pemalsuan yang semakin canggih memaksa industri manufaktur sekuriti menerapkan fitur pengamanan bertingkat (*multi-layer security features*), mulai dari substrat kertas berserat khusus (*security fibers*), tinta sekuriti berpendar ultra-violet (*UV-fluorescent security ink*), ornamen *guilloche*, *microtext*, hingga aplikasi *hologram foil* berpresisi tinggi.

Penerapan standar pengamanan tinggi tersebut secara langsung membentuk dinamika persaingan industri manufaktur sekuriti global pada dua pilar utama:
1. **Tuntutan Kualitas Tanpa Toleransi (*Zero-Defect Operations*):** Dalam produk dokumen sekuriti negara, cacat cetak fisik seperti tinta blobor, noda bintik, atau pergeseran posisi register antar-warna tidak hanya dianggap sebagai penurunan estetika, melainkan sebagai deviasi kritis yang dapat merusak autentikasi keaslian dokumen di mata publik dan aparat pengawas. Oleh karena itu, standar toleransi cacat di industri ini ditekan hingga mendekati titik nol (*near-zero defect*).
2. **Keterlacakan Digital & Efisiensi Berkelanjutan (*Lean & ESG Standards*):** Mengingat bahan baku kertas dan tinta sekuriti memiliki harga perolehan yang sangat mahal serta proses pengadaan yang diaudit secara internasional, industri manufaktur sekuriti global bergeser dari metode pengendalian mutu tradisional yang bersifat pasca-produksi (*post-mortem inspection*) menuju pemantauan proses langsung di area kerja secara seketika (*real-time process monitoring*). Setiap gram bahan baku dan lembar cetak yang terbuang (*waste/afval*) menjadi indikator inefisiensi yang membebani daya saing perusahaan.

Standar presisi, keterlacakan data, dan efisiensi manufaktur global inilah yang kemudian diadopsi dan diintegrasikan secara formal oleh Pemerintah Republik Indonesia ke dalam persyaratan pengadaan dokumen sekuriti negara.

---

## 2. Skala Tender Nasional: Kontrak Pengadaan & Integritas Fiskal DJBC Kemenkeu RI

Menjawab kebutuhan pengawasan penerimaan negara, Pemerintah Republik Indonesia melalui **Direktorat Jenderal Bea dan Cukai (DJBC) Kementerian Keuangan RI** menyelenggarakan proses pengadaan dokumen sekuriti negara berupa **Pita Cukai**, yang mencakup **Pita Cukai Hasil Tembakau (PCHT)** dan **Minuman Mengandung Etil Alkohol (MMEA)**. Pita cukai bukan sekadar label cetak biasa, melainkan instrumen fiskal legal yang menjadi bukti fisik pelunasan penerimaan cukai negara yang menyumbang ratusan triliun rupiah ke dalam kas Anggaran Pendapatan dan Belanja Negara (APBN).

Keterlibatan produk pita cukai dalam penerimaan negara menetapkan klausul kontrak tender pengadaan yang sangat ketat bagi pihak percetakan:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│               KLAUSUL KUALITAS & KEPATUHAN TENDER PENGADAAN PITA CUKAI                 │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. SPESIFIKASI MUTU MUTLAK:                                                            │
│    • Seluruh fitur pengamanan fisik (kertas sekuriti, tinta UV, guilloche, & hologram) │
│      wajib tercetak sempurna tanpa deviasi warna, register, maupun kepekatan.          │
│    • Cacat mutu berisiko memicu kesalahan identifikasi keaslian di pasar nasional.     │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 2. REKONSILIASI KETAT LEMBAR RUSAK (HCTS):                                             │
│    • Setiap lembar cetak yang mengalami kerusakan fisik wajib dikategorikan sebagai    │
│      Hasil Cetak Tidak Sempurna (HCTS) dan diaudit melalui proses pemusnahan resmi.    │
│    • Rasio lembar rusak (inschiet) yang tinggi meningkatkan beban verifikasi & audit.  │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 3. JAMINAN KETEPATAN SERVICE LEVEL AGREEMENT (SLA):                                    │
│    • Volume pesanan bernilai ratusan juta lembar wajib dikirimkan tepat waktu guna     │
│      menjamin kelancaran operasional industri tembakau dan penerimaan kas negara.      │
│    • Siklus cetak ulang (tambah cetak) yang panjang berisiko terkena sanksi penalti SLA.│
└────────────────────────────────────────────────────────────────────────────────────────┘
```

Skala pengadaan pita cukai nasional yang dikelola mencapai rata-rata **160.000.000 Lembar Cetak per tahun**, dengan realisasi pesanan aktual pada tahun anggaran 2025 menembus **177.636.930 Lembar Cetak**. Besarnya volume dan ketatnya parameter kepatuhan tender menuntut jaminan proses produksi yang stabil, akurat, dan bebas dari gangguan teknis yang berkepanjangan.

---

## 3. Arah Strategis & Mandat Korporasi Perum Peruri

Sebagai Badan Usaha Milik Negara (BUMN) yang ditunjuk oleh pemerintah berdasarkan **Peraturan Pemerintah Nomor 06 Tahun 2019**, **Perum Percetakan Uang Republik Indonesia (Peruri)** mengemban mandat tunggal untuk menyelenggarakan pencetakan Uang Rupiah serta dokumen sekuriti negara bernilai tinggi bagi Republik Indonesia. Dalam menjalankan amanah strategis tersebut, Perum Peruri menetapkan visi korporasi untuk menjadi perusahaan penjamin keaslian dan percetakan sekuriti terintegrasi terkemuka dengan keunggulan operasional berstandar dunia.

Untuk mempertahankan kepercayaan pemerintah dalam memenangkan tender pengadaan pita cukai secara berkelanjutan serta mengamankan profitabilitas perusahaan, Direksi dan Manajemen Perum Peruri menetapkan tiga sasaran strategis korporasi:
1. **Pengendalian Biaya Pokok Produksi (*Cost Leadership & Material Protection*):** Mengingat bahan baku kertas berpengaman khusus dan tinta sekuriti merupakan komponen berbiaya tinggi, manajemen mewajibkan seluruh lini operasi menekan rasio pemborosan bahan baku (*inschiet*) guna melindungi margin laba dan menjaga efisiensi anggaran korporasi.
2. **Pencapaian Keunggulan Operasional (*Operational Excellence & Zero Waste*):** Menyelaraskan proses manufaktur dengan standar manajemen mutu **ISO 9001:2015** dan prinsip *lean manufacturing* guna memastikan keandalan kapasitas produksi dalam memenuhi target kontrak tanpa menghasilkan penumpukan limbah padat kertas sekuriti.
3. **Peningkatan Maturitas Industri Cerdas (*Smart Factory & INDI 4.0*):** Mendorong digitalisasi area kerja di lini produksi, mentransformasikan pencatatan fisik manual menjadi aliran data digital terintegrasi yang memungkinkan pimpinan mengambil keputusan korektif berbasis data riil (*data-driven decision making*).

Seluruh arahan strategis, target efisiensi biaya, dan komitmen pemenuhan kontrak tender korporasi tersebut pada akhirnya bertumpu pada satu lini kerja utama dengan volume pekerjaan terbesar di perusahaan: **Unit Cetak Pita Cukai**.

---

## 4. Realitas Lapangan di Unit Cetak Pita Cukai: Dinamika Operasional & Titik Kritis

Unit Cetak Pita Cukai di bawah Departemen Khazanah dan Verifikasi Strategic Business Unit High Security Solution merupakan unit pelaksana teknis yang mengoperasikan lini pencetakan *sheet-fed offset*. Lini kerja ini beroperasi dengan intensitas tinggi selama **24 jam sehari secara non-stop** dengan menerapkan pola **3 gilir kerja (*shift*) bergilir** (*Shift* Pagi pukul 07.00–15.00 WIB, *Shift* Sore pukul 15.00–23.00 WIB, dan *Shift* Malam pukul 23.00–07.00 WIB), didukung oleh **9 unit mesin cetak *sheet-fed offset*** dan melibatkan sekitar **$\pm 42$ personel operator cetak dan kepala kelompok**.

Sembilan unit mesin cetak yang menjadi tulang punggung lini operasional terdiri dari:
* **4 Unit Mesin Komori:** `KMR 1`, `KMR 2`, `KMR 3`, dan `KMR 4`
* **2 Unit Mesin Ryobi:** `RYB 1` dan `RYB 2`
* **3 Unit Mesin GTO:** `GTO 1`, `GTO 2`, dan `GTO 3`

Tabel 1.1 merangkum parameter kapasitas operasional dan data baseline mutu cetak sepanjang tahun anggaran 2025 yang menjadi rujukan evaluasi di unit kerja.

*Tabel 1.1 Parameter Kapasitas dan Data Baseline Inschiet Unit Cetak Pita Cukai Tahun 2025*

| Parameter Operasional / Periode | Nilai / Angka | Satuan | Sumber Data Terverifikasi |
| :--- | :---: | :---: | :--- |
| **Jumlah Mesin Cetak Aktif** | **9 Mesin (4 Komori, 2 Ryobi, 3 GTO)** | Unit Mesin | Data Inventaris Aset Departemen Khazanah & Verifikasi |
| **Pola Gilir Kerja (*Shift*)** | **3 (Pagi, Sore, Malam)** | *Shift* / Hari | Standar Pola Penugasan Gilir Unit Cetak |
| **Durasi Operasional Lini** | **24** | Jam / Hari | *Standard Operating Procedure* (SOP) Unit Cetak |
| **Total Personel Operator Cetak** | **$\pm 42$** | Personel | Data Penugasan Kerja Seksi Cetak |
| **Rata-Rata Target Volume Tahunan** | **160.000.000** | Lembar Cetak | Perencanaan Kapasitas PPIC Peruri |
| **Total Volume Pesanan Aktual 2025** | **177.636.930** | Lembar Cetak | Modul *SAP Production Order* (`ZPPRSIPPC0012`) |
| **Inschiet Kuartal 1 (Q1 2025)** | **4,72%** | Persentase (%) | Rekap Verifikasi Mutu & Modul SAP |
| **Inschiet Kuartal 2 (Q2 2025)** | **3,97%** | Persentase (%) | Rekap Verifikasi Mutu & Modul SAP |
| **Inschiet Kuartal 3 (Q3 2025)** | **4,64%** | Persentase (%) | Rekap Verifikasi Mutu & Modul SAP |
| **Inschiet Kuartal 4 (Q4 2025)** | **5,11%** | Persentase (%) | Rekap Verifikasi Mutu & Modul SAP |
| **RATA-RATA BASELINE INSCHIET 2025** | **4,61%** | Persentase (%) | Konsolidasi Tahunan Verifikasi Mutu & SAP (`ZPPRSIPPC0012`) |
| **Durasi Pemeriksaan Mesin (*Trial Maintenance*)** | **> 1 *Shift* (> 8 Jam)** | Jam / Mesin | *Maintenance Log* & Rekap Kerusakan Mesin |

### 4.1 Analisis Fluktuasi Baseline 2025 & Pembuktian Kapabilitas
Berdasarkan data historis pada Tabel 1.1, rata-rata *inschiet* sepanjang tahun 2025 berada pada level **4,61%**. Pada **Kuartal 2 (Q2) 2025**, angka kerusakan sempat ditekan hingga mencapai **3,97%**. Pencapaian Q2 ini membuktikan bahwa lini cetak Peruri secara teknis memiliki kapabilitas manufaktur untuk beroperasi di bawah batas toleransi 4,00% apabila seluruh variabel operasional berada dalam kondisi terkontrol.

Namun, pada **Kuartal 4 (Q4) 2025**, terjadi lonjakan tajam tingkat kerusakan hingga menyentuh puncaknya pada level **5,11%** (+1,14 poin persentase dibandingkan Q2 2025). Lonjakan tajam ini bertepatan dengan masuknya volume pesanan pita cukai **desain baru dalam jumlah besar** menjelang penutupan tahun anggaran. Fenomena ini membuktikan bahwa ketika pesanan desain baru yang menuntut adaptasi setelan mesin masuk ke lini produksi, ketiadaan sistem diagnostik data di area mesin menyebabkan operator dan teknisi terlambat mendeteksi penyimpangan mutu, sehingga lonjakan volume pesanan berbanding lurus dengan pembengkakan jumlah lembar afval.

### 4.2 Kesenjangan Operasional Lapangan: Fenomena Pemisahan Aliran Data (*Data Silo*)
Meskipun lini produksi didukung oleh mesin-mesin cetak modern dan sistem ERP terpusat di kantor, tata kelola informasi operasional di lapangan masih terbelenggu oleh kondisi **pemisahan data (*data silo*)**:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                       STRUKTUR PEMISAHAN ALIRAN DATA OPERASIONAL                       │
├───────────────────────────────────────────┬────────────────────────────────────────────┤
│         SISI KUANTITAS DI LAPANGAN        │          SISI KUALITAS DI VERIFIKASI       │
├───────────────────────────────────────────┼────────────────────────────────────────────┤
│ • Dicatat manual pada BUKU FOLIO FISIK di │ • Lembar cetak disortir di Unit Verifikasi │
│   meja kontrol 9 mesin cetak.             │   dengan lead time pemeriksaan 1–2 hari.   │
│ • Data transaksi harian terisolasi dan    │ • Data diinput ke modul SAP ZPPRSIPPC0012  │
│   hanya menumpuk di meja mesin.           │   sebagai RINGKASAN KERUSAKAN GLOBAL       │
│ • Baru direkapitulasi secara manual oleh  │   di tingkat unit (unit-wide summary).     │
│   Kepala Kelompok saat evaluasi triwulan  │ • Data SAP terkunci di komputer kantor dan │
│   atau akhir masa kontrak pegawai.        │   TIDAK MENYEDIAKAN ATRIBUSI nomor mesin,  │
│ • Proses lambat & rawan kesalahan manusia.│   nomor PO, serta kelompok gilir pencetak. │
└───────────────────────────────────────────┴────────────────────────────────────────────┘
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                   IMPLIKASI TITIK BUTA DATA TERHADAP OPERASIONAL LAPANGAN              │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. PEMERIKSAAN TEKNIS SPEKULATIF (> 8 JAM / MESIN):                                    │
│    Saat verifikasi melaporkan kenaikan cacat blobor atau noda, teknisi tidak tahu      │
│    mesin mana yang menjadi pemicu utama. Teknisi terpaksa memeriksa seluruh 9 mesin    │
│    satu per satu secara trial-and-error, memboroskan jam henti mesin produktif.        │
│                                                                                        │
│ 2. BIAS DIAGNOSA AKAR MASALAH (MESIN VS GILIR KERJA):                                  │
│    Manajemen kesulitan membedakan apakah lonjakan cacat disebabkan oleh penurunan      │
│    performa fisik komponen mesin (rol karet mengeras/licin, selimut karet aus,         │
│    penjepit silinder melemah) atau akibat variasi penyetelan awal dan kelelahan        │
│    ritme sirkadian operator pada Shift Malam (pukul 23.00–07.00 WIB).                  │
│                                                                                        │
│ 3. EVALUASI KINERJA OPERATOR TERTUNDA:                                                 │
│    Kepala Unit dan Kepala Kelompok tidak dapat memberikan bimbingan teknis harian      │
│    karena rekam jejak kerja baru diketahui berbulan-bulan kemudian secara manual.      │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 4.3 Permasalahan yang Dialami pada Tahun 2025: Ketiadaan Atribusi Mesin & Pola Gilir Kerja (*The Missing Link*)
Sepanjang tahun operasional 2025, Unit Cetak Pita Cukai menghadapi kendala mendasar dalam tata kelola data pengendalian mutu cetak. Meskipun laporan verifikasi mutu dan sistem SAP telah mampu menyajikan kategori jenis cacat fisik secara global di tingkat unit (seperti cacat blobor, noda tinta, atau pergeseran register), data umum tersebut belum memadai untuk melakukan perbaikan presisi di area mesin. **Mengetahui *apa* jenis kerusakannya terbukti belum cukup tanpa mengetahui *di mesin mana* kerusakan tersebut terjadi dan *faktor operasional apa* yang memicunya.**

Kondisi inilah yang menjadi permasalahan utama yang dialami pada tahun 2025 di unit cetak, di mana sistem pencatatan eksisting belum mampu menjawab tiga pertanyaan operasional fundamental di lapangan:
1. *"Pada mesin cetak mana (dari 9 mesin yang beroperasi) kerusakan spesifik tersebut terkonsentrasi?"*
2. *"Apakah tingginya kerusakan dipicu oleh penurunan performa komponen mekanis mesin atau variasi metode kerja dan kelelahan operator pada pola gilir kerja (shift) tertentu?"*
3. *"Berapa kontribusi kuantitas lembar cetak dan tingkat kerusakan riil dari masing-masing tim kerja?"*

Ketiadaan jawaban atas ketiga pertanyaan fundamental tersebut mengakibatkan tindakan perbaikan teknis mesin berlangsung lambat karena teknisi harus memeriksa seluruh 9 mesin secara spekulatif (*trial-and-error*), evaluasi kinerja operator terhambat oleh rekapitulasi buku folio manual yang menumpuk, serta angka *inschiet* berfluktuasi tinggi sepanjang tahun 2025 (mencapai puncak 5,11% di Kuartal 4).

---

## 5. Skala Dampak Finansial & Risiko Pembiaran (*Cost of Inaction*)

Tingkat kerusakan cetak (*inschiet*) rata-rata sebesar **4,61%** pada volume produksi tahunan pita cukai menimbulkan konsekuensi biaya yang sangat masif bagi perusahaan. Mengingat rincian biaya pokok produksi maupun harga jual resmi produk pita cukai merupakan informasi rahasia perusahaan (*corporate privacy/confidential*), maka perhitungan simulasi finansial dalam kajian ini menggunakan angka estimasi biaya cetak sebesar **Rp 3.000\* per lembar cetak**. Nilai ini diperhitungkan secara rasional berdasarkan komponen biaya bahan baku (kertas sekuriti khusus dan tinta sekuriti), penyusutan mesin cetak, serta alokasi jam kerja tenaga kerja di lapangan.

### 5.1 Kertas Kerja Skala Dampak Finansial Baseline 2025
Kalkulasi dampak finansial disusun secara transparan ke dalam dua skenario perhitungan matematis terbuka:

#### Skenario A: Berdasarkan Standar Rata-Rata Pesanan Tahunan (160.000.000 Lembar)
$$\begin{aligned}
\text{Volume Pesanan Tahunan Rata-Rata} &= 160.000.000 \text{ Lembar Cetak} \\
\text{Estimasi Lembar Rusak Baseline (4,61\%)} &= 160.000.000 \times 4,61\% = \mathbf{7.376.000 \text{ Lembar Rusak / Tahun}} \\
\text{Nilai Kerugian Finansial Baseline} &= 7.376.000 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 22.128.000.000 \text{ / Tahun}} \\
&\approx \mathbf{\text{Rp } 22,13 \text{ Miliar / Tahun (atau Rp 1,84 Miliar / Bulan)}}
\end{aligned}$$

#### Skenario B: Berdasarkan Realisasi Volume Pesanan Aktual 2025 (177.636.930 Lembar)
$$\begin{aligned}
\text{Total Volume Pesanan Aktual 2025} &= 177.636.930 \text{ Lembar Cetak} \\
\text{Jumlah Lembar Rusak Aktual Baseline (4,61\%)} &= 177.636.930 \times 4,61\% = \mathbf{8.189.062 \text{ Lembar Rusak / Tahun}} \\
\text{Nilai Kerugian Finansial Aktual 2025} &= 8.189.062 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 24.567.186.000 \text{ / Tahun}} \\
&\approx \mathbf{\text{Rp } 24,56 \text{ Miliar / Tahun (atau Rp 2,05 Miliar / Bulan)}}
\end{aligned}$$

Perhitungan di atas menegaskan bahwa pada tingkat baseline 4,61%, potensi pemborosan biaya yang ditanggung perusahaan berkisar antara **Rp 22,13 Miliar hingga Rp 24,56 Miliar per tahun**.

### 5.2 Valuasi Efisiensi per 1,00% Penurunan Inschiet
Besarnya volume produksi pita cukai menunjukkan bahwa setiap keberhasilan memangkas **1,00% (100 basis poin) *inschiet*** akan menghasilkan potensi penghematan biaya produksi (*cost avoidance*) yang sangat signifikan bagi Perum Peruri:
* Pada standar volume rata-rata tahunan (160 Juta lembar), setiap penurunan 1,00% *inschiet* setara dengan penyelamatan **1.600.000 lembar kertas sekuriti fisik** atau efisiensi sebesar **Rp 4,80 Miliar / tahun**:
  $$\text{Efisiensi per 1,00\%} = 1.600.000 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 4.800.000.000 \text{ / Tahun}}$$
* Pada volume aktual pesanan tahun 2025 (177,6 Juta lembar), setiap penurunan 1,00% *inschiet* setara dengan penyelamatan **1.776.369 lembar kertas sekuriti fisik** atau efisiensi sebesar **Rp 5,33 Miliar / tahun**:
  $$\text{Efisiensi per 1,00\%} = 1.776.369 \text{ lembar} \times \text{Rp } 3.000 = \mathbf{\text{Rp } 5.329.107.000 \text{ / Tahun}}$$

### 5.3 Evaluasi Matriks Risiko Pembiaran (*The 5 Pillars Cost of Inaction*)
Apabila kondisi pemisahan data ini dibiarkan terus berlangsung tanpa adanya pembaruan sistemik, unit kerja dan korporasi akan menghadapi konsekuensi risiko operasional yang merugikan:

*Tabel 1.2 Matriks Risiko Pembiaran Operasional (Cost of Inaction)*

| Pilar Evaluasi | Bentuk Risiko Nyata Bila Dibiarkan (*Inaction*) | Tingkat Keparahan | Indikator Dampak Terukur |
| :--- | :--- | :---: | :--- |
| **1. Biaya (*Cost*)** | Akumulasi pemborosan biaya bahan baku kertas dan tinta sekuriti mencapai **Rp 22,13 – Rp 24,56 Miliar per tahun**. | **KRITIS** | Pemborosan biaya cetak ulang & penurunan margin laba unit. |
| **2. Mutu (*Quality*)** | Tingkat *inschiet* berfluktuasi tidak terkendali hingga **5,11%** akibat penanganan suku cadang mesin yang terlambat. | **TINGGI** | Tingginya persentase cacat mutu HCTS di unit kerja. |
| **3. Kepatuhan (*Compliance*)** | Lemahnya akuntabilitas pelacakan (*traceability*) karena pencatatan manual di buku folio menyulitkan audit mutu ISO 9001:2015. | **TINGGI** | Potensi temuan audit dan hilangnya rekam jejak digital per PO. |
| **4. K3L (*Safety & ESG*)** | Timbulan limbah padat lembar rusak mencapai **7,37 – 8,18 Juta lembar/tahun ($\pm 60–65$ Ton kertas)** dan kelelahan operator *shift* malam. | **SEDANG** | Pemborosan sumber daya kertas dan peningkatan beban fisik kerja. |
| **5. Layanan (*Service SLA*)** | Antrean proses cetak pengganti memperlambat serah terima pesanan pita cukai ke DJBC, mengancam target penerimaan APBN. | **TINGGI** | Ancaman denda keterlambatan SLA dan penurunan skor kepuasan DJBC. |

---

## 6. Kesimpulan & Urgensi Intervensi Inovasi (DSS SIRINE 4.0)

Berdasarkan runtutan analisis yang mengalir dari tuntutan mutu industri sekuriti global, kepatuhan klausul kontrak tender DJBC Kemenkeu RI, arahan strategis korporasi Perum Peruri, hingga temuan empiris pemisahan data di Unit Cetak Pita Cukai, dapat disimpulkan bahwa **ketiadaan integrasi data operasional di area mesin merupakan akar masalah fundamental yang menghambat pencapaian target efisiensi perusahaan**.

Untuk mengatasi kebuntuan tersebut, unit kerja melakukan intervensi inovasi terstruktur melalui pengembangan **Decision Support System (DSS) SIRINE 4.0**. Sistem ini menjembatani jurang data (*data silo*) dengan menghubungkan tiga pilar informasi operasional ke dalam satu platform digital terpadu:
$$\mathbf{Data\ Transaksi\ Meja\ Mesin\ (< 30\ Detik)} \longleftrightarrow \mathbf{Modul\ SAP\ Production\ Order\ (ZPPRSIPPC0012)} \longleftrightarrow \mathbf{Data\ Hasil\ Verifikasi\ Mutu\ (HCTS)}$$

Melalui integrasi ini, DSS SIRINE 4.0 menghadirkan keterlacakan data granular:
$$\mathbf{Nomor\ PO} \longrightarrow \mathbf{Nomor\ Mesin\ (9\ Mesin)} \longrightarrow \mathbf{Pola\ Gilir\ Kerja\ (Shift\ 1/2/3)} \longrightarrow \mathbf{Tim\ Operator} \longrightarrow \mathbf{Kategori\ Cacat\ Cetak}$$

*Tabel 1.3 Kertas Kerja Realisasi Penurunan Inschiet dan Simulasi Finansial Semester 1 2026*

| Periode Realisasi | Volume Produksi ($n$) | Inschiet Aktual (%) | Deviasi vs Baseline (4,61%) | Lembar Ekspektasi Cacat (4,61%) | Lembar Cacat Aktual Realisasi | Lembar Diselamatkan (*Defect Reduction*) | Nilai Potensi Penghematan ($\times \text{Rp } 3.000$)* |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Q1 2026** *(Adaptasi)* | **57.385.254** | **4,34%** | -0,27 pp (-5,86%) | 2.645.460 lb | 2.490.520 lb | **154.940 Lembar** | **Rp 464.820.000** *(Rp 464,82 Juta)* |
| **Q2 2026** *(Tindakan Presisi)* | **45.960.434** | **3,33%** | **-1,28 pp (-27,77%)** | 2.118.776 lb | 1.530.482 lb | **588.294 Lembar** | **Rp 1.764.882.000** *(Rp 1,76 Miliar)* |
| **TOTAL SEMESTER 1 2026** | **103.345.688** | **3,89%** *(avg)* | **-0,72 pp (-15,62%)** | 4.764.236 lb | 4.021.002 lb | **743.234 Lembar** | **Rp 2.229.702.000** *(Rp 2,23 Miliar)* |

*(Sumber: Konsolidasi Data Produksi & Verifikasi Mutu Peruri 2026. \*Catatan: Nilai estimasi biaya cetak untuk simulasi efisiensi internal).*

Keberhasilan implementasi DSS SIRINE 4.0 pada Semester 1 tahun 2026 terbukti secara empiris mampu:
1. Memangkas persentase *inschiet* dari baseline **4,61% menjadi 4,34% pada Q1** dan mencapai **3,33% pada Q2 2026** (penurunan sebesar **-1,28 pp / -27,77%**).
2. Menyelamatkan **743.234 lembar fisik kertas sekuriti** dari pemborosan cetak dalam kurun waktu 6 bulan pertama.
3. Mengamankan potensi efisiensi biaya manufaktur (*cost avoidance*) sebesar **Rp 2,23 Miliar pada Semester 1 2026** (dengan potensi penghematan tahunan terproyeksi sebesar **Rp 6,82 Miliar / tahun**).
4. Memangkas durasi pemeriksaan dan penanganan teknis mesin dari **> 1 *shift* (> 8 jam) menjadi < 2–4 jam (efisiensi waktu henti $\ge 50\%–75\%$)**.
