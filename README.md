# 📈 Tesla Stock Price Prediction using Machine Learning

This project predicts Tesla's stock **closing price** using historical market data and Machine Learning techniques.  
It demonstrates a complete ML workflow including data analysis, feature engineering, model training, evaluation, and prediction.

---

## 🚀 Project Overview

The goal of this project is to build a regression model that can predict the **next day's closing price** of Tesla stock based on:

- Opening price
- Highest and lowest prices
- Trading volume
- Technical indicators
- Moving averages
- Price change features

A Linear Regression model is trained and evaluated to achieve high prediction accuracy.

---

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Scikit-learn

Joblib

---

## 📂 Dataset

- Source: Public Tesla stock dataset (CSV format)
- Records: 254 rows
- Features:

| Column   | Description               |
|----------|---------------------------|
| Date     | Trading date              |
| Open     | Opening price             |
| High     | Highest price             |
| Low      | Lowest price              |
| Close    | Closing price (Target)    |
| Volume   | Trading volume             |

---

## ⚙️ Feature Engineering

Additional features were created to improve model performance:

- `Daily_Change` = Close - Open  
- `High_Low_Diff` = High - Low  
- `Pct_Change` = Percentage price change  
- `MA_5` = 5-day moving average  
- `MA_10` = 10-day moving average  

These features help the model understand short-term trends.

---

## 📊 Exploratory Data Analysis (EDA)

- Price trend visualization
- Volume analysis
- Outlier detection using boxplots
- Correlation analysis

EDA was performed to understand patterns and ensure data quality.

---

## 🤖 Machine Learning Model

- Algorithm: Linear Regression
- Library: Scikit-learn
- Train-Test Split: 80% / 20% (Time-based split)

---

## 📈 Model Performance

The trained model achieved:

- **RMSE:** ~5.4  
- **R² Score:** ~0.95  

This indicates strong predictive performance on test data.

---

## 🔮 Sample Prediction

Example input:

```python
{
  "Open": 340,
  "High": 345,
  "Low": 338,
  "Volume": 75000000,
  "Daily_Change": 2.1,
  "High_Low_Diff": 7,
  "MA_5": 335,
  "MA_10": 330,
  "Pct_Change": 0.6
}
```

## 📁 Project Structure

```Structure
Tesla-Stock-Prediction/
├── data/
│   └── `TSLA_Stock.csv` (Raw datasets)
├── notebook/
│   └── `tesla_analysis.ipynb`
│   └── `predict.ipynb`
├── model/
│   └── `tesla_price_model.pkl` (Today Closing Prediction)
│   └── `future_price_model.pkl`  (Tomorrow Closing Prediction)
├── `README.md`
└── `requirements.txt`
```

## 💻 Installation & Local Setup

Follow these steps to run this project on your local machine.

1️⃣ Clone the Repository
```bash
git clone https://github.com/Vishnu-Codebase/tesla_stock_predition.git
```

2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

3️⃣ Train the Model

Run all cells in:
```autohotkey
tesla_analysis.ipynb
```
To get prediction today and tomorrow run this file
```autohotkey
predict.ipynb
```