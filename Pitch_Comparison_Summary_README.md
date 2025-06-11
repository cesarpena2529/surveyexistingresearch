
# Summary of “Predicting MLB Pitch Classes”

## 🔍 Project Overview

This project, published on Analytics Vidhya, aimed to classify MLB pitch types using publicly available Statcast data. The author built a machine learning pipeline to predict the class of each pitch (e.g., fastball, slider, curveball) based on physical and motion-based characteristics.

## 🧱 Project Workflow

### 1. Data Collection
The dataset sourced from Kaggle includes thousands of pitches with attributes such as:
- Pitch speed
- Spin rate
- Horizontal & vertical movement
- Release extension
- Release point

### 2. Data Cleaning
- Removed duplicates and irrelevant columns.
- Handled missing values.
- Normalized numerical features for consistent scaling.

### 3. Exploratory Data Analysis (EDA)
- Visualized correlations between features.
- Explored the frequency and distribution of different pitch types.

### 4. Model Building
- Models used: K-Nearest Neighbors (KNN), Decision Trees, and Logistic Regression.
- KNN showed the best performance in classifying pitch types.

### 5. Evaluation
- Applied metrics: Accuracy, Confusion Matrix, and F1-score.
- Found that some pitch types are naturally harder to distinguish due to physical similarity.

### 6. Conclusion
- Demonstrated that standard machine learning methods can effectively classify pitches.
- Noted room for improvement, particularly in overlapping pitch types.

## 🔄 Comparison with My Project (PitchDNA)

| Aspect | Their Project | My Project |
|--------|---------------|------------|
| **Goal** | Predict pitch type from features | Identify similar MLB pitchers based on pitch input |
| **Model** | Classification (KNN, Decision Tree) | Similarity engine (KNN + UMAP) |
| **Frontend** | None | React app with UMAP visualization |
| **User Input** | Static data | Dynamic input via form (by player or pitch metrics) |
| **Visualization** | Static plots | Interactive UMAP projection with custom user point |
| **Use Case** | ML experimentation | Player development, pitch analysis, scouting tool |

## 💡 Summary

While the original project focuses on **categorizing pitches**, my project centers on **comparing pitch characteristics** to existing MLB pitchers. It offers an interactive web-based experience with real-time comparisons, visualizations, and coaching utility—bridging the gap between data science and on-field application.
