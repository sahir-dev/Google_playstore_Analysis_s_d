# Google Play Store Apps Analysis 📱

Exploratory Data Analysis on 10,000+ Android apps and 37,000+ user reviews.

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Status](https://img.shields.io/badge/Status-Complete-green)

---

## About

I analyzed the Google Play Store dataset to find out what makes apps successful. The data includes app metadata (ratings, downloads, category, price) and user reviews with sentiment scores.

**Questions I wanted to answer:**
- Which categories have the most apps?
- What's the relationship between ratings and downloads?
- Do paid apps perform better than free ones?
- What do users actually think? (sentiment analysis)

## Dataset

| File | Description | Size |
|------|-------------|------|
| `googleplaystore.csv` | App information | 10,841 rows |
| `googleplaystore_user_reviews.csv` | User reviews + sentiment | 64,295 rows |

Source: [Kaggle](https://www.kaggle.com/datasets/lava18/google-play-store-apps)

## Key Findings

### The Numbers
- **10,357 apps** analyzed (after cleaning)
- **37,427 reviews** with sentiment data
- **33 categories**
- Average rating: **4.20**/5

### Interesting Insights

1. **92.6% of apps are free** - but paid apps actually have higher ratings (statistically significant!)

2. **Reviews ↔ Installs correlation: 0.63** - More reviews = more installs. Engagement matters.

3. **GAME category dominates** with 31.5 billion installs, but has lower user sentiment. Users are harsh on games!

4. **64% of reviews are positive** - Overall, users are happy.

5. **EVENTS and EDUCATION** are underserved but have the highest ratings. Opportunity?

## Visualizations

All charts are saved in the `figures/` folder:

| # | Chart | What it shows |
|---|-------|---------------|
| 01 | Rating Distribution | Most apps rated 4.0-4.5 |
| 02 | Category Distribution | FAMILY has most apps |
| 03 | Free vs Paid | 92.6% free, but paid rates higher |
| 04 | Content Rating | Mostly "Everyone" |
| 05 | Install Distribution | Wide range |
| 06 | Rating by Category | EVENTS tops the list |
| 07 | Installs by Category | GAME wins by far |
| 08 | Correlation Matrix | Reviews & Installs linked |
| 09 | Reviews vs Installs | Clear positive trend |
| 10 | Sentiment Distribution | 64% positive |
| 11 | Sentiment Polarity | Slightly positive overall |
| 12 | Top Apps by Sentiment | Best & worst rated |
| 13 | Rating vs Sentiment | They correlate! |
| 14 | Price Analysis | Most paid apps under $5 |
| 15 | Top Apps | Facebook, WhatsApp lead |
| 16 | Dashboard | Everything at a glance |

## Project Structure

```
├── google_playstore_analysis.ipynb   # Main notebook
├── googleplaystore.csv               # App data
├── googleplaystore_user_reviews.csv  # Reviews data
├── figures/                          # All visualizations
│   ├── 01_rating_distribution.png
│   ├── 02_category_distribution.png
│   └── ... (16 total)
├── cleaned_data/                     # Processed datasets
│   ├── cleaned_apps.csv
│   ├── cleaned_reviews.csv
│   └── merged_data.csv
├── requirements.txt
└── README.md
```

## How to Run

1. Clone the repo
```bash
git clone https://github.com/yourusername/google-playstore-analysis.git
cd google-playstore-analysis
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Run the notebook
```bash
jupyter notebook google_playstore_analysis.ipynb
```

4. Run all cells - figures and cleaned data will be saved automatically

## Tech Stack

- Python 3.8+
- Pandas - data manipulation
- NumPy - numerical operations
- Matplotlib & Seaborn - visualization
- SciPy - statistical tests

## Takeaways for App Developers

Based on this analysis:

1. **Aim for 4.0+ rating** - Most successful apps are in this range
2. **Free with in-app purchases works** - Gets downloads while monetizing
3. **Look at EVENTS/EDUCATION** - Less competition, higher ratings
4. **Respond to reviews** - Sentiment affects everything
5. **Update regularly** - Recently updated apps rate better

---

Made with ☕ and Python

