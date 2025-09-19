# Revenue Forecasting with DNN, CNN, and Transformer

This repository explores the application of **deep learning models** to predict monthly revenue of Taiwanese listed companies. It extends previous work with tree-based models (Random Forest, XGBoost) by introducing **DNN**, **CNN**, and **Transformer architectures**.

---

## Project Structure
- `revenue_forecasting_dnn_cnn_transformer.ipynb` : Jupyter Notebook with implementation and experiments.
- `revenue_forecasting_dnn_cnn_transformer.pdf` : Full report (in Chinese) with results, figures, and discussion.

---

## Research Overview

### Objectives
1. Forecast monthly revenue for **2020 (Jan–Dec)** using DNN, CNN, and Transformer models.
2. Compare results with:
   - **2018 predictions** (earlier period, more stable)
   - **Tree-based models** from HW3 (Random Forest, XGBoost)
3. Evaluate performance using **RMSE** and **MAE**.
4. Analyze **semiconductor industry** performance and model robustness to shocks.

---

## Methodology
- **Models:**
  - Deep Neural Network (DNN)
  - Convolutional Neural Network (CNN)
  - Transformer
- **Preprocessing:**
  - Time-series formatting
  - Standardization (deflation) to reduce outlier effects and improve stability
- **Evaluation Metrics:**
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)

---

## Key Findings
- **DNN and Transformer outperform CNN**, which is less suited for non-visual sequential data.
- **Normalization improves accuracy** across all models.
- **Important features:** recent lags (t-1, t-2, t-3) and seasonal lags (t-12, t-13).
- **Best models:** DNN and Transformer in Aug–Sep 2020, capturing recent revenue momentum.
- **Worst models:** CNN and Transformer in late 2020, affected by **COVID-19 impacts** and **Huawei semiconductor sanctions**.
- Compared to HW3 (Random Forest & XGBoost):
  - **Deep learning models (DNN, Transformer) achieved higher accuracy**, while CNN underperformed.

---

## Semiconductor Industry Analysis
- Restricting data to the **semiconductor sector (129 companies)** improved model accuracy.
- Short-term lags (t-1 to t-4) are more influential than long-term lags.
- External shocks (COVID-19 in April 2020, Huawei ban in September 2020) created prediction difficulties.

---

## Environment & Dependencies
- Python 3.9+
- Jupyter Notebook
- Libraries:
  - `pandas`, `numpy`
  - `scikit-learn`
  - `tensorflow` / `keras`
  - `matplotlib`, `seaborn`

Install dependencies:
```bash
pip install -r requirements.txt
