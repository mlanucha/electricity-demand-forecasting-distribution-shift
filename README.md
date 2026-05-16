# Electricity Demand Forecasting Under Distribution Shift

Master's thesis project focused on forecasting electricity demand in Poland using machine learning models and analyzing how model performance changes under unstable conditions such as COVID-19 and war-related disruptions.

## Project Goal

The goal of this project is not only to forecast electricity demand but also to evaluate the robustness of forecasting models under changing data distributions (distribution shift).

Two main experiments are performed:

### Experiment A
Train:
- Calm period

Test:
- COVID period
- War period

Purpose:
- Examine how models trained on stable conditions generalize to crisis situations.

### Experiment B

Train:
- Calm + COVID periods

Test:
- War period

Purpose:
- Evaluate whether adding disturbed data improves model generalization.

---

## Dataset

Source:

- ENTSO-E Transparency Platform

Region:

- Poland

Data characteristics:

- Hourly electricity demand
- Multiple periods:
  - Calm
  - COVID
  - War

---

## Feature Engineering

Features include:

- Hour
- Day
- Month
- Calendar-based variables
- Lag features
- Rolling statistics
- Period labels

---

## Models Used

Current model basket:

1. Linear Regression
2. Random Forest
3. Decision Tree
4. Gradient Boosting
5. K-Nearest Neighbors (KNN)
6. Support Vector Regression (SVR)

---

## Evaluation Metrics

Models are evaluated using:

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)

Metrics are analyzed:

- Overall
- By period

---

## Project Structure

```plaintext
electricity-demand-forecasting-distribution-shift/

├── notebooks/
│   ├── 01_data_acquisition.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03a_train_calm_only.ipynb
│   └── 03b_train_calm_covid.ipynb
│
├── data/
│   ├── raw/
│   └── processed/
│
├── figures/
│
├── thesis/
│
├── models/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Preliminary Findings

Early experiments suggest:

- Tree-based ensemble methods demonstrate stronger robustness under changing conditions.
- Random Forest consistently outperforms simpler baseline models.
- Including COVID-period data in training improves generalization to war-period data.
- Some models appear more sensitive to distribution shifts than others.

---

## Future Work

- Expand literature review
- Compare additional forecasting approaches
- Build result visualizations
- Complete thesis discussion and interpretation

---

## Technologies

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook
- Matplotlib
- Power BI
- ENTSO-E API

---

## Author

Michael Lanucha

Master's Thesis – Applied Computer Science
