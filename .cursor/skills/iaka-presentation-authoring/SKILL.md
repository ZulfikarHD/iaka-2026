---
name: iaka-presentation-authoring
description: Author, format, and update pitch-deck PowerPoint (PPTX) presentations for Innovation and Kaizen Awards (IAKA) following Peruri standards, natural shop-floor wording, native chart generation, and value-driven layouts. Use when creating or updating IAKA presentation slides, modifying PPTX files, or designing Kaizen pitch deck slides.
disable-model-invocation: true
---

# IAKA Presentation Authoring & Slide Design

This skill provides step-by-step instructions for authoring and updating PowerPoint (`.pptx`) presentations for the Innovation & Kaizen Award (IAKA) following the official Peruri presentation template, pitch-deck principles, and natural shop-floor Indonesian wording.

---

## 1. Core Principles: Pitch Deck & Shop-Floor Grounding

1. **Self-Explanatory for Jury:** The presentation is what gets submitted and scored. Every slide must be immediately understandable without requiring the jury to read the thick paper.
2. **Pitch Deck Value-Driven:** Lead with metrics, operational reality, clear Before/After comparisons, and financial/process value.
3. **Controlled Slide Expansion:** It is permitted to split a template section (e.g., Point 1 Latar Belakang) into 1–2 focused sub-slides (e.g. `01.1` and `01.2`) to cover "Tujuan" and "Yang harus disampaikan" without crowding text. Keep additions minimal and high-impact.
4. **Natural Shop-Floor Phrasing (Anti-AI Tone):**
   - ❌ *Agregat* $\rightarrow$ ✅ **Data general / Data umum / Ringkasan global**
   - ❌ *Keausan* $\rightarrow$ ✅ **Penurunan performa komponen mesin seiring umur mesin** (atau sebut komponen: *rol karet mengeras/licin*, *blanket turun elastisitas*, *penjepit silinder melemah*)
   - ❌ *Lantai produksi / Lantai pabrik* $\rightarrow$ ✅ **Di lapangan / Di unit cetak / Di area mesin**
   - ❌ *Armada / Fleet* $\rightarrow$ ✅ **6 Mesin cetak (4 Komori: KMR 1–4, 2 Ryobi: RYB 1–2)**
   - ❌ *Kertas kerja finansial* $\rightarrow$ ✅ **Skala dampak finansial / Simulasi finansial**

---

## 2. Template Assets & Dimensions

The standard IAKA 2026 widescreen layout:
- **Dimensions:** 13.333" $\times$ 7.5" (16:9 Widescreen | 12,192,000 $\times$ 6,858,000 EMU).
- **Primary Color Palette:**
  - Navy (Primary Brand): `#20288F` (`RGBColor(32, 40, 143)`)
  - Purple (Primary Accent / Badges): `#6A2CC9` (`RGBColor(106, 44, 201)`)
  - Dark Neutral (Body Text): `#2A2A3D` (`RGBColor(42, 42, 61)`)
  - Muted Neutral (Footers / Subtitles): `#6E6E82` (`RGBColor(110, 110, 130)`)
  - Container Fills: Light Navy (`#F4F7FE`), Light Purple (`#F8F6FE`), Light Red (`#FFF5F5`), Light Amber (`#FFF9E6`), Light Green (`#E8F5E9`)
  - Status Indicators: Red Alert (`#C62828`), Green Success (`#2E7D32`), Amber Warning (`#E65100`)

---

## 3. Slide Architecture & Layout Patterns

### A. Header Standard
Every content slide must maintain the template header:
1. **Left Top Wave Image:** Position `left=-0.118"`, `top=-0.196"`, `width=1.584"`, `height=0.891"`.
2. **Right Top Peruri Logo:** Position `left=12.09"`, `top=0.013"`, `width=1.247"`, `height=0.694"`.
3. **Badge Box:** Rounded rectangle `left=0.60"`, `top=0.65"`, `width=0.80"`, `height=0.72"`, Purple fill, white bold number (e.g., `01.1`, `02`).
4. **Slide Title:** Font Arial 25pt Bold Navy (`#20288F`), `left=1.55"`, `top=0.60"`.
5. **Purpose Subtitle:** `"Tujuan bagian ini: [Tujuan template]"` in Arial 11.5pt (`#6A2CC9` bold prefix + `#2A2A3D` regular text).
6. **Footer:** `"IAKA 2026 — Kerangka Presentasi Peserta · DSS SIRINE 4.0 Unit Cetak Pita Cukai"`.

### B. Content Layout Types
- **3-Column Card Layout:** Used for operational profiles, context setting, problem pillars (e.g. Slide 01.1).
- **Hero KPIs + Split Panels + Native Chart:** Used for data-heavy sections (e.g. Slide 01.2). Top strip has 4 KPI cards; bottom split features a native PPTX column/bar chart on the left and a structured workpaper/callout on the right.

---

## 4. Python-PPTX Automation Recipe

When modifying or generating slides, run a Python script using `python-pptx`:

```python
import io
import pptx
from pptx.util import Inches, Pt
from pptx.dml.color import RGBColor
from pptx.enum.text import PP_ALIGN
from pptx.enum.shapes import MSO_SHAPE
from pptx.chart.data import CategoryChartData
from pptx.enum.chart import XL_CHART_TYPE, XL_LABEL_POSITION

prs = pptx.Presentation('Kerangka_Presentasi_Peserta_IAKA_2026 (1).pptx')
# Add / Modify shapes and charts cleanly
```

### Adding a Native Chart Example:
```python
chart_data = CategoryChartData()
chart_data.categories = ['Q1 (Jan-Mar)', 'Q2 (Apr-Jun)', 'Q3 (Jul-Sep)', 'Q4 (Okt-Des)']
chart_data.add_series('Inschiet 2025 (%)', (4.72, 3.97, 4.64, 5.11))

chart_shape = slide.shapes.add_chart(
    XL_CHART_TYPE.COLUMN_CLUSTERED,
    left, top, width, height,
    chart_data
)
chart = chart_shape.chart
chart.has_legend = False
plots = chart.plots[0]
plots.has_data_labels = True
plots.series[0].format.fill.solid()
plots.series[0].format.fill.fore_color.rgb = RGBColor(106, 44, 201)
```

---

## 5. Verification Checklist

Before finalizing any slide:
- [ ] No banned AI-like words (*agregat*, *keausan*, *lantai produksi*, *armada*, *kertas kerja finansial*).
- [ ] Verified numbers have all 4 attributes (Value, Unit, Period, Source).
- [ ] Visual elements (charts, diagrams, KPI cards) are paired with clear takeaways.
- [ ] Slide is clean, legible, and directly addresses the IAKA template prompt.
