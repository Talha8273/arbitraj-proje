# 🌍 Global Life Analyzer: AI-Powered City Decision Engine

**Global Life Analyzer** is a sophisticated data science project designed to find the optimal balance between cost of living, safety, and quality of life for digital nomads, expats, and investors.

Unlike simple cost comparators, this tool uses a **Weighted Decision Matrix** and **Machine Learning (Voting Regressor)** to identify "undervalued" cities—places that offer high living standards for a fraction of the expected price.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Production-green)
![Data](https://img.shields.io/badge/Data-Numbeo-orange)

## 🎯 Project Goal
To answer the question: *"Where can I live the best life for the most reasonable price?"*

This tool scrapes real-time data from Numbeo, processes it through a custom-built algorithm, and segments cities based on a **"Life Score"** that prioritizes human needs over simple luxury.

## ⚙️ How It Works

The system operates in three main stages:

### 1. Data Collection & Engineering
Real-time data is scraped regarding:
* Cost of Living & Purchasing Power
* Safety & Healthcare Quality
* Climate, Pollution, and Traffic
* *External Datasets:* Internet Speeds (Mbps), English Proficiency, and Cultural Richness Scores.

### 2. The "Life Score" Algorithm (The Logic)
Cities are ranked based on a **Human-Centric Weighted Formula** designed to prioritize financial freedom and safety while maintaining a high quality of life:

| Metric | Weight | Description |
| :--- | :--- | :--- |
| **💰 Financial Freedom** | **35%** | Purchasing Power & Cost of Living. (Prioritizes affordable luxury). |
| **🛡️ Safety** | **15%** | Crime index and general safety. (Non-negotiable). |
| **🏥 Healthcare** | **15%** | Quality and accessibility of medical services. |
| **🎭 Culture** | **10%** | Museums, history, and social vibrancy. |
| **🚗 Environment** | **9%** | Low traffic congestion and high air quality. |
| **☀️ Climate** | **8%** | Weather comfort index. |
| **📶 Internet** | **5%** | Digital infrastructure speed. |
| **🗣️ Language** | **3%** | English proficiency ease. |

### 3. AI Price Prediction (The Arbitrage)
The project uses a **Voting Regressor** (combining `GradientBoostingRegressor` and `RandomForestRegressor`) to predict the "Fair Price" of a city based on its quality metrics.
* **Arbitrage Opportunity:** If the *Predicted Price* is higher than the *Actual Cost*, the city is considered a "Hidden Gem" (Undervalued).

## 🚀 Technologies Used
* **Python:** Core logic.
* **Pandas & NumPy:** Data manipulation and vectorization.
* **Scikit-Learn:** Machine Learning pipeline (Preprocessing, Scaling, Regression).
* **Plotly Express:** Interactive data visualization.
* **BeautifulSoup (bs4):** Web scraping.

## 📊 Outputs

When you run the script, it generates two key files:

1.  **`Global_Life_Project_Final.xlsx`**: A comprehensive, filterable Excel dataset containing all calculated metrics (Social Vibrancy, Life Score, Arbitrage Gap, etc.).
2.  **`Global_Analiz_Grafigi.html`**: An interactive scatter plot.
    * *X-Axis:* AI Predicted Price (Fair Value)
    * *Y-Axis:* Actual Market Price
    * *Bubble Size:* Life Score
    * *Color:* Arbitrage Opportunity (Green = Good Deal)

## 📦 Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Talha8273/global-life-analyzer.git](https://github.com/Talha8273/global-life-analyzer.git)
    cd global-life-analyzer
    ```

2.  **Install requirements:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the analyzer:**
    ```bash
    python main.py
    ```
    *The script will automatically scrape the latest data, train the model, and open the results in your browser/Excel.*

## 📈 Future Improvements
* [ ] Integration of Visa/Passport friendliness filters.
* [ ] NLP analysis of city reviews for sentiment analysis.
* [ ] Historical trend analysis to predict future price hikes.

---
*Created by [Talha Cürmen]