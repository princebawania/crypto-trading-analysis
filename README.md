# Crypto Trading Analytics — Fear & Greed Index

Analysis of crypto trading behavior and profitability across different market sentiment conditions.

## Setup

```bash
pip install pandas numpy matplotlib seaborn scikit-learn 
```

## Files

| File | Description |
|------|-------------|
| `Assignment_Q1.ipynb` | Data loading, cleaning, timestamp alignment, key metrics |
| `Assignment_Q2.ipynb` | Performance & behavior analysis by sentiment |
| `Assignment_Q3.ipynb` | Strategy recommendations and Predictive model + trader clustering|
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
