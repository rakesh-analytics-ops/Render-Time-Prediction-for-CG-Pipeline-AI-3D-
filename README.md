
🚀 Render Time Prediction for CG Pipeline

This project focuses on predicting Blender render time using machine learning, based on key 3D scene parameters.
The goal is to estimate render time before rendering starts, so artists and teams can plan scenes better and avoid repeated trial-and-error during production.

This problem is something I have personally faced while working with CG scenes, where small changes in scene complexity often lead to unexpected increases in render time.

📌 Problem Statement

In CG production, estimating render time is challenging because it depends on multiple interacting factors such as:

scene geometry complexity

texture size

lighting setup

output resolution

Render time is usually known only after execution, which makes planning inefficient.
This project aims to predict render time in advance using a regression-based machine learning approach.

🧠 Approach & Key Decisions

Problem Type: Regression

I started with Linear Regression as a baseline model to understand basic relationships.

Linear Regression struggled to model complex patterns between scene features and render time.

I then used Random Forest Regressor, which performed better because render time increases non-linearly with scene complexity.

Random Forest was chosen because it can naturally handle feature interactions without heavy manual feature engineering.

📊 Features Used

The following features were selected based on real CG pipeline considerations:

Polygon Count

Texture Size (MB)

Number of Lights

Output Resolution

Target Variable:

Render Time (in seconds)

📈 Results & Observations

Random Forest outperformed Linear Regression based on MAE and R² score.

Actual vs Predicted plots show a strong alignment, indicating the model captures scene complexity effectively.

Scenes with similar polygon counts but larger textures showed higher render times, which the ensemble model handled better than the linear model.

🛠️ Tech Stack

Python

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

Jupyter Notebook

✅ Conclusion

This project demonstrates that machine learning can be effectively used to estimate render time before execution.
Such predictions can help artists optimize scenes earlier and improve overall CG pipeline efficiency.
