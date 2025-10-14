# 🚀 Improving One-vs-Rest Multiclass Classification with Unsupervised Structure

## 📘 Overview
This project explores the integration of **unsupervised learning** into a traditional **One-vs-Rest (OvR) multiclass classification** system to improve accuracy and generalization on the **Digits dataset**.  
Traditional supervised models like Logistic Regression rely solely on predefined labels, which may hide latent patterns.  
Here, we test whether **unsupervised learning** can reveal these hidden structures and enhance performance.

---

## 🧩 Problem Statement
Traditional supervised learning models for multiclass classification, such as One-vs-Rest Logistic Regression, rely entirely on predefined labels. However, these labels may obscure latent patterns or natural groupings within the data that could improve classification accuracy.  

The challenge is to determine whether **unsupervised learning** can reveal underlying structures in the dataset — and whether these insights can be used to design a **better-performing multiclass classification system** based on binary classifiers.

---

## 🏗️ High-Level Architecture

### 1. Data Loading & Preprocessing
- Dataset: **Digits (8×8 grayscale images, 10 classes)**
- Normalize features  
- Split into **training and testing sets**

### 2. Baseline Model
- **One-vs-Rest Logistic Regression** trained as the baseline classifier

### 3. Unsupervised Structure Discovery
- Apply clustering algorithms:
  - **K-Means**
  - **Gaussian Mixture Model (GMM)**
  - **Agglomerative Clustering**
- Evaluate discovered clusters using:
  - **Adjusted Rand Index (ARI)**
  - **Normalized Mutual Information (NMI)**

### 4. Integration Strategies
Combine unsupervised insights into supervised learning via:
- **(A)** One-hot encoded cluster labels as extra features  
- **(B)** Cluster-specific “local expert” classifiers  
- **(C)** GMM soft probabilities as stacked features (best-performing)

### 5. Evaluation & Visualization
- Compare models using:
  - Accuracy
  - Confusion matrices
  - PCA plots for visual separation
- Conduct **stability checks** across random seeds

---

## 📊 Results Summary

| Approach | Description | Accuracy |
|-----------|--------------|-----------|
| Baseline | OvR Logistic Regression | 93–94% |
| Cluster Features | Added K-Means/GMM cluster labels | 95–96% |
| GMM Soft Probabilities | Probabilistic features from GMM | **Best & most stable** |

✅ Cluster-based feature augmentation improved accuracy  
✅ GMM-based integration achieved **robust and consistent performance**  
✅ PCA visualizations showed **clearer class separation** after adding unsupervised features

---

## ✅ Conclusion
Incorporating **unsupervised learning insights** into a **supervised One-vs-Rest framework** improves multiclass classification.  
This hybrid method reveals that **latent data structures**, once captured, can significantly boost model performance and generalization compared to purely label-driven approaches.

---

## 🧠 Key Learnings
- Blending **unsupervised + supervised** learning improves accuracy and robustness.  
- **GMM soft probabilities** are powerful for feature enrichment.  
- The **Digits dataset** effectively demonstrates latent structure discovery.

---

## 👩‍💻 Team Members
- **Tanushri Mohan Chougale** — *PES2UG24CS826*  
- **Neela G** — *PES2UG23CS376*  

---

## ⚙️ Technologies Used
- **Python**
- **Scikit-learn**
- **NumPy**
- **Pandas**
- **Matplotlib / Seaborn**
- **SciPy**
- **Jupyter Notebook**

---

## 📂 Repository Structure
ml_project/
│
├── ml_project.ipynb # Main implementation
├── project_report.pdf # Report with analysis and results
├── README.md # Documentation (this file)



---

## 💻 How to Run

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Tanushri002/ML_F_PES2UG24CS826_TANUSHRI.git

2️⃣Navigate to the Project Folder
cd ml_project

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Run the Notebook
jupyter notebook ml_project.ipynb