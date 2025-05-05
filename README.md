# Support Vector Machines (SVM) for Breast Cancer Classification

##  Objective
Apply Support Vector Machines (SVM) for both linear and non-linear classification using the Breast Cancer Wisconsin dataset. Understand concepts like margin maximization, kernel trick, and hyperparameter tuning.

---

##  Dataset
**Breast Cancer Wisconsin (Diagnostic) Dataset**

- 569 samples
- 32 columns (ID, diagnosis, 30 numeric features)
- Target: `diagnosis` (M = Malignant, B = Benign)

---

## 🛠 Tools & Libraries
- Python 3
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn (optional for enhanced visualization)

---

##  Tasks Performed

1. **Data Preprocessing**
   - Removed `id` column
   - Converted `diagnosis` to binary (`M`=1, `B`=0)
   - Standardized features
   - Used only 2 features (`radius_mean`, `texture_mean`) for 2D visualization

2. **SVM Training**
   - Trained SVM with **linear** and **RBF** kernels
   - Visualized decision boundaries (for 2D feature space)
   - Tuned hyperparameters using `GridSearchCV`

3. **Hyperparameter Tuning**
   - Parameters tuned: `C`, `gamma`, `kernel`
   - Best parameters: `{'C': 0.1, 'gamma': 'scale', 'kernel': 'rbf'}`
   - Best cross-validation score: **0.903**

---

##  Results

| Kernel Type | Accuracy (CV) | Best Parameters               |
|-------------|----------------|-------------------------------|
| Linear      | ~0.896         | `C`=1.0 (default)             |
| RBF         | **~0.903**     | `C`=0.1, `gamma`='scale'      |

- **RBF kernel** performs slightly better, capturing non-linear patterns in the data.
- **Linear kernel** still gives decent performance with better interpretability.

---


## 📊 Visualization

- Decision boundary plots were generated to compare linear and RBF kernels.



