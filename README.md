# 🌍 Global Cost of Living Arbitrage Detector (AI-Powered)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 🚀 Project Overview
**"New York, Bali, or Berlin? Where does your money go further?"**

This project is an **End-to-End Data Science solution** that identifies global market inefficiencies (arbitrage opportunities) by analyzing cost of living versus purchasing power. By scraping real-time data from Numbeo and processing it through an Ensemble Learning pipeline, the model detects cities that are **"Undervalued"** (High Quality of Life, Low Cost) vs. **"Overvalued"**.

---

## 📸 Results & Screenshots

### 1. Global Arbitrage Analysis (Scatter Plot)
*Green bubbles represent "Opportunity Cities" where purchasing power outweighs the cost of living.*
![Scatter Plot](BURAYA_SCATTER_PLOT_RESMINI_YUKLE_VE_LINKINI_KOY.png)

### 2. Opportunity Table (Market Inefficiencies)
*Top cities identified by the AI as having the highest arbitrage potential.*
![Table](BURAYA_TABLO_RESMINI_YUKLE_VE_LINKINI_KOY.png)

---

## 🧠 Technical Architecture

The project follows a rigorous 4-step pipeline:

### 1. Data Mining (Web Scraping)
* Built a custom bot using `BeautifulSoup` and `Pandas` to scrape real-time economic data (Rent, Groceries, Salaries, etc.) for 500+ cities.
* Replaced static CSVs with **dynamic data ingestion**.

### 2. Preprocessing & Feature Engineering
* **Outlier Removal:** Applied statistical clipping (quantile-based) to remove noisy data points.
* **Feature Engineering:** Derived new metrics like `Prosperity_Score` and `Pollution_Impact`.
* **Robust Scaling:** Utilized `RobustScaler` instead of Standard Scaler to handle outliers effectively.

### 3. AI Model (Ensemble Learning)
Instead of relying on a single model, I implemented a **Voting Regressor** combining three powerful algorithms:
* **Gradient Boosting:** To optimize errors and bias.
* **Random Forest:** To reduce variance and overfitting.
* **Extra Trees:** To enhance generalization.

**🏆 Model Performance:**
* **R² Score:** ~80% (High Explainability)
* **MAE:** ~6.0 Points (Low Error Margin)
* **Overfitting:** None (Controlled via Regularization).

### 4. Segmentation (Unsupervised Learning)
Cities are segmented into 4 profiles using `K-Means Clustering`:
* *Elite / Wealthy*
* *Low Purchasing Power*
* *Risky Zones*
* *Balanced / Standard*

---

## 🛠️ Installation & Usage

To run this project on your local machine:

```bash
# 1. Clone the repository
git clone [https://github.com/YOUR_USERNAME/Global-Arbitrage.git](https://github.com/YOUR_USERNAME/Global-Arbitrage.git)

# 2. Install requirements
pip install -r requirements.txt

# 3. Run the application
python main.py