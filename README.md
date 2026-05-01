# Crypto Trading Analytics — Fear & Greed Index

Analysis of crypto trading behavior and profitability across different market sentiment conditions.

## Setup

```bash
pip install pandas numpy matplotlib seaborn scikit-learn 
```

## Files

| File | Description |
|------|-------------|
| `assignment.py` | Data loading, cleaning, timestamp alignment, key metrics |
| `assignment_q2.py` | Performance & behavior analysis by sentiment |
| `assignment_q3.py` | Strategy recommendations |
| `model_clustering.py` | Predictive model + trader clustering |
| `dashboard.py` | Streamlit dashboard |
| `writeup.md` | Methodology, insights, strategy summary |

## How to Run

**Option A — Google Colab**
1. Upload all `.py` files and both CSVs to Colab
2. Run in order: `assignment.py` → `assignment_q2.py` → `assignment_q3.py` → `model_clustering.py`

**Option B — Locally**
```bash
# run analysis
python assignment.py
python assignment_q2.py
python assignment_q3.py
python model_clustering.py

# run dashboard (after model_clustering.py generates the CSVs)
streamlit run dashboard.py
```

## Data

- `fear_greed_index.csv` — daily sentiment score (0–100) from 2018 to 2025
- `historical_data.csv` — 211,224 crypto trades across 32 accounts in 2024
