
# 🚀 Render Time Prediction for CG Pipeline

This project focuses on building a **machine learning regression model** to predict **Blender render time** using key 3D scene parameters. The solution helps reduce trial-and-error and improves planning in CG production workflows.

---

## 📌 Problem Statement
Estimating render time for complex 3D scenes is difficult due to multiple interacting factors such as geometry complexity, textures, lighting, and resolution. This project aims to predict render time **before execution** using machine learning.

---

## 🧠 Approach
- Problem Type: Regression
- Models Used:
  - Linear Regression (baseline)
  - Random Forest Regressor (ensemble)
- Random Forest achieved better accuracy by capturing non-linear relationships.

---

## 📊 Features Used
- Polygon Count
- Texture Size (MB)
- Number of Lights
- Output Resolution

**Target Variable:** Render Time (seconds)

---

## 📈 Results
- Random Forest outperformed Linear Regression based on MAE and R² score.
- Actual vs Predicted plots show strong alignment, indicating reliable predictions.

---

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## ✅ Conclusion
The model provides accurate pre-render time estimation, enabling better scene optimization and efficient CG pipeline planning.

---

## 🔮 Future Improvements
- Automate data collection directly from Blender using bpy
- Deploy the model as a Streamlit web application
