# 🧠 Findings Summary

## 1. 📊 Exploratory Data Analysis (EDA)

**Age Group Analysis:**
- Ages 45–60 showed the highest campaign response rate.
- Younger groups (under 30) had very low response.

![Age vs Response](visuals/ResponsebyAge.png)

**Income Insights:**
- Medium income bracket ($35,000–$70,000) had highest engagement.
- High-income customers were underrepresented (possible outliers).

**Purchase Behavior:**
- Responders had more web purchases and recent activity.
- Website visits last month correlated strongly with response.

![Age vs Response](./eda-visuals/age_vs_response.png)

---

## 2. 🧪 Simulating Campaign Response

Created a formula combining:
- Income Bracket
- Recency of Last Purchase
- Website Visits Last Month
- Years as a Customer

Used nested `IF` logic + `RANDBETWEEN()` in Excel for variability and business realism.

---

## 3. 🤖 Model Performance

### First Model
- Accuracy: 77.5%
- Misleading due to class imbalance (predicted all "No")

### Second Model
- Accuracy: 48.9%
- Captured both responders and non-responders
- Tradeoff: lower accuracy, higher balance

---

## 4. 🔍 Key Takeaways
- Accuracy alone isn't a reliable metric (especially with imbalanced classes)
- Simulation helped apply realistic business logic to raw data
- EDA was crucial in selecting predictive features

---

## 👩‍💻 Next Steps (if extended)
- Try SMOTE or class weights instead of manual rebalancing
- Explore tree-based models (e.g., Random Forest)
- A/B test campaign strategies on high-potential segments
