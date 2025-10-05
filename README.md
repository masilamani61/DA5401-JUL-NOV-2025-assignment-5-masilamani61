#  DA5401 Assignment 5 — Manifold Visualization

**Author:** V. G. Masilamani (DA25S005)

---

##  Overview

This notebook explores **manifold learning techniques** to visualize high-dimensional data, as part of **Assignment 5 for DA5401 - Data Analytics**.  
The main objective is to understand and compare nonlinear dimensionality reduction methods — **t-SNE** and **Isomap** — and evaluate their ability to reveal hidden data structures.

The analysis also includes a **veracity inspection**, identifying:
- **Noisy labels**
- **Outliers**
- **Hard-to-learn samples**

Through visualization and interpretation, the assignment aims to assess both the **performance** and **interpretability** of manifold embeddings.

---

##  Structure of the Notebook

### **1. Data Preprocessing**
- Loaded the dataset and inspected its shape and properties.  
- Applied **StandardScaler** to standardize feature scales, ensuring fair distance-based computations.  
- Created simplified categorical variables to assist in visualization and color-coding.

### **2. Label Categorization**
- Analyzed label distribution.  
- Identified **top single-label** and **multi-label combinations** for focus.  
- Constructed a categorical variable capturing major label patterns (`Top1`, `Top2`, `CommonCombo`, `Other`).

### **3. Manifold Learning**
- Implemented **t-SNE (t-distributed Stochastic Neighbor Embedding)** for nonlinear embeddings.  
- Implemented **Isomap**, leveraging geodesic distances for preserving local and global structures.  
- Compared t-SNE and Isomap embeddings visually and conceptually.

### **4. Veracity Inspection**
- Identified data irregularities, including:
  - **Noisy labels**
  - **Outliers**
  - **Hard-to-learn instances**
- Visualized these anomalies within the manifold space for interpretation.

### **5. Discussion & Interpretation**
- Compared the quality of embeddings.
- Interpreted cluster separability and overlaps.
- Evaluated how veracity issues influence the manifold representation.

---

##  Key Concepts

| Concept | Description |
|----------|--------------|
| **t-SNE** | Nonlinear dimensionality reduction method preserving local neighborhood structure. |
| **Isomap** | Extends MDS by using geodesic distances to preserve global manifold geometry. |
| **Standardization** | Ensures all features contribute equally to distance metrics. |
| **Veracity Analysis** | Detects data quality issues such as noise and outliers. |

---

##  Environment Setup

### **Requirements**
Ensure the following Python packages are installed:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
