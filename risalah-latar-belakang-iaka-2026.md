# BACKGROUND AND PROBLEM IDENTIFICATION REPORT
### *Quality Control Governance Transformation in the Excise Stamp Printing Unit: Meeting Global Market Demands, National Tender Commitments, and Peruri's Strategic Objectives Through Machine-Desk Data Integration*

---

> ***Executive Takeaway:***  
> To uphold high-security printing standards and secure national excise stamp procurement contracts from the Directorate General of Customs and Excise (DJBC), Ministry of Finance of the Republic of Indonesia, Perum Peruri prioritizes cost efficiency and stringent quality assurance. All corporate strategic targets converge at the shop-floor level within the Excise Stamp Printing Unit, which managed an actual production volume of **177,636,930 Print Sheets in 2025** (with an annual baseline average of **160,000,000 Print Sheets**). Throughout 2025, the average printing defect rate (*inschiet*) stood at **4.61%**, with a fourth-quarter peak reaching **5.11%**, generating an annual cost of poor quality of **Rp 22.13 Billion to Rp 24.56 Billion per year**. The core operational bottleneck stemmed from **fragmented data silos**: production progress was logged manually in physical folio logbooks at machine control desks, while quality sorting data in SAP module `ZPPRSIPPC0012` was aggregated only at the unit-wide level without machine-specific or shift-level attribution. This data blindness forced maintenance technicians into speculative trial-and-error troubleshooting lasting **> 1 shift (> 8 hours) per machine**, delayed operator feedback, and heightened delivery schedule (*Service Level Agreement*) risks. The deployment of the **Decision Support System (DSS) SIRINE 4.0** integrated machine-desk transaction data, SAP production orders, and sorting verification results in real time, successfully reducing the defect rate to **3.89% in H1 2026 (reaching 3.33% in Q2 2026)**, rescuing **743,234 security print sheets**, and delivering verified cost avoidance of **Rp 2.23 Billion**.

---

## 1. Global Market Dynamics: Precision Standards & Competitive Advantage in High-Security Printing

In the high-security printing industry, a security printer's reputation and market competitiveness depend on strict compliance with international benchmarks, including standards established by *Intergraf* and the *World Customs Organization* (WCO). Every sovereign security document requires absolute dimensional and chromatic precision to prevent counterfeiting (*anti-counterfeiting*). Multi-layered security features are systematically integrated across substrates and print stages, ranging from specialized security fibers embedded in watermarked paper, ultra-violet (UV) luminescent and optically variable inks, intricate *guilloche* patterns, and microscopic text (*microtext*), to high-precision diffractive optically variable image devices (DOVID/holograms).

When competing against domestic commercial security printers and global printing conglomerates, Peruri's competitive standing is evaluated against four primary criteria:

1. **Zero-Defect Assurance:** For sovereign fiscal security documents, physical print anomalies such as ink bleeding (*blobor*), hickies (*noda bintik*), or inter-color register shifts (*misregister*) represent critical defects. These flaws undermine the document's anti-counterfeiting integrity, obstruct automated or field verification by law enforcement officers, and pose serious legal risks regarding document authenticity. Consequently, defect tolerances in high-security printing are strictly minimized toward zero.
2. **Cost Competitiveness:** Government procurement evaluations consistently demand rigorous value-for-money. Given the high unit costs of imported security substrates, specialized security inks, and proprietary features, printing facilities burdened by high spoilage rates (*inschiet*) incur inflated unit manufacturing costs, thereby eroding the company's pricing competitiveness during tender evaluations.
3. **Strict Delivery Service Level Agreements (SLAs):** Clients enforce rigid distribution timelines across nationwide logistical networks. Supply chain bottlenecks caused by extended reprinting cycles (*tambah cetak*) disrupt downstream manufacturing operations and delay state revenue collection.
4. **Substrate Accountability & Chain of Custody (Zero-Leakage):** Clients require total accountability over all raw security materials and finished sheets. Every defective security sheet must be systematically tracked, isolated, and officially destroyed under strict chain-of-custody protocols (*berita acara pemusnahan*) to prevent unauthorized circulation into illicit secondary markets.

These four market criteria are directly reflected in the technical and operational clauses governing the national security document procurement tenders issued by the Government of the Republic of Indonesia.

---

## 2. National Tender Scale: Procurement Contracts & Fiscal Integrity of DJBC Ministry of Finance RI

The Government of the Republic of Indonesia, through the **Directorat Jenderal Bea dan Cukai (DJBC) - Ministry of Finance RI**, conducts annual national procurement tenders for sovereign fiscal security documents in the form of **Excise Stamps (*Pita Cukai*)**, comprising **Tobacco Product Excise Stamps (*Pita Cukai Hasil Tembakau / PCHT*)** and **Alcoholic Beverage Excise Stamps (*Minuman Mengandung Etil Alkohol / MMEA*)**. As an official fiscal instrument, the excise stamp serves as legal proof of tax settlement, directly safeguarding hundreds of trillions of Rupiah allocated to the State Budget (*Anggaran Pendapatan dan Belanja Negara / APBN*).

The strategic fiscal significance of excise stamps establishes stringent contract clauses and technical compliance requirements for the authorized security printer:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│             QUALITY & COMPLIANCE CLAUSES IN NATIONAL EXCISE STAMP TENDERS             │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. ABSOLUTE QUALITY SPECIFICATIONS:                                                    │
│    • All physical security features (security paper, UV inks, guilloche, & holograms) │
│      must be printed with micron-level precision, free from color or register shifts.  │
│    • Print defects risk triggering false-positive counterfeit alerts in the market.    │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 2. RIGOROUS RECONCILIATION OF DEFECTIVE SHEETS (HCTS):                                 │
│    • Every non-conforming sheet is classified as a Defective Print Sheet (HCTS)        │
│      and must be accounted for through official chain-of-custody destruction records.  │
│    • Elevated defect rates overburden verification sorting and physical audit teams.   │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 3. STRICT SERVICE LEVEL AGREEMENT (SLA) COMPLIANCE:                                    │
│    • Nationwide delivery schedules totaling hundreds of millions of sheets must be     │
│      fulfilled on time to ensure continuous operations for manufacturers and steady    │
│      cash inflows for state revenue collection.                                        │
│    • Lengthy reprinting cycles directly introduce severe financial delay penalties.    │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

The scale of annual national excise stamp procurement averages **160,000,000 Print Sheets per year**, with total actual production orders in fiscal year 2025 reaching **177,636,930 Print Sheets**. This massive operational volume, combined with unforgiving quality parameters, requires printing lines to operate with high mechanical stability and minimal recurring defects.

---

## 3. Strategic Mandate & Corporate Objectives of Perum Peruri

Pursuant to **Government Regulation No. 06 of 2019 (*Peraturan Pemerintah Nomor 06 Tahun 2019*)**, **Perum Percetakan Uang Republik Indonesia (Peruri)** is entrusted with the exclusive state mandate to print Rupiah currency notes and produce high-security sovereign documents for the Republic of Indonesia. Peruri is committed to serving as an integrated high-security printing enterprise and world-class authenticity guarantor.

To maintain customer trust, secure long-term tender wins with DJBC, and protect corporate operating margins, Peruri's Board of Directors and Executive Management established three primary strategic pillars:

1. **Cost Leadership & Material Protection:** Because security paper substrates and proprietary security inks represent high-cost direct materials, management mandates aggressive reductions in the material spoilage ratio (*inschiet*) to protect manufacturing margins.
2. **Operational Excellence:** Aligning manufacturing workflows with **ISO 9001:2015** quality management standards to ensure installed production capacity fulfills contract commitments without generating excessive paper waste (*afval*).
3. **Shop-Floor Digitalization (*Smart Factory & INDI 4.0*):** Transforming manual logbooks at machine control desks into an integrated, real-time digital operational data flow, empowering shop-floor supervisors and technical teams to execute data-driven corrective interventions.

---

## 4. Shop-Floor Reality in the Excise Stamp Printing Unit: Operational Dynamics & Critical Pain Points

The Excise Stamp Printing Unit (*Unit Cetak Pita Cukai*), operating under the Vault and Verification Department (*Departemen Khazanah dan Verifikasi*), Strategic Business Unit (SBU) High Security Solution, manages high-speed sheet-fed offset printing lines. The production facility runs **continuously 24 hours a day, 7 days a week**, utilizing a **3-shift rotating schedule**:
* **Morning Shift:** 07:00 – 15:00 WIB
* **Afternoon Shift:** 15:00 – 23:00 WIB
* **Night Shift:** 23:00 – 07:00 WIB

The printing operations are executed across **9 sheet-fed offset printing presses** manned by approximately **$\pm 42$ certified press operators and shift team leaders**. The 9-machine press fleet comprises:
* **4 Komori Presses:** `KMR 1`, `KMR 2`, `KMR 3`, and `KMR 4`
* **2 Ryobi Presses:** `RYB 1` and `RYB 2`
* **3 Heidelberg GTO Presses:** `GTO 1`, `GTO 2`, and `GTO 3`

Table 1.1 summarizes the operational capacity parameters and baseline print quality data for fiscal year 2025 in the printing unit.

*Table 1.1 Operational Parameters and 2025 Baseline Printing Defect Rate (Inschiet) in the Excise Stamp Printing Unit*

| Operational Parameter / Period | Value / Metric | Unit | Verified Data Source |
| :--- | :---: | :---: | :--- |
| **Active Printing Press Fleet** | **9 Presses (4 Komori, 2 Ryobi, 3 GTO)** | Machine Units | Asset Inventory, Vault & Verification Department |
| **Shift Rotation Schedule** | **3 Shifts (Morning, Afternoon, Night)** | Shifts / Day | Standard Shop-Floor Shift Roster |
| **Daily Operational Duration** | **24** | Hours / Day | Standard Operating Procedure (SOP), Printing Unit |
| **Total Press Operating Crew** | **$\pm 42$** | Personnel | Workforce Allocation Records, Printing Section |
| **Annual Target Volume Standard** | **160,000,000** | Print Sheets | PPIC Production Capacity Planning Standard |
| **Actual Total Production Volume 2025** | **177,636,930** | Print Sheets | SAP Production Order Module (`ZPPRSIPPC0012`) |
| **Q1 2025 Defect Rate (*Inschiet*)** | **4.72%** | Percentage (%) | Quality Verification Summary & SAP Module |
| **Q2 2025 Defect Rate (*Inschiet*)** | **3.97%** | Percentage (%) | Quality Verification Summary & SAP Module |
| **Q3 2025 Defect Rate (*Inschiet*)** | **4.64%** | Percentage (%) | Quality Verification Summary & SAP Module |
| **Q4 2025 Defect Rate (*Inschiet*)** | **5.11%** | Percentage (%) | Quality Verification Summary & SAP Module |
| **2025 ANNUAL BASELINE INSCHIET** | **4.61%** | Percentage (%) | Annual Consolidated QC Report & SAP (`ZPPRSIPPC0012`) |
| **Trial Troubleshooting Downtime** | **> 1 Shift (> 8 Hours)** | Hours / Machine | Machine Maintenance Incident Logs |

### 4.1 2025 Baseline Fluctuation Analysis: Process Capability vs. Year-End Order Spikes
Historical production records in Table 1.1 show that the annual average defect rate (*inschiet*) across 2025 stood at **4.61%**. Notably, during **Quarter 2 (Q2) 2025**, the defect rate dropped to **3.97%**. This Q2 milestone empirically demonstrated that the unit's machines and operator crews possess the technical capability to operate below the corporate 4.00% defect tolerance threshold when press parameters, roller nip pressures, and operational conditions remain well-calibrated.

However, in **Quarter 4 (Q4) 2025**, the defect rate escalated to an annual peak of **5.11%** (+1.14 percentage points compared to Q2 2025). This surge coincided with the release of high-volume production orders featuring new annual excise stamp designs ahead of fiscal year-end deadlines. Because the press floor lacked a real-time machine-level diagnostic system, initial make-ready setup times expanded, and subtle print deviations went unnoticed during press speed ramp-ups, compounding defective sheet output across multiple shifts.

### 4.2 Shop-Floor Operational Disconnect: The Data Silo Phenomenon
The persistence of high defect rates and prolonged technical troubleshooting in the field stemmed directly from **operational data silos** separating the machine control desks from the administrative quality management systems:

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        STRUCTURE OF OPERATIONAL DATA SILOS                             │
├───────────────────────────────────────────┬────────────────────────────────────────────┤
│         MACHINE CONTROL DESK LOGGING      │         VERIFICATION SORTING WORKFLOW      │
├───────────────────────────────────────────┼────────────────────────────────────────────┤
│ • Manually recorded in PHYSICAL FOLIO     │ • Printed sheets undergo sorting in the    │
│   LOGBOOKS at the 9 press consoles.       │   Verification Unit with a 1–2 day lag.    │
│ • Daily transaction data remains isolated │ • Defect counts entered into SAP module    │
│   and dormant at individual presses.      │   ZPPRSIPPC0012 as a UNIT-WIDE SUMMARY     │
│ • Manually compiled by Team Leaders only  │   (general aggregated defect total).       │
│   during quarterly performance reviews.   │ • SAP records reside on office computers   │
│ • Highly vulnerable to calculation errors │   WITHOUT MACHINE-SPECIFIC, PO-SPECIFIC,   │
│   and physical document misplacement.     │   OR SHIFT-SPECIFIC ATTRIBUTION.           │
└───────────────────────────────────────────┴────────────────────────────────────────────┘
                                    │
                                    ▼
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                  SHOP-FLOOR OPERATIONAL IMPACT OF DATA BLINDNESS                       │
├────────────────────────────────────────────────────────────────────────────────────────┤
│ 1. SPECULATIVE TRIAL-AND-ERROR TROUBLESHOOTING (> 8 HOURS / MACHINE):                  │
│    When verification teams report an increase in ink bleeding or hickies, technicians  │
│    cannot pinpoint which press is responsible. Mechanics must inspect all 9 presses    │
│    sequentially through trial and error, prolonging unproductive downtime.             │
│                                                                                        │
│ 2. INABILITY TO ISOLATE MECHANICAL VS. OPERATIONAL ROOT CAUSES:                        │
│    Technicians cannot differentiate whether defect spikes stem from mechanical         │
│    degradation (roller glazing/hardening, blanket fatigue, loose cylinder grippers)     │
│    or operational variance and visual fatigue during the Night Shift (23:00–07:00 WIB).│
│                                                                                        │
│ 3. DELAYED OPERATOR PERFORMANCE FEEDBACK:                                              │
│    Section Heads and Team Leaders cannot deliver timely coaching because individual    │
│    crew performance records are compiled months after production runs conclude.        │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

### 4.3 2025 Quality Bottleneck: Lack of Machine & Shift Attribution (*The Missing Link*)
Throughout 2025, SAP summaries and quality reports presented defect counts only as global unit-wide categories (such as general ink bleeding, ink spots, or register shifts). The reporting pipeline failed to capture which specific printing press, which production order (PO), and which operational shift generated those non-conforming sheets. Identifying *what* defect occurred proved insufficient without knowing *on which machine* it originated and *under which operating parameters* it developed.

This attribution blindness left three fundamental operational questions unanswered on the shop floor:
1. *"Across the 9 operating printing presses, which specific machine generated the majority of a given defect?"*
2. *"Is a defect spike driven by mechanical degradation of specific press components or by make-ready variance and circadian fatigue on the night shift?"*
3. *"What exact quantities of perfect conforming sheets (HCS) and defective sheets (HCTS) were produced by each operating crew per production order?"*

Because these questions could not be answered from existing data, mechanical troubleshooting remained speculative (*trial-and-error*) lasting > 8 hours per machine, operator skill coaching was delayed, and the 2025 defect rate remained stagnant at a 4.61% baseline (peaking at 5.11% in Q4).

---

## 5. Scale of Financial Impact & The Cost of Inaction

An average printing defect rate (*inschiet*) of **4.61%** across annual excise stamp production volumes imposes substantial financial losses. Because detailed bill-of-materials and official commercial sales prices are proprietary corporate data, the financial simulations in this study utilize a standard industry reprint cost estimate of **Rp 3,000\* per print sheet** (accounting for security paper substrates, specialized security inks, press depreciation, and direct manufacturing labor).

### 5.1 2025 Baseline Financial Impact Simulation
The baseline financial impact is modeled across two distinct operational volume scenarios:

#### Scenario A: Standard Annual Capacity Target (160,000,000 Sheets)
$$\begin{aligned}
\text{Standard Annual Planned Volume} &= 160,000,000 \text{ Print Sheets} \\
\text{Estimated Baseline Defective Sheets (4.61\%)} &= 160,000,000 \times 4.61\% = \mathbf{7,376,000 \text{ Defective Sheets / Year}} \\
\text{Baseline Financial Loss (Standard)} &= 7,376,000 \text{ sheets} \times \text{Rp } 3,000 = \mathbf{\text{Rp } 22,128,000,000 \text{ / Year}} \\
&\approx \mathbf{\text{Rp } 22.13 \text{ Billion / Year (or Rp 1.84 Billion / Month)}}
\end{aligned}$$

#### Scenario B: Actual Realized Order Volume in 2025 (177,636,930 Sheets)
$$\begin{aligned}
\text{Actual Total Production Volume 2025} &= 177,636,930 \text{ Print Sheets} \\
\text{Actual Baseline Defective Sheets (4.61\%)} &= 177,636,930 \times 4.61\% = \mathbf{8,189,062 \text{ Defective Sheets / Year}} \\
\text{Actual Baseline Financial Loss 2025} &= 8,189,062 \text{ sheets} \times \text{Rp } 3,000 = \mathbf{\text{Rp } 24,567,186,000 \text{ / Year}} \\
&\approx \mathbf{\text{Rp } 24.56 \text{ Billion / Year (or Rp 2.05 Billion / Month)}}
\end{aligned}$$

These calculations confirm that at the 4.61% baseline defect rate, the company incurs an avoidable quality cost burden of **Rp 22.13 Billion to Rp 24.56 Billion per year**.

### 5.2 Financial Valuation per 1.00% Defect Rate Reduction (100 bps)
Given the massive volume of sovereign print production, every **1.00% (100 basis points) reduction in *inschiet*** delivers immediate, verified cost avoidance for Perum Peruri:
* **Under Standard Capacity (160 Million sheets/year):** Each 1.00% defect reduction preserves **1,600,000 security sheets**, yielding annual cost savings of **Rp 4.80 Billion / year**:
  $$\text{Savings per 1.00\% Reduction} = 1,600,000 \text{ sheets} \times \text{Rp } 3,000 = \mathbf{\text{Rp } 4,800,000,000 \text{ / Year}}$$
* **Under 2025 Actual Volume (177.6 Million sheets/year):** Each 1.00% defect reduction preserves **1,776,369 security sheets**, yielding annual cost savings of **Rp 5.33 Billion / year**:
  $$\text{Savings per 1.00\% Reduction} = 1,776,369 \text{ sheets} \times \text{Rp } 3,000 = \mathbf{\text{Rp } 5,329,107,000 \text{ / Year}}$$

### 5.3 5-Pillar Cost of Inaction Risk Assessment
Allowing operational data silos and speculative troubleshooting to persist exposes the organization to critical risks across five core pillars:

*Table 1.2 Five-Pillar Cost of Inaction Risk Matrix*

| Evaluation Pillar | Operational Risk of Inaction | Severity | Measurable Impact Indicator |
| :--- | :--- | :---: | :--- |
| **1. Cost** | Cumulative material and ink waste reaching **Rp 22.13 – Rp 24.56 Billion per year**. | **CRITICAL** | Inflated reprinting costs and eroded manufacturing margins. |
| **2. Quality** | Unchecked defect rate spikes reaching **5.11%** due to delayed component replacement. | **HIGH** | Elevated volume of non-conforming sheets (HCTS) in the sorting unit. |
| **3. Compliance** | Manual logbooks hinder rapid batch traceability during ISO 9001:2015 quality audits. | **HIGH** | Audit non-conformances and missing digital production histories per PO. |
| **4. Safety & ESG** | Substantial physical substrate waste of **7.37 – 8.18 Million sheets/year ($\pm 60–65$ Metric Tons of paper)** and operator fatigue. | **MEDIUM** | Depletion of raw materials and heightened night-shift operator workload. |
| **5. Service SLA** | Extended reprinting cycles delay delivery handovers to DJBC and disrupt downstream cigarette manufacturing lines. | **HIGH** | Contractual late-delivery penalties and customer dissatisfaction. |

---

## 6. Synthesis & Urgency of Innovation: Decision Support System (DSS) SIRINE 4.0

The analytical progression—spanning global high-security industry benchmarks, national DJBC tender requirements, Peruri's strategic corporate mandate, and shop-floor data silos—confirms that **the absence of integrated machine-level operational data was the fundamental root cause constraining manufacturing efficiency**.

To resolve this challenge, the printing unit developed and deployed the **Decision Support System (DSS) SIRINE 4.0**. The platform digitally bridges three critical operational nodes into an integrated data ecosystem:
$$\mathbf{Machine\ Control\ Desk\ Data\ (< 30\ Seconds)} \longleftrightarrow \mathbf{SAP\ Production\ Order\ Module\ (ZPPRSIPPC0012)} \longleftrightarrow \mathbf{Sorting\ Verification\ Quality\ Data\ (HCTS)}$$

Through this architecture, operational data flows seamlessly across all production parameters:
$$\mathbf{PO\ Number} \longrightarrow \mathbf{Machine\ Number\ (9\ Presses)} \longrightarrow \mathbf{Shift\ Pattern\ (Shifts\ 1/2/3)} \longrightarrow \mathbf{Operating\ Crew} \longrightarrow \mathbf{Specific\ Defect\ Category}$$

*Table 1.3 Realized Defect Reduction and Financial Simulation Worksheet for First Half (H1) 2026*

| Operational Period | Production Volume ($n$) | Actual Inschiet (%) | Deviation vs. Baseline (4.61%) | Expected Baseline Defects (4.61%) | Actual Realized Defects | Rescued Sheets (*Defect Reduction*) | Verified Cost Avoidance ($\times \text{Rp } 3,000$)* |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Q1 2026** *(Adaptation Phase)* | **57,385,254** | **4.34%** | -0.27 pp (-5.86%) | 2,645,460 sheets | 2,490,520 sheets | **154,940 Sheets** | **Rp 464,820,000** *(Rp 464.82 Million)* |
| **Q2 2026** *(Precision Action)* | **45,960,434** | **3.33%** | **-1.28 pp (-27.77%)** | 2,118,776 sheets | 1,530,482 sheets | **588,294 Sheets** | **Rp 1,764,882,000** *(Rp 1.76 Billion)* |
| **TOTAL H1 2026** | **103,345,688** | **3.89%** *(avg)* | **-0.72 pp (-15.62%)** | 4,764,236 sheets | 4,021,002 sheets | **743,234 Sheets** | **Rp 2,229,702,000** *(Rp 2.23 Billion)* |

*(Source: Consolidated Production & Verification Records, Perum Peruri 2026. \*Note: Reprint unit cost used for internal financial simulation).*

The empirical deployment of DSS SIRINE 4.0 during the First Half (H1) of 2026 demonstrated clear operational and financial breakthroughs:
1. **Accelerated Defect Reduction:** Reduced the printing defect rate from the **4.61% baseline to 4.34% in Q1 2026**, reaching **3.33% in Q2 2026** (an overall reduction of **-1.28 percentage points / -27.77%**).
2. **Substrate Preservation:** Successfully prevented the destruction of **743,234 high-security print sheets** across six months of production.
3. **Direct Financial Impact:** Generated **Rp 2.23 Billion in verified cost avoidance during H1 2026**, with annualized cost avoidance projected at **Rp 6.82 Billion / year**.
4. **Targeted Maintenance Efficiency:** Reduced machine troubleshooting and diagnostic downtime from **> 1 shift (> 8 hours) to < 2–4 hours per machine (a 50% to 75% reduction in diagnostic downtime)**.
