# Clustering Algorithms — From Scratch & Sklearn

---

## Overview
This project implements **K-Means** and **K-Medoids** clustering algorithms entirely
from scratch using only `numpy`, `pandas`, and `matplotlib`, and compares the results
against `scikit-learn`'s built-in implementations.

---

## Dataset
- **File:** `clustering_dataset.csv`
- **Shape:** 210 rows × 2 features (`Feature_1`, `Feature_2`)

---

## What's Implemented

### Task 1 — From Scratch
- K-Means with K-Means++ initialisation
- K-Medoids using PAM (Partitioning Around Medoids)
- Elbow Curve for K = 1 to 12 with optimal K detection
- Per-iteration logging: cluster sizes, per-cluster SSE, total SSE
- Medoid evolution tracking across iterations
- Wall-clock execution time measurement
- Side-by-side final cluster visualisation

### Task 2 — Scikit-Learn
- Re-implementation using `sklearn.cluster.KMeans` and `sklearn_extra.cluster.KMedoids`
- Same parameters as scratch implementation (K, init strategy, distance metric, stopping criterion)
- 4-subplot comparison: Scratch vs Sklearn for both algorithms
- SSE percentage difference computation between scratch and sklearn

---

## Results Summary

| Metric | K-Means Scratch | K-Means Sklearn | K-Medoids Scratch | K-Medoids Sklearn |
|--------|----------------|-----------------|-------------------|-------------------|
| Optimal K | 2 | 2 | 2 | 2 |
| Iterations | 4 | 3 | 2 | 3 |
| Cluster Sizes | [120, 90] | [48, 162] | [52, 158] | [61, 149] |
| Total SSE | 1492.64 | 1628.70 | 2048.67 | 1506.92 |
| Time (s) | 0.0053 | 0.4729 | 0.0156 | 0.0385 |
| SSE Diff | 8.35% | — | 35.95% | — |

---

## Files
```
A-07/
├── clustering_assignment.ipynb   # Main Jupyter Notebook
├── clustering_dataset.csv        # Dataset
├── elbow_curve.png               # Elbow curve plot
├── final_clusters.png            # K-Means vs K-Medoids final clusters
├── scratch_vs_sklearn.png        # 4-subplot comparison
└── README.md
```

---

## Requirements
```
numpy
pandas
matplotlib
scikit-learn
scikit-learn-extra
```

Install dependencies:
```bash
pip install numpy pandas matplotlib scikit-learn scikit-learn-extra
```

---

## How to Run
1. Clone the repository
2. Place `clustering_dataset.csv` in the same folder as the notebook
3. Open `clustering_assignment.ipynb` in Jupyter Notebook or JupyterLab
4. Run all cells in order
