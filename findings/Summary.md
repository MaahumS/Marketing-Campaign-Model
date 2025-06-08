# 🧠 Findings Summary

## 1. 📊 Exploratory Data Analysis (EDA)

**Age Group Analysis:**
- Ages 45–60 showed the highest campaign response rate.
- Younger groups (under 30) had very low response.

![Age vs Response](/visuals/ResponsebyAge.png)

**Income Insights:**
- Medium income bracket ($35,000–$70,000) had highest engagement.
- High-income customers could be skewing data (only 12 customers had income over 100,000)

![Income vs Response](/visuals/ResponsebyIncome.png)

**Purchase Behavior:**
- Responders had more web purchases and recent activity.
- Website visits last month correlated strongly with response.

![Website visits vs Response](/visuals/ResponsebyWebvisits.png)
![Purchase Type vs Response](/visuals/PurchasesbyType.png)

---

## 2. 🧪 Simulating Campaign Response

Created a formula combining:
- Income Bracket
- Recency of Last Purchase
- Website Visits Last Month
- Years as a Customer

Used nested `IF` logic + `RANDBETWEEN()` in Excel for variability and business realism.

### 💰 Income Brackets

| Bracket   | Criteria                        |
|-----------|---------------------------------|
| Highest   | `x ≥ 100,000`                   |
| High      | `70,000 < x < 100,000`          |
| Medium    | `35,000 ≤ x ≤ 70,000`           |
| Low       | `x < 35,000`                    |

---

### ⏳ Recency (Days Since Last Purchase)

| Activity Level     | Criteria              | Notes                                  |
|--------------------|-----------------------|----------------------------------------|
| Highly Active      | `x ≤ 25`              | Purchased within last 25 days          |
| Moderately Active  | `25 < x ≤ 50`         | Last purchase was 26–50 days ago       |
| Low Activity       | `50 < x ≤ 75`         | Last purchase was 51–75 days ago       |
| Inactive           | `x > 75`              | No purchase in over 75 days            |

---

### 🌐 Website Visits Last Month

| Engagement Level   | Criteria              | Notes                                    |
|--------------------|-----------------------|------------------------------------------|
| Highly Active      | `x > 10`              | Over 10 visits in last 30 days           |
| Moderately Active  | `6 < x ≤ 10`          | Between 6 and 10 visits                  |
| Low Activity       | `3 ≤ x ≤ 6`           | Between 3 and 6 visits                   |
| Inactive           | `x < 3`               | Fewer than 3 visits                      |

---

### 🧾 Customer Loyalty (Years as a Customer)

| Loyalty Level       | Criteria              | Notes                                       |
|---------------------|-----------------------|---------------------------------------------|
| Highly Loyal        | `x = 8`               | 8 years as a customer                       |
| Moderately Loyal    | `x = 7`               | 7 years as a customer                       |
| Low Loyalty         | `x = 6`               | 6 years as a customer                       |

> ⚠️ *Note: The dataset only includes customers with 6, 7, or 8 years of history.*

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
- Being able to interpret results in-depth is KEY (high accuracy doesn't = good model)
- Simulation helped apply realistic business logic to raw data
- EDA was crucial in selecting predictive features

---

## 👩‍💻 Next Steps (if extended)
- Intruduce weights in calcuation of simulated campaign response
- Exlcude possible outliers (high income)
- Explore Decision Trees or Random Forest models 
- A/B test campaign strategies on high-potential segments
