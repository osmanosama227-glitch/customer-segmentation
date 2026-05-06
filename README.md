# 🛍️ Customer Segmentation — Interactive GUI

> **Data Mining Course Project** | Egyptian Chinese University (ECU)  
> K-Means & Agglomerative Clustering with an interactive ipywidgets dashboard

---

## 📌 Overview

This project applies unsupervised machine learning to segment mall customers based on their **Annual Income** and **Spending Score**, using the classic Mall Customer dataset. The notebook features a fully interactive GUI built with `ipywidgets` — no separate app needed, just run the cells.

---

## ✨ Features

| Tab | Description |
|-----|-------------|
| 📊 **Optimal K Finder** | Elbow Method + Silhouette Scores with interactive K slider |
| 🔵 **K-Means Explorer** | Scatter plot with switchable axes and centroid toggle |
| 🌳 **Agglomerative + Dendrogram** | Ward linkage dendrogram with draggable cut line |
| 🏷️ **Segment Profiles Dashboard** | 6-chart dashboard comparing cluster profiles (toggle K-Means / Agglomerative) |
| ⚖️ **Algorithm Comparison** | Side-by-side silhouette score comparison |
| 🔮 **Predict Customer Segment** | Enter income & spending score → get instant segment prediction + marketing strategy |
| 📋 **Raw Data Explorer** | Filter by cluster and browse the dataset |

---

## 🗂️ Dataset

**Mall Customer Segmentation** — [`Mall_Customers.csv`](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

| Column | Description |
|--------|-------------|
| `CustomerID` | Unique customer identifier |
| `Gender` | Male / Female |
| `Age` | Customer age |
| `Annual Income (k$)` | Annual income in thousands USD |
| `Spending Score (1–100)` | Mall-assigned spending behavior score |

> ⚠️ Download `Mall_Customers.csv` from Kaggle and place it in the same folder as the notebook.

---

## 🧠 Algorithms

- **K-Means Clustering** (k-means++ init, k=5)
- **Agglomerative Clustering** (Ward linkage, n=5)
- **Evaluation metric:** Silhouette Score

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/customer-segmentation-gui.git
cd customer-segmentation-gui
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add the dataset
Download `Mall_Customers.csv` from [Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) and place it in the root folder.

### 4. Run the notebook
```bash
jupyter notebook Customer_Segmentation_GUI.ipynb
```

> **Tip:** Run all cells top to bottom. The interactive widgets activate after each cell executes.

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
scipy
ipywidgets
jupyter
```

---

## 📊 Results

| Algorithm | Silhouette Score |
|-----------|-----------------|
| K-Means ✅ | ~0.554 |
| Agglomerative | ~0.551 |

**K-Means** produces slightly better-defined clusters on this dataset.

### Identified Segments

| Cluster | Segment | Profile |
|---------|---------|---------|
| 0 | Careful Customers | Low Income · Low Spending |
| 1 | Impulsive Buyers | Low Income · High Spending |
| 2 | Average Customers | Medium Income · Medium Spending |
| 3 | Potential Savers | High Income · Low Spending |
| 4 | VIP Targets ⭐ | High Income · High Spending |

---

## 🗃️ Project Structure

```
customer-segmentation-gui/
│
├── Customer_Segmentation_GUI.ipynb   # Main notebook
├── Mall_Customers.csv                # Dataset (download separately)
├── requirements.txt
└── README.md
```

---

## 👨‍💻 Author

**Osman Osama**  
Computer Science — Data Science Track, Egyptian Chinese University  
Founder, [Data Wizards](https://github.com/osmanosama227-glitch) Community

---

## 📄 License

This project is for academic purposes.
