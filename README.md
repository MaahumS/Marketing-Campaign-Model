# 📈 Marketing Campaign Simulation & Predictive Modeling 
## 📍 Project Overview: 
- This project uses a real company's dataset containing information on the customer base (Age, income, website visits, last purchase, etc.)
- I performed exploratory analysis and used my findings to create a variable that simulates customers' responses to a potential marketing campaign
- I used the real data + simulated data to create a predictive linear regression model and classify customers as responders to campaign and nonresponders

## 💼 Dataset Context:
I sourced this dataset from an old practice assignment in my undergraduate data mining course. 
This dataset contains 2204 rows of real data from a company's customer base

**Key variables:**
- `Age`, `Income`, `Years_Customer`
- `Recency` (days since last purchase)
- `WebVisits_last_Month`
- Purchase types: `Catalog`, `Web`, and `Store`
- **Simulated column**: `Campaign_Response` (1 = responded, 0 = did not respond)

## 🛠️ Tools Used
- **Microsoft Excel** - Data cleaning, EDA, simulating a campaign response variable, visualizations
- **Python** – pandas, scikit-learn, NumPy, matplotlib  
- **Jupyter Notebooks** – Modeling and documentation  
- **VS Code** – IDE for running Python notebooks
  
## 🔍 What I Did
- Performed Exploratory Data Analysis (EDA) in Excel
- Used EDA findings to simulate Campaign_Response variable with nested IF formulas, RANDBETWEEN, and weighting
- Exported file into VS Code
- Created and trained a logistic regression model
- Tested model's accuracy
- Rebalanced model in Excel and created second model
- Tested accuracy again

## 📊 Key EDA Insights
- **Features used to simulate response**: Income, Recency, WebVisits, Years as customer  
- **Overall simulated response rate**: 23%  
- **Highest response rate by income**: $35,000–$70,000 (medium bracket)  
- **Highest response rate by age**: 45–60 years  
- **Responders** made more **web purchases** and used more **promotions/deals**  
- **Outliers** noted: Only 12 customers had income > $100,000

## 🔍 Key Findings from First Model 

**Model Accuracy:** 77.5%

| Confusion Matrix   | Predicted No (0) | Predicted Yes (1) |
|----------------------|------------------|-------------------|
| **Actual No (0)**    | 342              | 0                 |
| **Actual Yes (1)**   | 99               | 0                 |

**Insights:**
- Model predicted “No” for every customer
- Missed all actual responders (0 true positives)
- The data is likely imbalanced
- Accuracy is misleading due to imbalanced data

## 🔍 Key Findings from Second Model

**Model Accuracy:** 48.9%

| Confusion Matrix   | Predicted No (0) | Predicted Yes (1) |
|----------------------|------------------|-------------------|
| **Actual No (0)**    | 112              | 95                |
| **Actual Yes (1)**   | 130              | 104               |

**Insights:**
- Accuracy dropped, but predictions were more balanced
- Captured a meaningful number of responders (104)
- Correctly predicted 112 customers wouldn't respond
- 48.9% accuracy is generally not an acceptable number for most logistic regression models

## ✍️ Results and Reflection
Final logistic regression model's accuracy: ~49%
Second confusion matrix showed improvement but overall model needs additional improvement

This project was created as a way to practice and demonstrate:
- My understanding of data simulation and predictive modeling
- My familiarity with Python libraries Pandas, matplotlib, Scikit-learn, NumPy, etc.
- My familiarity with using Jupyter Notebooks for documentation in VS Code
- My ability to thoughtfully interpret results and remodel real data as needed

## 👥 Author
- Maahum Sattar
