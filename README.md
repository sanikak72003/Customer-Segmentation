# Customer Segmentation using Machine Learning

## Project Overview
This project uses unsupervised machine learning to segment mall customers into groups based on their age, annual income, and spending score.

The objective is to identify customer groups with similar characteristics and derive useful business insights from these segments.

## Dataset
- Dataset: Mall Customers
- Total records: 200
- Features used:
  - Age
  - Annual_Income
  - Spending_Score

## Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn
- SciPy
- Joblib

## Project Workflow

1. Exploratory Data Analysis (EDA)
2. Feature selection
3. Feature scaling using StandardScaler
4. K-Means clustering
5. Optimal cluster selection using the Elbow Method and Silhouette Analysis
6. Cluster visualization and profiling
7. Hierarchical Clustering using Agglomerative Clustering
8. Comparison of clustering algorithms
9. Final model pipeline creation
10. Model serialization using Joblib
11. Prediction of clusters for new customers

## Model Evaluation

Two clustering algorithms were evaluated using the Silhouette Score.

| Algorithm | Silhouette Score |
|---|---:|
| K-Means (6 clusters) | 0.4284 |
| Hierarchical Clustering (6 clusters) | 0.4201 |

K-Means was selected as the final model because it achieved a slightly higher Silhouette Score and supports straightforward prediction for new customers.

## Customer Segments

The six clusters represent the following broad customer profiles:

| Cluster | Customer Profile |
|---|---|
| 0 | Older, moderate income, moderate spending |
| 1 | Young, moderate income, moderate spending |
| 2 | Middle-aged, high income, low spending |
| 3 | Young, high income, high spending |
| 4 | Young, low income, high spending |
| 5 | Middle-aged, low income, low spending |

## Model Deployment Preparation

The final preprocessing and clustering steps were combined into a Scikit-learn Pipeline and saved using Joblib.

The saved model can be loaded to assign new customers to one of the six learned clusters without retraining.

## Project Structure

```text
Customer-Segmentation/
├── dataset/
│   └── Mall_Customers.csv
├── notebooks/
│   └── Customer_Segmentation.ipynb
├── models/
│   └── customer_segmentation_model.pkl
├── README.md
└── requirements.txt
```

## How to Run

1. Clone this repository.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the Jupyter Notebook in the `notebooks` directory.
4. Run the notebook cells.

## Conclusion

This project demonstrates how unsupervised learning can be used to identify customer segments and derive business insights from customer demographic and spending data.