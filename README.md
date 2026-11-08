# Eigenfaces from Scratch

A rigorous, step-by-step implementation of **Principal Component Analysis (PCA)** and **Eigenfaces** from scratch using pure **NumPy** (`eigh` / `svd`), exploring what principal components actually represent in facial image space.

---

## 🔍 Core Question
If PCA turns a face into a short list of numbers, **what is each number actually doing to the image?**

Our investigation tests the hypothesis that:
- The **earlier** components primarily capture **coarse, global structures** (such as lighting, illumination gradients, and overall head shape).
- The **later** components capture **finer details** and subtle facial variations.

---

## 📊 Dataset
- **Olivetti Faces Dataset** (via `scikit-learn`): 40 distinct individuals, 10 photographs per person.
- Image dimensions: $64 \times 64$ pixels (flattened to 4,096-dimensional vectors).

---

## 📐 Implementation Rules
1. **PCA from Scratch:** Implemented exclusively using NumPy matrix operations (`np.linalg.eigh` and `np.linalg.svd`).
2. **Strict Data Separation:** Mean calculation and eigenface basis components are computed strictly from **training images only** to prevent data leakage.
3. **Libraries:** `NumPy` for mathematical computations, `Matplotlib` for visual analysis, `scikit-learn` strictly for dataset loading.

---

## 🗺️ Roadmap & Notebook Structure

- **Part I — Building Face Space**
  - Data loading, train/test splitting per individual.
  - Centering data and computing the mean face.
  - Gram matrix PCA & covariance matrix formulation.
  - Reconstructions and reconstruction error analysis.
  - SVD cross-validation check.

- **Part II — Interpreting Principal Components**
  - Honest step sizes and face morphing along individual principal axes.
  - Quantitative measurements of component impact.
  - Comparing early vs. late principal components.

- **Part III — Conclusions & Insights**
  - Summary of empirical findings regarding global vs. local feature representation.

---

## 🚀 Getting Started

### Prerequisites
Ensure you have Python 3.9+ installed.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/eigenfaces-from-scratch.git
   cd eigenfaces-from-scratch
   ```

2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook eigenfaces_from_scratch.ipynb
   ```

---

## 📝 License
This project is open source and available under the [MIT License](LICENSE).
