
# 🔬 Predicting Hydrate Formation and Internal Corrosion in Natural Gas Pipelines

## Overview

This project investigates the complex interplay between **hydrate formation** and **internal corrosion** in natural gas pipelines using a hybrid approach that combines **deterministic modeling** with **machine learning**. By simulating 100,000 operating scenarios using a simplified 1D pipeline model, the study predicts hydrate likelihood (classification) and corrosion rates (regression) under varying thermodynamic and fluid conditions.

---

## 📁 Project Structure

```
hydrate_corrosion_dashboard.html   ← Static HTML visualization of results
README.md                          ← Project documentation and usage
```

---

## ⚙️ Simulation Details

- **Model Type**: 1D deterministic simulation
- **Pipeline Specs**: Diameters (12–48 in), Pressures (50–250 bar), Temperatures (5–15°C)
- **Key Parameters**: Pressure, temperature, flow rate, pH, gas composition (20 mol% CO₂), wall shear stress, Reynolds number, hydrate stability, corrosion rate

### Methodology:
- Latin Hypercube Sampling (LHS) for input variability
- NORSOK M-506 standard for CO₂ corrosion modeling
- SHAP values for explainability

---

## 🤖 Machine Learning Models

### 1. **Hydrate Formation Prediction (Classification)**

- **LightGBM Results**:
  - Accuracy: 99.713%
  - F1-Score: 0.99814
  - Precision: 0.99801
  - Recall: 0.99827
  - AUC: 0.99582

- **ANN Results**:
  - Accuracy: 99.787%
  - F1-Score: 0.99805
  - Precision: 0.99671
  - Recall: 0.99939
  - AUC: 0.99422

### 2. **Corrosion Rate Prediction (Regression with ANN)**

- MAE: 84.97 mm/yr
- MSE: 3,466,958.44
- RMSE: 1861.98 mm/yr
- R²: 0.829

---

## 📊 Key Insights from SHAP

Top Influential Features (for corrosion prediction):
- Temperature
- Temperature-Dependent Constant (K_T)
- pH-dependent term (f(pH)_T)
- Pressure
- Flow Rate

These features showed non-linear interactions, emphasizing the necessity of hybrid modeling in real-world systems.

---

## 💡 Usage

1. Clone/download the repo.
2. Open `hydrate_corrosion_dashboard.html` in any browser.
3. Use visualizations to explore model predictions and SHAP-based explanations.
4. Leverage findings to guide mitigation strategies for hydrate/corrosion management.

---

## 🔬 Future Work

- Integrate multi-phase and heat transfer physics
- Improve hydrate thermodynamic modeling
- Validate models with lab/field datasets

---

## 📫 Contact

**Victor Ikechukwu**  
📧 Email: [vikechukwu43@gmail.com](mailto:vikechukwu43@gmail.com)  
🔗 LinkedIn: [linkedin.com/in/victor-ikechukwu-1169942a7](https://www.linkedin.com/in/victor-ikechukwu-1169942a7?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)  
📍 Location: Port Harcourt, Nigeria
