# Marketing ROI & Cohort Analytics Engine

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thrineshthode/Marketing-Analytics-Portfolio/blob/main/Marketing_ROI_Analysis.ipynb)

A full-funnel marketing analytics project that turns a year of e-commerce server logs into budget decisions — cohort retention, unit economics (LTV vs CAC), and return on marketing investment by ad source.

## 📊 The Business Problem

Marketing spend was spread across 7 ad sources with no clear view of which channels actually paid back. This analysis answers one question: **which sources are worth the money, and which are burning it?**

## 📁 Dataset — June 2017 to May 2018

| File | Size | Contents |
|------|------|----------|
| `data/visits_log_us.csv` | ~25 MB | 350,000+ sessions — timestamps, device, ad source per visit |
| `data/orders_log_us.csv` | ~2.3 MB | Transactions — user ID, order time, revenue |
| `data/costs_us.csv` | ~49 KB | 2,542 rows of daily marketing spend by ad source |

## 🔬 Methodology

1. **Examination & preprocessing** — validated schemas, zero missing values, cut memory footprint (strings → datetime/category, downcast numerics)
2. **Exploratory analysis** — daily/weekly/monthly active users, sessions per day, session length, conversion funnels
3. **Cohort analysis** — monthly retention heatmaps; activity surge around the November "Black Friday" period
4. **Unit economics** — LTV vs CAC by cohort and by ad source, break-even analysis
5. **ROMI modeling** — return on marketing investment by ad source and device

## 📈 Key Findings

- **Source 3** was the single most expensive channel — and had the lowest ROI of all.
- Sources **2 and 3** had the highest customer acquisition cost; sources 4, 9, and 10 were the cheapest to acquire from.
- **No cohort returned a profit** after acquisition costs — the acquisition model as it stands is not sustainable.
- **Recommendation:** increase investment in sources **1, 2, and 9**; scale back or phase out sources **3, 10, 4, and 5**.

## ▶️ Run It

**Option 1 — no setup (recommended):** click the **Open in Colab** badge above.

**Option 2 — locally:**
```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Marketing_ROI_Analysis.ipynb
```

## 🛠 Tech Stack

Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter

## 📂 Project Structure

```
├── Marketing_ROI_Analysis.ipynb   # Full analysis: EDA → cohorts → LTV/CAC → ROMI
├── data/
│   ├── visits_log_us.csv          # Session logs
│   ├── orders_log_us.csv          # Order transactions
│   └── costs_us.csv               # Marketing spend by source
└── README.md
```

---
*Built as an end-to-end analytics case study: raw server logs in, marketing budget recommendations out.*
