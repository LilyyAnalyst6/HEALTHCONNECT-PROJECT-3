# HealthConnect Clinic — Data Analytics Track
**AnalystLab Africa Experience Lab | HealthConnect Clinic Experience Lab**

## 📊 Dashboard Overview

**Page 1 — Executive Overview**
Headline KPIs (Total Appointments, Attended, Cancelled, No-Shows, Overall No-Show Rate, Repeat No-Show Rate) alongside the primary drivers: distance band, reminder status, booking lead time, and prior no-show history — each with a reminder-status breakdown for interaction context.

**Page 2 — Secondary Drivers**
Day of week, time of day, reminder channel, appointment type, and the original 3-factor risk segmentation (Low/Medium/High Risk), with synced slicers carried over from Page 1.

**Page 3 — Validation** *(Week 6, tested & refined in Week 7)*
A validation table confirming which Week 5 factors are statistically significant, the refined 4-factor risk segment (Critical/Medium/Minimal Risk), a live Critical Risk Count — now labelled "Critical Risk Count (94 eligible for no-show rate)" following Week 7 testing — and a lead-time-by-distance interaction chart.

---

## 🔑 Key Findings

| Finding | Result |
|---|---|
| Overall no-show rate | **51.2%** (n = 4,737 eligible appointments) |
| Strongest validated driver | **Booking lead time** — 29.5% (0–7 days) → 71.4% (45+ days) |
| Repeat no-show rate | 57.8% (has prior no-show) vs. 46.3% (clean record) |
| Distance effect | 48.7% (<5km) → 56.9% (>15km) |
| Reminder effect | 54.6% (no reminder) → 49.9% (reminder sent); SMS performs best |
| **Refined risk segment (Week 6)** | **Critical Risk: 80.9%** vs. **Minimal Risk: 22.4%** — a validated 58.5-point spread |

Day of week, time of day, age group, and gender were tested and found **not** statistically significant — they are not used as targeting criteria.

---

## 🧪 Methodology

- **Week 5:** Data quality assessment → EDA → 5 KPIs → dashboard → 6 business insights
- **Week 6:** Chi-square significance testing of every Week 5 factor → multivariate logistic regression to confirm independent effects → refined 4-factor risk segmentation validated with 95% confidence intervals → dashboard extended (not rebuilt) → findings handed off to the Data Science track as candidate model features

Full methodology, statistical results, and business recommendations are documented in the two `.docx` reports.

---

## 🧪 Testing & Refinement (Week 7)

Every headline KPI card was independently recomputed against the cleaned dataset, and the dashboard itself was stress-tested rather than assumed correct:

| Test | Finding | Outcome |
|---|---|---|
| KPI recomputation | All core totals and the 51.2% overall rate reproduce exactly | ✅ Pass |
| "No-Show Rate by Distance" card | Card was silently showing the overall rate (51%) instead of the >15km segment | 🔧 Fixed — now correctly shows 56.9–57% |
| Critical Risk Count card | 97 (total tagged) vs. 94 (eligible for the rate) could be misread as inconsistent | 🔧 Fixed — card label now reads "94 eligible for no-show rate" |
| Slicer interactions (6 combinations + 2 edge cases) | No broken or empty visuals, even in small high-risk segments | ✅ Pass |

Full before/after evidence, retest results, and a manual-verification checklist for the significance table are in the Week 7 report.

---



## ⚠️ Limitations

- Dataset is fictional/simulated and does not reflect real-world clinical behaviour
- Cancelled appointments are excluded from the no-show rate denominator (pending formal business confirmation)
- Critical/Minimal risk segments are based on ~100 appointments each; directionally reliable but should be re-validated as more data becomes available

---

## 🛠 Tools Used
 Power BI for the interactive dashboard · Microsoft Word for reporting

