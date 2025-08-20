# 🚜 Predicting the Sale Price of Bulldozers using Machine Learning

## 📌 Project Overview
This project demonstrates an **machine learning regression task** using the Kaggle **Bluebook for Bulldozers** dataset.  
The goal is to predict the **future sale price of bulldozers** given their characteristics and historical sales data.

---

## 🛠 Approach

### 1. Problem Definition
How well can we predict the future sale price of a bulldozer, given its characteristics and previous examples of similar bulldozer sales?

---

### 2. Data
The dataset comes from Kaggle’s [Bluebook for Bulldozers Competition](https://www.kaggle.com/competitions/bluebook-for-bulldozers).  

The competition provides three datasets:
- **Train.csv** → Training set (data through the end of 2011)  
- **Valid.csv** → Validation set (January 1, 2012 – April 30, 2012)  
- **Test.csv** → Test set (May 1, 2012 – November 2012, used for final leaderboard)  

A **data dictionary** is also provided by Kaggle and can be found in the `data/` folder.

---

### 3. Evaluation
The official evaluation metric is **RMSLE (Root Mean Squared Logarithmic Error)** between the actual and predicted auction prices.

Mathematically:

\[
RMSLE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} ( \log(y_i + 1) - \log(\hat{y_i} + 1))^2 }
\]

Where:
- \(y_i\) = actual sale price  
- \(\hat{y_i}\) = predicted sale price  

---

### 4. Features
The dataset contains a variety of features related to bulldozer sales, including:
- **SalesID** – Unique identifier  
- **SalePrice** – Target variable (what we want to predict)  
- **MachineID** – Unique machine identifier  
- **ModelID** – Unique model identifier  
- **YearMade** – Year the bulldozer was made  
- **ProductGroup** – Category of the bulldozer  
- **Enclosure, Hydraulics, Engine details** – Machine specifications  
- **SaleDate** – Date of sale  

For a detailed explanation, refer to the **data dictionary** provided in the dataset.

---

## 📊 Workflow
1. Data loading and exploration  
2. Handling missing values  
3. Feature engineering (parsing dates, categorical encoding, extracting useful features)  
4. Model selection (Baseline → Random Forest → other regressors)  
5. Training and evaluation using **RMSLE**  
6. Hyperparameter tuning  
7. Final model deployment  

---

username/bulldozer-price-prediction-ml.git
   cd bulldozer-price-prediction-ml
