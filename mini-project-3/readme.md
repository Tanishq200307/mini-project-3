# Mall Customer Segmentation & Anomaly Detection

## Project Overview

This project performs an end-to-end **unsupervised learning analysis** on a mall customer dataset to uncover meaningful customer segments, validate them using dimensionality reduction techniques, and identify unusual customer behaviors using anomaly detection.

By integrating **K-Means clustering**, **PCA**, **t-SNE**, and **Isolation Forest**, the analysis moves beyond surface-level insights to provide **actionable business recommendations** grounded in data.

---

## Objectives

- Segment mall customers based on demographic and behavioral features
- Validate clustering results using dimensionality reduction
- Detect anomalous customers with unusual spending or income patterns
- Integrate findings into cohesive, real-world business insights

---

## Dataset

**Source:** Mall Customers Dataset  
**Size:** 200 customers  
**Features:**

| Feature | Description |
|------|------------|
| CustomerID | Unique customer identifier |
| Gender | Customer gender |
| Age | Customer age |
| Annual Income (k$) | Annual income in thousands |
| Spending Score (1–100) | Spending behavior score |

---

## Project Structure
```
mini-project-3/
├── data/
│   └── Mall_Customers.csv
├── notebooks/
│   └── analysis.ipynb
├── .gitignore
├── README.md
└── requirements.txt

```

### Install Dependencies
```bash
pip install -r requirements.txt
```

---

## Methodology

### 1. Data Preprocessing
- Encoded categorical variable (Gender)
- Removed non-informative identifier (CustomerID)
- Standardized all features using `StandardScaler` (critical for distance-based models)

---

### 2. Clustering (K-Means)
- Used **Elbow Method** and **Silhouette Score** to evaluate optimal cluster counts
- Selected **K = 5** for best balance between statistical quality and business interpretability
- Generated distinct customer segments based on age, income, and spending behavior

---

### 3. Dimensionality Reduction

#### Principal Component Analysis (PCA)
- Reduced data to 2 dimensions
- Explained ~60% of total variance
- Confirmed that clusters align with dominant linear structure in the data
- Revealed partial overlap between some high-value segments

#### t-SNE
- Captured non-linear and local relationships
- Showed clearer separation between behaviorally distinct clusters
- Revealed that some clusters represent closely related sub-segments rather than entirely separate groups

---

### 4. Anomaly Detection (Isolation Forest)
- Tested multiple contamination levels
- Selected **5% contamination**, identifying **10 anomalous customers**
- Anomalies were distributed across all clusters
- Highlighted exceptional customers rather than a single anomalous segment

---

## Key Findings

### Customer Segments
The analysis identified five meaningful customer segments, including:
- High-income, low-spending customers
- Young, high-spending customers
- Premium shoppers with strong purchasing power
- Budget-conscious older customers
- Young, value-oriented shoppers

### Validation
- PCA confirmed that clusters reflect real variance in the data
- t-SNE showed strong local consistency and revealed sub-structure among premium segments

### Anomalies
- Anomalous customers exist within every segment
- These represent high-impact individuals (e.g., VIPs or disengaged high-income customers)
- Should be handled with personalized strategies rather than ignored

---

## Business Recommendations

- **Personalize marketing** for premium and anomalous customers
- **Target high-income, low-spending segments** with engagement campaigns
- **Flag anomalies for manual review** or A/B testing
- Use clustering as a foundation for **customer segmentation strategies**, while anomaly detection identifies exceptions that need special attention

---

## Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn  
  - KMeans
  - PCA
  - t-SNE
  - Isolation Forest

---

## Authors

- **Tanishq Rawat** — Analysis & Exploratory Data Analysis (EDA)
- **Brendan Zapf** — Analysis & Final Report

---


## 🚀 How to Run the Project
Clone the repository:
   ```bash
   git clone https://github.com/Tanishq200307/mini-project-2
   ```

## Notes

This project demonstrates how combining multiple unsupervised learning techniques produces deeper insights than using any single method in isolation. The integrated approach enables both **segment-level strategy** and **individual-level decision-making**.


