# 🧠 Unsupervised Learning: Preprocessing, Scaling, and PCA

Welcome to the **Unsupervised Learning** repository! This project explores preprocessing techniques, scaling, and **Principal Component Analysis (PCA)** for unsupervised learning tasks. It includes data scaling, visualization, and dimensionality reduction using PCA.

---

## 📂 **Project Overview**

This repository demonstrates how to preprocess and scale data for machine learning models, as well as how to use **PCA** for dimensionality reduction. It covers:

- **Data Scaling**: Using `MinMaxScaler` and `StandardScaler`.
- **PCA**: Dimensionality reduction and visualization of high-dimensional data.
- **Impact on Supervised Learning**: How scaling affects model performance.

---

## 🛠️ **Tech Stack**

- **Python**
- **Scikit-learn**
- **mglearn**
- **NumPy**
- **Matplotlib**

---

## 📊 **Datasets**

The project uses the following datasets:
- **Breast Cancer Dataset**: For scaling and PCA.
- **Synthetic Blobs Dataset**: For visualizing scaling effects.

---

## 🧠 **Key Concepts**

### 1. **Data Scaling**
- **MinMaxScaler**: Scales data to a specified range (e.g., [0, 1]).
- **StandardScaler**: Standardizes data to have zero mean and unit variance.

### 2. **Principal Component Analysis (PCA)**
- A linear dimensionality reduction technique.
- Projects data onto orthogonal components that capture maximum variance.
- Used for visualization and feature extraction.

### 3. **Impact on Supervised Learning**
- Scaling data can significantly improve model performance.
- PCA can reduce overfitting and improve interpretability.

---

## 🚀 **Code Highlights**

### Data Scaling with MinMaxScaler
```python
scaler = MinMaxScaler()
scaler.fit(X_train)
X_train_scaled = scaler.transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

### Data Scaling with StandardScaler
```python
scaler = StandardScaler()
scaler.fit(X_train)
X_train_scaled = scaler.transform(X_train)
X_test_scaled = scaler.transform(X_test)
```

### PCA for Dimensionality Reduction
```python
pca = PCA(n_components=2)
pca.fit(X_scaled)
X_pca = pca.transform(X_scaled)
```

### Visualizing PCA Components
```python
plt.figure(figsize=(8, 8))
mglearn.discrete_scatter(X_pca[:, 0], X_pca[:, 1], cancer.target)
plt.xlabel("First principal component")
plt.ylabel("Second principal component")
```

### Impact of Scaling on Model Performance
```python
svm = SVC(C=100)
svm.fit(X_train_scaled, y_train)
print(svm.score(X_test_scaled, y_test))
```

---

## 🛠️ **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/navidfalah/unsupervised-learning.git
   cd unsupervised-learning
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   ```bash
   jupyter notebook unsupervised_learning.ipynb
   ```

---

## 🤝 **Contributing**

Feel free to contribute to this project! Open an issue or submit a pull request.

---

## 📧 **Contact**

- **Name**: Navid Falah
- **GitHub**: [navidfalah](https://github.com/navidfalah)
- **Email**: navid.falah7@gmail.com
