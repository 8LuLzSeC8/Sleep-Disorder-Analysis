# 💤 Sleep Disorder and Lifestyle Analysis

This project focuses on analyzing and predicting sleep disorders using various data mining techniques in Rapidminer. The dataset includes diverse physiological and lifestyle parameters like the patient’s daily activity, profession, medical conditions etc. that potentially influence sleep quality and sleep-related health conditions. The goal is to leverage these variables to identify patterns, correlations, and risk factors associated with sleep disorders, thereby enabling proactive interventions and better health outcomes.


## 🧾 Executive Summary and Key Findings

This project focuses on **analyzing and predicting sleep disorders** using various **data mining and machine learning techniques**.  
The dataset includes diverse physiological and lifestyle parameters such as daily activity, profession, and medical conditions that potentially influence sleep quality and sleep-related health outcomes.

The goal is to leverage these variables to:
- Identify **patterns, correlations, and risk factors** associated with sleep disorders.
- Build an **optimized prediction model** to classify individuals as having or not having a sleep disorder.
- Perform **clustering** to identify specific target profiles for intervention.

This model was applied to unlabeled data from an **insurance company** to predict the likelihood of sleep disorders, enabling:
- Identification of **high-risk individuals**.
- Development of **targeted health strategies** and **risk management optimization**.

---

### 🔍 Significant Predictors of Sleep Disorders

- **Diastolic Blood Pressure (BP)**
- **Heart Rate**
- **Sleep Duration**
- **Daily Steps**
- **Stress Levels**

These were the most influential factors in predicting disorders like **Insomnia** and **Sleep Apnea**.

---

### 🌳 Decision Tree Model

| Metric | Value |
|:--|:--|
| **Accuracy** | 92.15% |
| **Precision (Sleep Apnea)** | 93.40% |
| **Recall (Sleep Apnea)** | 93.05% |
| **Precision (Insomnia)** | 93.40% |
| **Recall (Insomnia)** | 89.18% |

✅ Strong interpretability makes it ideal for healthcare and insurance use.

---

### 🧠 Neural Network Model

| Metric | Value |
|:--|:--|
| **Accuracy** | 95.19% |
| **Precision (Insomnia)** | 94.95% |
| **Recall (Insomnia)** | 95.90% |
| **Precision (Sleep Apnea)** | 94.66% |
| **Recall (Sleep Apnea)** | 96.55% |

⚠️ Higher accuracy but less interpretability — better for research and advanced prediction.

---

### 📊 Clustering Insights

Clustering revealed subgroups such as:
- **High stress + low physical activity** → increased risk of sleep disorders.
- These insights help design **targeted interventions** and **personalized wellness plans**.

---

### 🧠 Key Behavioral Observations

- **Higher physical activity** → better sleep quality.  
- **Increased stress** → reduced sleep duration.  
- Stress management should be a key intervention area.

---

## 💼 Business Opportunities

Sleep disorders are linked to **hypertension, obesity, diabetes, cardiovascular, and mental health issues** — making early detection a business and public health priority.

### 1. Insurance and Risk Management
- Identify **high-risk policyholders**.
- Offer **customized health interventions**.
- Adjust **premium rates** to reduce claims.

### 2. Healthcare and Wellness
- Develop **targeted programs** (sleep therapy, stress management, fitness).
- Enable **preventive health strategies**.

### 3. Corporate Productivity
- Use predictive insights to enhance **employee wellness programs**.
- Reduce **absenteeism** and **boost performance**.

#### 🏢 Example Companies
- **Headspace** – mindfulness & sleep programs  
- **ResMed** – sleep apnea management solutions  
- **Hatch** – smart sleep and sound technology

---

## 🎯 Purpose of the Data Mining Task

| Technique | Purpose |
|:--|:--|
| **Classification** | Predict individuals likely to have a sleep disorder for early detection and intervention. |
| **Clustering** | Group individuals into distinct profiles to uncover patterns and design targeted health programs. |

Together, these techniques enable **personalized recommendations** and **data-driven strategies** for improving sleep health.

---

## 📚 Data for Analysis

**Dataset Name:** Sleep Health Data  
**Source:** [Kaggle – Sleep Health Data (Sampled)](https://www.kaggle.com/datasets/imaginativecoder/sleep-health-data-sampled)  
**Total Records:** 12,000  

### 🧩 Columns Overview

| Type | Columns |
|:--|:--|
| **Numerical** | Age, Sleep Duration, Quality of Sleep, Physical Activity Level, Stress Level, Systolic BP, Diastolic BP, Heart Rate, Daily Steps |
| **Categorical** | Gender, Occupation, BMI Category, Sleep Disorder |
| **Identifier** | Person ID |

### 🧠 Target Variable
- **Sleep Disorder:** {Healthy, Insomnia, Sleep Apnea}

---

## 🧹 Data Cleaning

- **BMI Category:** Merged “Normal” and “Normal weight” to standardize categories.
- **Blood Pressure:** Split combined “Systolic/Diastolic” into two numeric columns for accurate modeling.

---

## 🧩 Data Selection

The following columns were selected for modeling:

> Gender, Age, Occupation, Sleep Duration, Quality of Sleep, Physical Activity Level, Stress Level, BMI Category, Systolic BP, Diastolic BP, Heart Rate, Daily Steps, and Sleep Disorder (target).

---

## 🧮 Model Assessment

### 🔹 Decision Tree (Classification)

**Parameters:**
- Criterion: `gain_ratio`
- Max Depth: `20`
- Confidence: `0.15`
- Min Gain: `0.15`

**Results:**

| Metric | Value |
|:--|:--|
| Accuracy | 92.15% ± 0.58% |
| Kappa | 0.882 ± 0.009 |

**Precision & Recall:**

| Class | Precision | Recall |
|:--|:--|:--|
| Healthy | 89.82% | 94.23% |
| Sleep Apnea | 93.40% | 93.05% |
| Insomnia | 93.40% | 89.18% |

**Advantages:**
- Highly interpretable
- Handles mixed data types

**Disadvantages:**
- Prone to overfitting; requires pruning.

---

### 🔹 Neural Network (Classification)

**Parameters:**
- Training cycles: `800`
- Learning rate: `0.01`
- Momentum: `0.9`

**Results:**

| Metric | Value |
|:--|:--|
| Accuracy | 95.19% ± 0.54% |
| Kappa | 0.928 ± 0.008 |

**Precision & Recall:**

| Class | Precision | Recall |
|:--|:--|:--|
| Healthy | 96.01% | 93.12% |
| Sleep Apnea | 94.66% | 96.55% |
| Insomnia | 94.95% | 95.90% |

**Advantages:**
- Excellent accuracy and ability to model nonlinear relationships.

**Disadvantages:**
- Less interpretable.
- Computationally intensive.

---

### ⚖️ Model Comparison

| Model | Accuracy | Kappa | Interpretability |
|:--|:--|:--|:--|
| Decision Tree | 92.15% | 0.882 | ✅ High |
| Neural Network | 95.19% | 0.928 | ⚠️ Low |

**Selected Model:**  
✅ **Decision Tree** — balances interpretability, accuracy, and business usability.

---

## 🔢 Model Application (Unlabeled Data)

Used to predict **3,000 unlabeled records** from an insurance company:

| Class | Count |
|:--|:--|
| Healthy | 1045 |
| Sleep Apnea | 996 |
| Insomnia | 959 |

Confidence levels were analyzed to refine predictions and identify potentially misclassified “healthy” individuals.

---

## 🔸 Clustering (Unsupervised Learning)

**Purpose:** Identify groups with similar patterns in lifestyle and health metrics.

**Process:**
- Mixed Euclidean distance for mixed data types.
- Normalized numerical features to ensure equal weighting.

**Cluster Profiles:**

| Cluster | Description |
|:--|:--|
| **0** | Older females, high activity (Nurses), overweight BMI, higher HR → mostly Sleep Apnea. |
| **1** | Younger group, balanced lifestyle (Teachers, Sales), moderate stress, healthy sleep. |
| **2** | Mid-age professionals (Engineers), high stress, low sleep, low steps → Insomnia. |

---

## 🧾 Conclusions

### 🌳 Decision Tree Model
- Accuracy: **92.15%**, Kappa: **0.882**
- Key attributes: Diastolic BP, Heart Rate, BMI
- ✅ Best balance of interpretability and performance.

### 🧠 Neural Network Model
- Accuracy: **95.19%**, Kappa: **0.928**
- Key attributes: Heart Rate, Sleep Duration, Daily Steps
- ⚠️ High performance but poor interpretability.

### 🌀 Clustering Model
- Reveals behavioral subgroups for targeted wellness programs.
- Supports classification insights with hidden patterns.

---

## 💡 Business and Healthcare Implications

- Enables **early detection** of sleep disorders.
- Supports **risk-based insurance pricing**.
- Guides **personalized treatment** and **wellness plans**.

---

## 📈 Recommendations to Management

1. **Adopt the Decision Tree Model**
   - Reliable (92.15% accuracy) and interpretable for operational deployment.

2. **Use Neural Networks for Research**
   - For high-accuracy or experimental validation studies.

3. **Leverage Clustering for Targeted Programs**
   - Focus wellness initiatives on clusters with higher risk (e.g., Nurses, Engineers).

4. **Prioritize High-Risk Conditions**
   - Emphasize early interventions for **Insomnia** and **Sleep Apnea**.

5. **Track Key Predictors**
   - Regularly monitor **Diastolic BP, Heart Rate, Sleep Duration, Daily Steps** for early alerts.

---

## 🧩 Tools & Technologies

- **Python**, **RapidMiner / AI Studio**
- **Excel** (Data Cleaning & Preprocessing)
- **Machine Learning Techniques:** Decision Tree, Neural Network, Clustering
