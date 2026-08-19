# PRESENTASI IAKA 2026
## DSS SIRINE 4.0 — Decision Support System Cetak Pita Cukai
### Perum Peruri · Unit Cetak Pita Cukai · Departemen Khazanah dan Verifikasi Strategic Business Unit High Security Solution

---

# POINT 1 — LATAR BELAKANG & MASALAH

---

## Slide 1.1 — Latar Belakang
### Pita Cukai: Dokumen Sekuriti Negara, Diproduksi 177 Juta Lembar Setahun — di Lini yang Beroperasi 24 Jam Tanpa Henti

**Konteks Operasional:**

- **Mandat Strategis Negara:** Berdasarkan PP No. 06/2019, Perum Peruri mencetak **Pita Cukai Hasil Tembakau (PCHT)** dan **MMEA** sebagai instrumen fiskal DJBC Kemenkeu RI — setiap lembar bernilai kepatuhan dan penerimaan negara
- **Skala Operasional:**
  - **177.636.930 Lembar Cetak** diproses sepanjang tahun 2025 *(SAP `ZPPRSIPPC0012`)*
  - **9 mesin cetak aktif** — Komori (KMR1–4), Ryobi (RYB1–2), GTO (1–3)
  - **3 Shift × 24 Jam**, ±42 operator cetak dan kepala kelompok
- **Tantangan Produk:** Spesifikasi pengamanan bertingkat (*guilloche*, *microtext*, *hologram foil*, tinta UV) menuntut toleransi deviasi mutu yang sangat ketat — setiap lembar cacat wajib dikategorikan sebagai **HCTS (Hasil Cetak Tidak Sempurna)**

> **Takeaway Slide:** Di lini produksi berskala masif dan kritis negara ini, penurunan satu persen pun *inschiet* bernilai **Rp 4,80–5,33 Miliar/tahun**. Setiap titik buta operasional langsung berbiaya besar.

---

## Slide 1.2 — Latar Belakang (lanjutan)
### SIRINE 3.5 (2024) Menjawab *"Apa Jenis Kerusakannya?"* — Tapi Tahun 2025 Melahirkan Titik Buta Baru yang Lebih Dalam

**Evolusi & Kesenjangan Sistem:**

| Sistem | Pertanyaan yang Terjawab | Keterbatasan Kritis |
| :--- | :--- | :--- |
| **SIRINE 3.5 (2024)** | ✅ *"Jenis kerusakan apa yang mendominasi unit cetak?"* | ❌ Tidak menjawab: *mesin mana, shift mana, PO mana* |
| **DSS SIRINE 4.0 (2026)** | ✅ *"Mesin mana? Shift mana? Tindakan presisi apa?"* | — Solusi yang dirancang untuk menutup kesenjangan ini |

**Tiga Pulau Data yang Tak Saling Terhubung (Data Silo):**

```
 SAP ZPPRSIPPC0012          Unit Verifikasi HCTS          Buku Folio Fisik
 ─────────────────          ────────────────────          ────────────────
 Data PO & volume           Data jenis kerusakan          Data mesin, shift,
 cetak tersimpan di         tersaji sebagai               operator — ditulis
 format raw CSV/tabel       ringkasan global unit         tangan di meja mesin
 komputer kantor            tanpa atribusi mesin
      ↓                          ↓                              ↓
  "Data pasif"            "Tidak ada nomor             "Tidak terhubung ke
 tidak terpakai            mesin & shift-nya"           data mutu, rawan
 di lapangan"                                           hilang/rusak"
```

**Dampak Langsung di Lapangan:**
1. **Inspeksi mesin trial-and-error** — teknisi memeriksa seluruh armada satu per satu karena tidak tahu mesin mana yang bermasalah → **>1 shift (>8 jam) downtime per mesin**
2. **Evaluasi kinerja operator bias & terlambat** — data baru direkap saat penilaian kuartalan / akhir kontrak, bukan harian
3. **Tindakan perbaikan salah sasaran** — mesin disetel ulang padahal akar masalahnya ada di variasi SOP operator *shift* malam

> **Takeaway Slide:** SIRINE 3.5 (2024) adalah lompatan besar — tapi telah mencapai *plateau*. Tahun 2025 membuktikan bahwa mengetahui *apa* jenis kerusakannya **belum cukup** tanpa mengetahui *di mesin mana* dan *faktor operasional apa* yang memicunya.

---

## Slide 1.3 — Masalah
### Baseline *Inschiet* 4,61% Sepanjang 2025 = Rp 24,56 Miliar/Tahun Tergerus Diam-Diam

**Data Baseline Terverifikasi (SAP `ZPPRSIPPC0012` & Unit Verifikasi 2025):**

| Kuartal | Inschiet (%) | Catatan Operasional |
| :---: | :---: | :--- |
| Q1 2025 | **4,72%** | Awal tahun, volume normal |
| Q2 2025 | **3,97%** | Kondisi stabil — *terbukti lini mampu <4%* |
| Q3 2025 | **4,64%** | Mulai fluktuasi naik |
| Q4 2025 | **5,11%** ⚠️ | Lonjakan desain baru volume besar |
| **Rata-rata 2025** | **4,61%** | **Baseline resmi** |

**Konversi Finansial — Kerugian Akibat Inschiet Baseline:**

$$\begin{aligned}
\text{Volume Aktual 2025} &= 177.636.930 \text{ Lembar Cetak} \\
\text{Lembar Rusak Baseline (4,61\%)} &= 177.636.930 \times 4{,}61\% = \mathbf{8.189.062 \text{ Lembar / Tahun}} \\
\text{Potensi Kerugian} &= 8.189.062 \times \text{Rp } 3.000^* = \mathbf{\text{Rp } 24{,}56 \text{ Miliar / Tahun}}
\end{aligned}$$

*\*Estimasi internal biaya cetak untuk simulasi dampak finansial (bukan biaya produksi atau harga jual resmi)*

**Matriks Risiko Pembiaran — 5 Pilar** *(bila dibiarkan tanpa intervensi):*

| Pilar | Risiko Nyata | Level |
| :--- | :--- | :---: |
| 💰 **Biaya** | Rp 22,13–24,56 Miliar/tahun tergerus pemborosan bahan baku & jam mesin | 🔴 KRITIS |
| 🎯 **Mutu** | Inschiet berfluktuasi tak terkendali hingga 5,11%, tindakan perbaikan tidak bertahan | 🔴 TINGGI |
| 📋 **Kepatuhan** | Pencatatan manual buku folio tidak dapat diaudit digital → risiko temuan ISO 9001:2015 | 🟠 TINGGI |
| 🌱 **K3L / ESG** | 7,37–8,18 Juta lembar rusak/tahun ≈ ±60–65 Ton kertas terbuang + risiko fatigue shift malam | 🟡 SEDANG |
| 📦 **Layanan SLA** | Antrean cetak pengganti → keterlambatan serah terima ke DJBC → risiko denda SLA | 🟠 TINGGI |

> **Takeaway Slide:** Q2 2025 membuktikan lini ini **mampu** menyentuh 3,97% — artinya kapabilitas ada, tapi sistem diagnostiknya tidak. Tanpa intervensi, pola lonjakan Q4 akan terus berulang dan menguras Rp 2+ Miliar setiap bulannya.

---
