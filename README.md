#  Student Performance Predictor

This project uses Machine Learning to **predict whether a student will pass or fail** based on their personal, academic, and social background.

---

##  Project Overview

Educational institutions often need to identify students who might be at risk of failing so that early intervention can be provided. This project applies a classification model on a real-world dataset to make such predictions.

---

##  Dataset

- **Source:** [UCI Student Performance Dataset](https://archive.ics.uci.edu/ml/datasets/Student+Performance)
- **Total Rows:** 395 students
- **Features:** Demographic (age, gender, parents' job), Academic (study time, failures), Social (going out, absences)

---

##  Workflow

1. Data Cleaning and Preprocessing  
2. Feature Engineering and One-Hot Encoding  
3. Splitting Data into Train/Test  
4. Model Training (Random Forest Classifier)  
5. Evaluation using Accuracy, Confusion Matrix, F1-score  
6. Predicting on New Student Input  
7. Visualizing Student Features with Model Outcome  

---

##  Model Performance

- **Model Used:** Random Forest Classifier  
- **Accuracy Achieved:** ~60%  
- **Evaluation Metrics Used:**
  - Accuracy
  - Confusion Matrix
  - Precision, Recall, F1-Score

---

##  Prediction Sample (Visualization Included)

This notebook includes a section to **predict a new student's outcome** and visualize:
- Their feature values in a horizontal bar chart
- A clear textual prediction: ✅ Pass or ❌ Fail

---

## What I Learned (and What Surprised Me)

The model only hit ~60% accuracy, which initially felt like a failure. But digging into the confusion matrix 
revealed something interesting: the model was systematically wrong about students with moderate social activity 
scores, not the extremes. This pointed to the feature "going out frequency" being noisier than I expected, 
and raised a real question about whether self-reported social data is reliable enough for prediction.

The bigger lesson: a 60% accurate model that surfaces a real data quality problem is more useful than a 
95% accurate model on clean synthetic data. I learned to treat model failures as diagnostic tools, not just 
failure states.

## 🚀 How to Run

1. Clone this repository or download the notebook  
2. Make sure you have the required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
