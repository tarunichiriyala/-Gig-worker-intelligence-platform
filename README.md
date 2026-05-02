# 🔍 Gig Worker Intelligence Platform
### Auditing what India's 5 largest gig platforms actually pay vs what they advertise

> **Rapido claims ₹50,000/month. Workers actually earn ₹15,705. That's a 68.6% gap.**
> This project audits earnings claims across 52,000 worker records spanning
> Swiggy, Zomato, Rapido, Urban Company and Porter across 5 Indian cities.

---

## 📊 Key Findings

| Platform | Claimed | Reality | Gap |
|---|---|---|---|
| Rapido | ₹50,000 | ₹15,705 | 68.6% |
| Zomato | ₹35,000 | ₹13,153 | 62.4% |
| Swiggy | ₹40,000 | ₹15,381 | 61.5% |
| Porter | ₹38,000 | ₹18,439 | 51.5% |
| Urban Company | ₹45,000 | ₹25,941 | 42.4% |

- 27% of workers earn **below minimum wage** after deducting costs
- 34.9% of workers fall in **Surviving** persona — the largest group
- Only **17%** of workers are actually Thriving
- Mumbai workers earn most, Chennai workers earn least

---

## 🛠️ Tools Used

Python · Pandas · NumPy · Scikit-learn · SciPy · PostgreSQL  · Power BI · Jupyter

---

## 📁 Project Structure

gig-worker-intelligence-platform/
├── data/
│   ├── raw/                    ← Platform claims CSV
│   └── processed/              ← Generated datasets
├── notebooks/
│   ├── 01_data_generation.ipynb
│   ├── 02_load_to_database.ipynb
│   └── 03_analysis.ipynb
├── sql/
│   └── business_queries.sql
├── dashboard/
│   └── gig_intelligence.pbix
└── reports/
└── key_findings.txt

---

## 🔑 Original Metrics Created

**1. Earnings Gap Score**

Gap Score = ((Claimed - Actual) / Claimed) × 100
Measures how much each platform overstates earnings in advertising.

**2. Effective Hourly Rate**
Net earnings after fuel + phone + depreciation
divided by total hours worked
Compared against Hyderabad minimum wage ₹54/hour

---

## 🧠 Machine Learning

- **K-Means Clustering** — segmented 2,000 workers into 4 personas
- **Statistical Testing** — t-test proving peak hour earnings difference is significant

---

## 📈 Dashboard

4-page interactive Power BI dashboard:
- **Truth Dashboard** — Promised vs Reality comparison
- **City Intelligence** — Earnings by city and platform
- **Persona Explorer** — Interactive worker segment explorer
- **Platform Scorecard** — Full audit report with rankings

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/tarunichiriyala/gig-worker-intelligence-platform.git

# Navigate to folder
cd gig-worker-intelligence-platform

# Create virtual environment
python -m venv venv
venv\Scripts\activate

# Install libraries
pip install pandas numpy matplotlib seaborn scikit-learn scipy shap jupyter psycopg2-binary sqlalchemy

# Run notebooks in order
# 1. notebooks/01_data_generation.ipynb
# 2. notebooks/02_load_to_database.ipynb
# 3. notebooks/03_analysis.ipynb
```

---

## 📋 Data Sources

- PLFS Annual Report 2023-24 (mospi.gov.in)
- ILO Platform Workers India Research
- Platform partner pages (direct earnings claims)
- Telangana minimum wage notification 2024


