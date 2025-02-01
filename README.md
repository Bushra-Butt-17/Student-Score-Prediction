# Student Score Prediction using Linear Regression

## 📌 Overview
This repository contains a comprehensive analysis and prediction model for forecasting students' final scores based on individual activity scores using a **Linear Regression Model**. The dataset includes student performance in various activities, such as quizzes, assignments, and midterms. The model progressively improves by incorporating more features, demonstrating the impact of additional data on predictive accuracy.

---

## 📂 Dataset
The dataset consists of two parts:
- **ICT Morning Dataset** 📊
- **ICT Afternoon Dataset** 🌅

Each dataset contains scores for various activities such as **Quizzes (Q1, Q2, Q3, etc.), Assignments (A1, A2, etc.), Midterms, and Total Score**.

### 🔍 Data Preprocessing:
✔️ Unnecessary columns (e.g., Weights/Scale, Unnamed columns) were removed.  
✔️ Missing values were handled by filling them with **0** or another suitable strategy.  
✔️ Column names were standardized, with the last column renamed as **'Total'** to represent the final score.  
✔️ The first row was set as the column names and dropped from both datasets.  

---

## ⚡ Model Training & Prediction
A **Linear Regression Model** was trained using:
- **Training Set:** ICT Morning Dataset
- **Testing Set:** ICT Afternoon Dataset

### 🔬 Feature Engineering:
The model was progressively trained using different numbers of activities (ranging from **5 to 12** activities). For each step:
1. The model was trained on a subset of activities.
2. Predictions were made.
3. Performance metrics were evaluated.

### 📈 Evaluation Metrics:
The model was assessed using:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **R-Squared (R²)**

---

## 📊 Results & Performance Analysis
| # Activities | MAE  | MSE   | R²    | Avg Diff | Max Diff | Min Diff |
|-------------|------|-------|------|---------|---------|---------|
| 5           | 9.23 | 142.23 | 0.4684 | -1.24 | 28.43 | -28.73 |
| 12          | 0.24 | 0.0858 | 0.9997 | -0.05 | 0.57 | -0.59 |

### 🔥 Key Observations:
✅ **Accuracy Improves** as more activities are included.  
✅ **Lowest Error** achieved with **12 activities**.  
✅ **Maximum & Minimum Differences** reduce significantly with additional features.  

---

## 📊 Visualizations
📌 **Correlation Heatmap** - Shows relationships between different activities.  
📌 **Pairplot** - Displays score distributions across activities.  
📌 **Boxplot** - Analyzes activity-wise score spread.  
📌 **Bar Chart** - Compares average activity scores with the final score.  
📌 **Line Chart** - Tracks students' score progression.  

---

## 🎯 Interactive Prediction
A user-friendly function allows real-time predictions:
1. Select **5-12 activities**.
2. Enter scores for selected activities.
3. Get **Predicted vs. Actual Scores** instantly.  
4. Visualize the **Prediction Accuracy** through a dynamic comparison plot.  

---

## 🚀 Getting Started
### 🔧 Prerequisites
Ensure you have Python installed and required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### ▶️ Run the Model
```bash
python model_training.py
```

### 📌 Example Usage
```python
from model import predict_score
predicted_score = predict_score([10, 8, 9, 7, 10, 8, 9, 10, 9, 8, 10, 7])
print("Predicted Final Score:", predicted_score)
```

---

## 📌 Conclusion
🔹 A **Linear Regression model** successfully predicts students' final scores based on activity scores.  
🔹 Performance **significantly improves** as more features are added.  
🔹 **Interactive Prediction Feature** enhances usability and real-time analysis.  

---

## ⭐ Contributing
If you’d like to contribute, feel free to fork this repository and submit a pull request. 🚀

---

## 📜 License
This project is licensed under the **MIT License**.

---

## 📧 Contact
For queries, reach out at: [your email/LinkedIn/GitHub profile]

