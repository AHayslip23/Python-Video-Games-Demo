# Python Video Games Demo

An exploratory analysis and modeling project on video game sales: games that sold more than 100,000 copies, scraped from vgchartz.com ([Kaggle](https://www.kaggle.com/code/upadorprofzs/eda-video-game-)). It focuses on Nintendo consoles.

## Repository Contents

| File | Description |
|---|---|
| `VideoGamesDemo.ipynb` | Full analysis: cleaning, Nintendo-focused EDA, regression, clustering and classification |

## Commit History

### `8359fe0`: Upload of the video games notebook (2025-03-27)
- **Cleaning:** dropped 2016, 2017 and 2020, which have too little data to analyze.
- **Nintendo EDA:**
  - the Wii and Nintendo DS sell far better than other Nintendo consoles
  - Wii sales rose from 2006 to 2009 and then declined
  - Sports is the top Wii genre, largely because of Wii Sports: Wii Sports and Wii Sports Resort make up about 40% of Wii sports-game sales
  - Mario Kart Wii makes up about 51% of 2008 racing sales
  - Nintendo's yearly sales peaked in 2009
- **Simple linear regression:** North American sales strongly predict global sales (R² = 0.85).
- **Multiple linear regression:** North American, European and Japanese sales predict global sales almost exactly (R² ≈ 0.99), which makes sense because global sales are mostly the sum of the regions.
- **K-means clustering:** grouped games by North American vs. global sales. Most games sit in a dense cluster below $10M.
- **Classification: does a game belong to a Nintendo console, based on its sales?**
  - the data is slightly imbalanced: 61% non-Nintendo, 39% Nintendo
  - logistic regression scored **62.6%** accuracy
  - grid search, class balancing, `MinMaxScaler`, random forest, decision tree and SVM didn't improve on it (60.2–62.5%)
  - conclusion: sales data alone isn't a strong predictor of which console a game is on

## Tools
Python, pandas, NumPy, scikit-learn, matplotlib, seaborn, Jupyter Notebook
