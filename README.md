# 📊 Causal Machine Learning for Marketing Uplift Analysis

## 🚀 Project Overview

This project develops a **causal machine learning framework** to estimate the impact of marketing email campaigns on customer conversion behavior.

Unlike traditional machine learning models that focus on prediction, this project answers a more important question:

> **“Did the campaign actually cause customers to convert?”**

We go beyond average effects to identify:

* Which customers are influenced by the campaign
* How much they benefit
* How to optimize targeting strategies

---

## 🧠 Key Contributions

* Built a complete **causal inference pipeline**
* Estimated **Average Treatment Effect (ATE)** using multiple methods
* Modeled **Individual Treatment Effects (ITE)** for personalized targeting
* Applied **Causal Forests** for non-linear treatment effect estimation
* Developed **uplift-based segmentation** for business decision-making
* Used **SHAP** to interpret drivers of treatment effect
* Simulated **A/B targeting strategies** for ROI evaluation

---

## 📂 Project Structure

```
causal-ml-project/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Baseline_Model.ipynb
│   ├── 03_PSM.ipynb
│   ├── 04_Meta_Learners.ipynb
│   ├── 05_Causal_Forest.ipynb
│   ├── 06_Uplift_Analysis.ipynb
│
├── src/
├── results/
├── reports/
├── README.md
```

---

## 📊 Dataset

* **Hillstrom Email Marketing Dataset**
* ~64,000 customers
* Randomized experiment:

  * Treatment: Email campaign (Mens/Womens)
  * Control: No email
* Outcome: Customer conversion

---

## ⚙️ Methodology

### 1. Exploratory Data Analysis

* Verified randomized treatment assignment
* Compared treatment vs control groups
* Identified potential biases

---

### 2. Baseline Model (Non-Causal)

* Logistic Regression
* Demonstrated that:

  > Prediction ≠ Causation

---

### 3. Propensity Score Matching (PSM)

* Balanced treated and control groups
* Estimated unbiased **Average Treatment Effect (ATE)**

---

### 4. Meta-Learners

#### 🔹 S-Learner

Single model including treatment as a feature

#### 🔹 T-Learner

Separate models for treated and control groups

#### 🔹 X-Learner

Improved estimation using pseudo-outcomes

---

### 5. Causal Forest (Advanced)

* Captures **non-linear treatment effects**
* Estimates **heterogeneous treatment effects (HTE)**
* Provides feature-level causal importance

---

### 6. Uplift Modeling

#### 📈 Uplift Segmentation

* Customers grouped into quartiles based on treatment effect
* Identifies:

  * High-impact users (target)
  * Low-impact users (avoid)

#### 🧪 A/B Simulation

* Evaluated performance of targeting top 20% users
* Demonstrated improved campaign efficiency

---

### 7. Explainability (SHAP)

* Applied SHAP on ITE predictions
* Identified key drivers of treatment effect:

  * Customer purchase history
  * Recency of activity
  * Channel and demographics

---

## 📈 Results

### ✅ Consistent ATE Across Methods

| Method        | ATE     |
| ------------- | ------- |
| PSM           | ~0.0055 |
| T-Learner     | ~0.0050 |
| X-Learner     | ~0.0050 |
| Causal Forest | ~0.0050 |

👉 Strong agreement across models confirms robustness

---

### 🔥 Key Insights

* Email campaign increases conversion by ~**0.5%**
* High-value customers benefit the most
* Targeted campaigns outperform mass campaigns
* Significant heterogeneity in treatment effects

---

## 💡 Business Impact

Instead of sending emails to all users:

👉 Target only high-uplift users
👉 Reduce cost + increase ROI

This framework enables:

* Personalized marketing
* Efficient resource allocation
* Data-driven decision-making

---

## 🧠 Key Takeaways

* Machine Learning ≠ Causal Inference
* Treatment effect varies across individuals
* Personalized targeting is critical for business success
* Explainability is essential for trust and adoption

---

## 🛠️ Tech Stack

* Python
* Scikit-learn
* EconML
* SHAP
* Pandas / NumPy / Matplotlib

---

## 🎯 Future Improvements

* Doubly Robust (DR) Learner
* Qini / AUUC evaluation metrics
* Hyperparameter optimization
* Real-world deployment simulation

---

## 👤 Author

**Dev Sharma**
Data Science | Machine Learning | Causal Inference

---

## ⭐ If you found this useful, consider starring the repo!
