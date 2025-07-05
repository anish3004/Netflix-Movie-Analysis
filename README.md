#  Netflix Movie Data Analysis & Popularity Prediction

This project explores a Netflix movie dataset with the goal of understanding trends and building a machine learning model to predict whether a movie is likely to be a **HIT** or **FLOP**, based on key features like genre, vote count, and popularity score.

---

##  Dataset Overview

- **Source**: `mymoviedb.csv`
- **Total Records**: 9,827
- **Features**:
  - `Title`, `Release_Date`, `Popularity`, `Vote_Count`, `Vote_Average`, `Genre`, etc.
  
---

##  Exploratory Data Analysis (EDA)

### Key Questions Answered:
1. **Most frequent genre**: `Drama`
2. **Genre with highest votes**: `Drama`, `Action`, `Thriller`
3. **Highest popularity movie**: `Spider-Man: No Way Home`
4. **Lowest popularity movie**: `Threads` and `The United States vs. Billie Holiday`
5. **Most active year for releases**: `2020`

### Visualizations:
- Genre distribution count
- Vote average categories
- Release year distribution
- Feature importance plot from ML model

---

##  Data Cleaning & Preprocessing

- Converted `Release_Date` to year format
- Dropped unnecessary columns: `Overview`, `Poster_Url`, `Original_Language`
- Split multiple genres into single values using `.explode()`
- Converted `Vote_Average` into 4 categories:
  - `Popular`, `Average`, `Below_Average`, `Not_Popular`
- One-hot encoded genre features for ML input

---

##  Machine Learning Model

### Model Used:
- `RandomForestClassifier` from `scikit-learn`

### Features Used:
- `Release Year`, `Popularity`, `Vote Count`, `Genre` (One-hot encoded)

### Target:
- Binary classification: **HIT (1)** or **FLOP (0)**

### Performance:
| Metric          | Value |
|-----------------|--------|
| **Accuracy**     | 79.1%  |
| **Precision**    | 63%    |
| **Recall (HIT)** | 38%    |
| **F1-score**     | 48%    |

### Confusion Matrix:
