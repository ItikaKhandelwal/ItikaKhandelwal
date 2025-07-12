📈 Stock Price Predictor with News Sentiment Analysis 📰
This project builds a machine learning-based stock price prediction model that incorporates both historical price data and real-time news sentiment analysis to improve forecast accuracy. It combines quantitative indicators (moving averages, past prices) with qualitative market sentiment extracted from news headlines.

🔍 Project Overview
Stock market prices are influenced by a mix of technical trends and investor sentiment. While traditional price prediction relies on historical numerical data, this project enhances predictive performance by integrating news sentiment, using Natural Language Processing (NLP) and Machine Learning (ML) techniques.

🎯 Objectives
Collect and process historical stock price data

Scrape financial news headlines

Perform sentiment analysis using VADER (Valence Aware Dictionary and sEntiment Reasoner)

Merge sentiment scores with price data

Train ML models (e.g., Linear Regression, XGBoost) for prediction

Visualize actual vs. predicted prices

🛠️ Tools & Technologies
Category	Tools/Libraries
Programming Language	Python
Data Sources	Yahoo Finance, NewsAPI
Data Handling	pandas, numpy
Visualization	matplotlib, seaborn
Sentiment Analysis	nltk (VADER), optional: FinBERT (Hugging Face)
Machine Learning	scikit-learn, xgboost, keras (optional for LSTM)
IDE / Platform	Google Colab / Jupyter Notebook

📂 Project Structure

├── stock_price_predictor/
│   ├── stock_data_fetch.py       # Fetch stock data using yfinance
│   ├── news_sentiment.py         # Fetch and analyze news sentiment
│   ├── merge_features.py         # Combine technical and sentiment features
│   ├── model_training.py         # ML model training and evaluation
│   ├── prediction_plot.py        # Plot predicted vs actual prices
│   ├── README.md                 # Project documentation
│   └── requirements.txt          # Python dependencies


📊 Features
📉 Stock Data Collection: Automatically fetches OHLC (Open, High, Low, Close) stock data using yfinance.

📰 News Scraping: Uses NewsAPI to gather headlines relevant to the selected stock ticker.

🧠 Sentiment Analysis: VADER assigns compound sentiment scores (−1 to +1) to each headline.

🔄 Feature Merging: Combines sentiment and technical indicators like moving averages.

🤖 Modeling:

Linear Regression (Baseline)

XGBoost Regressor (Advanced)

Optional: LSTM for time series forecasting

📈 Visualization: Shows actual vs predicted stock prices with clear time-series plots.


🚀 How to Run
Install dependencies (recommended in virtualenv or Colab):

`pip install -r requirements.txt`

Fetch historical stock price data:

`import yfinance as yf
data = yf.download('AAPL', start='2023-01-01', end='2023-12-31')`

Fetch news headlines using NewsAPI:

Sign up at newsapi.org and get your API key.


# Replace with your own API key
`url = f"https://newsapi.org/v2/everything?q=AAPL&from=2023-01-01&apiKey=YOUR_API_KEY"`

Run sentiment analysis:

`from nltk.sentiment.vader import SentimentIntensityAnalyzer`

Merge features and train your model:

`model = LinearRegression()
model.fit(X_train, y_train)`

Evaluate and visualize predictions.

✅ Future Improvements
* Integrate FinBERT for domain-specific sentiment (finance)

* Use Twitter or Reddit for real-time social sentiment

* Add macroeconomic indicators (interest rates, CPI)

* Deploy as a Flask web app for interactive use

* Fine-tune LSTM model for long-term forecasting

🤝 Contributors
Your Name – Itika Khandelwal

📄 License
This project is licensed under the MIT License – see the LICENSE file for details.
