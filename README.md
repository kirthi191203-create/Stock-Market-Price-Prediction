📈 Tesla Stock Price Prediction
Deep Learning-based Time Series Forecasting using Stacked LSTM
📌 Overview
A deep learning project that predicts Tesla (TSLA) stock closing prices using a Stacked LSTM neural network trained on 14 years of historical market data (2010–2024).

The model uses a 60-day rolling window to learn sequential price patterns and forecast future closing prices — with real future price prediction implemented at the end.

🎯 Key Highlights
📅 3,637 days of Tesla historical stock data (2010–2024)
🔁 60-day rolling window for sequence modeling
🧠 Stacked LSTM architecture with 2 LSTM layers + Dense layers
📉 RMSE: 15.87 — evaluated against actual test prices
🔮 Future price forecasting — predicts next day closing price
📊 Actual vs Predicted price visualization
🛠️ Tech Stack
Category	Tools
Language	Python
Deep Learning	TensorFlow, Keras
Data Processing	Pandas, NumPy
Preprocessing	MinMaxScaler (Scikit-learn)
Visualization	Matplotlib
Environment	Google Colab
🧠 Model Architecture
Input Shape: (60, 1)  →  60-day sequence of closing prices

LSTM  (units=50, return_sequences=True)
LSTM  (units=50, return_sequences=False)
Dense (units=25)
Dense (units=1)   →  Predicted closing price

Optimizer : Adam
Loss      : Mean Squared Error
📊 Training Results
Phase	Epochs	Batch Size	Final Loss
Phase 1	10	64	0.000267
Phase 2	20	64	0.000039
RMSE on test data: 15.87

⚙️ How It Works
Load Data — Tesla stock CSV with Open, High, Low, Close, Volume columns
Preprocess — Extract Close price, apply MinMaxScaler (0 to 1)
Sequence Creation — Build 60-day rolling windows for X, next day for y
Train/Test Split — 80% training, 20% testing
Model Training — Stacked LSTM trained on sequence data
Evaluation — RMSE calculated on test predictions
Visualization — Actual vs Predicted prices plotted
Future Forecast — Last 60 days used to predict next closing price
🔮 Sample Prediction
Predicted TSLA closing price for 2024-11-30: $371.70
📁 Project Structure
stock-price-prediction/
│
├── stock_prediction.ipynb   # Main Colab notebook
├── TESLA.csv                # Historical stock data (2010–2024)
└── README.md
📦 Requirements
tensorflow
keras
pandas
numpy
scikit-learn
matplotlib
Install with:

pip install tensorflow pandas numpy scikit-learn matplotlib
📈 Dataset
Field	Details
Source	Yahoo Finance — TSLA
Period	2010 – 2024
Rows	3,637 trading days
Target Column	Close Price
