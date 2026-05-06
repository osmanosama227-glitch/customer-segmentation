# 🛍️ Customer Segmentation using Clustering
BY:Osman Osama
> Comparing **K-Means** vs **Agglomerative Hierarchical Clustering** on Mall Customer data

---

## 📌 Project Overview

This project applies unsupervised machine learning techniques to segment mall customers based on their **Annual Income** and **Spending Score**. The goal is to identify distinct customer groups that can guide targeted marketing strategies.

Two clustering algorithms are implemented and compared:
- **K-Means Clustering** — partition-based, fast, scalable
- **Agglomerative Hierarchical Clustering** — bottom-up, dendrogram-driven

---

## 📂 Repository Structure

```
customer-segmentation/
│
├── notebooks/
│   └── Customer_Segmentation_Clustering.ipynb   # Main analysis notebook
│
├── data/
│   └── Mall_Customers.csv                        # Dataset (place here before running)
│
├── images/                                        # Auto-generated plots
│   ├── elbow_method.png
│   ├── silhouette_method.png
│   ├── kmeans_income_spending.png
│   ├── kmeans_age_spending.png
│   ├── dendrogram.png
│   ├── agg_income_spending.png
│   ├── agg_age_spending.png
│   └── comparison_plot.png
│
├── requirements.txt
└── README.md
```

---

## 📊 Dataset

**Mall Customer Segmentation Data**  
Source: [Kaggle — Mall Customers Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

| Feature | Description |
|---|---|
| `CustomerID` | Unique customer identifier |
| `Gender` | Male / Female |
| `Age` | Customer age |
| `Annual Income (k$)` | Annual income in thousands of USD |
| `Spending Score (1-100)` | Score assigned by the mall (1 = low, 100 = high) |

> **Features used for clustering:** `Annual Income (k$)` and `Spending Score (1-100)`

---

## ⚙️ Methodology

### Step 1 — Determine Optimal K
Two methods are used to confirm the ideal number of clusters:

| Method | Optimal K Found |
|---|---|
| Elbow Method (Inertia/WCSS) | **5** |
| Silhouette Score | **5** |
| Dendrogram Cut (Agglomerative) | **5** |

All three methods converge on **K = 5**, confirming the choice.

### Step 2 — Apply Clustering
- **K-Means** with `k-means++` initialization, `random_state=42`
- **Agglomerative** with Ward linkage, 5 clusters

### Step 3 — Evaluate & Compare
Silhouette scores are computed for both algorithms on the same data.

---

## 🏆 Results

### Algorithm Comparison

| Algorithm | Pros | Cons |
|---|---|---|
| **K-Means** | Fast, scalable, clear centroids | Sensitive to outliers, requires K upfront |
| **Agglomerative** | No K needed initially, hierarchical view | Slower on large data, no centroid info |

> **K-Means achieves a slightly higher Silhouette Score** on this dataset, producing well-separated and visually distinct clusters.

### 🧩 Customer Segments Identified

| Cluster | Income | Spending | Profile | Marketing Strategy |
|---|---|---|---|---|
| 0 | Low | Low | Careful customers | Price-sensitive promotions |
| 1 | Low | High | Impulsive buyers | Deals & loyalty programs |
| 2 | Medium | Medium | Average customers | Standard campaigns |
| 3 | High | Low | Potential savers | Exclusive & premium offers |
| 4 | High | High | VIP targets ⭐ | Premium marketing |

---

## 🖼️ Key Visualizations

| Plot | Description |
|---|---|
| Elbow Method | Inertia vs K to find the "elbow" |
| Silhouette Method | Score vs K to confirm optimal clusters |
| K-Means Scatter (Income vs Spending) | Clusters + centroids |
| K-Means Scatter (Age vs Spending) | Age-based segmentation |
| Dendrogram | Hierarchical view of cluster merging |
| Agglomerative Scatter (Income vs Spending) | Comparison with K-Means |
| Side-by-Side Comparison | K-Means vs Agglomerative final view |

---

## 🚀 Getting Started

### Prerequisites
Make sure you have Python 3.8+ installed.

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/customer-segmentation.git
cd customer-segmentation
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add the dataset
Download `Mall_Customers.csv` from [Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) and place it in the `data/` folder.

### 4. Run the notebook
```bash
jupyter notebook notebooks/Customer_Segmentation_Clustering.ipynb
```

Or open it directly in [Google Colab](https://colab.research.google.com/).

---

## 🛠️ Technologies Used

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

| Library | Purpose |
|---|---|
| `pandas` | Data loading & manipulation |
| `numpy` | Numerical operations |
| `scikit-learn` | K-Means, Agglomerative, Silhouette Score |
| `scipy` | Dendrogram & linkage |
| `matplotlib` | Plotting |
| `seaborn` | Styled visualizations |

---

## 👨‍💻 Author

**Osman Osama**  
3rd Year Computer Science Student — Data Science Track  
Egyptian Chinese University (ECU), Cairo, Egypt  
Founder, [Data Wizards Community](https://github.com/osmanosama227-glitch)

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/osmanosama227-glitch)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/https://www.linkedin.com/in/osman-hegazy-5538262b0)

---

## 📄 License


---



