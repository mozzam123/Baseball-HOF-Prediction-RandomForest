# Baseball Hall of Fame Prediction using Random Forest Classifier

## Project Overview

This project leverages a **Random Forest Classifier** to predict whether a baseball player should be inducted into the **Baseball Hall of Fame**. The dataset contains career statistics for numerous baseball players, and the model is trained to identify Hall of Fame-worthy players based on their performance metrics.

### Key Objectives:
- **Predict** the likelihood of a baseball player being inducted into the Hall of Fame.
- **Evaluate** player career statistics to determine the most important factors in the Hall of Fame decision.
- **Optimize** the Random Forest Classifier for better prediction performance using hyperparameter tuning.

## Dataset Overview

The dataset includes various performance statistics for baseball players. Each row represents a player's career, and the target variable, HOF, indicates whether the player has been inducted into the Hall of Fame (1) or not (0).

Key features include:
- **YRS**: Years played
- **G**: Games played
- **AB**: At-bats
- **R**: Runs
- **H**: Hits
- **2B, 3B, HR**: Doubles, triples, home runs
- **RBI**: Runs batted in
- **BB**: Base on balls (walks)
- **SO**: Strikeouts
- **SB**: Stolen bases
- **CS**: Caught stealing
- **BA**: Batting average
- **HOF**: Hall of Fame status (target variable)

## Methodology

### 1. Data Preprocessing
- The dataset is loaded and cleaned by removing unnecessary columns (e.g., PLAYER, CS).
- Features are split into independent variables (X) and the target variable (y).

### 2. Model Selection: Random Forest Classifier
- A **Random Forest Classifier** was chosen for its ability to handle both classification tasks and feature importance analysis.
- The model was first trained using default hyperparameters and then optimized using hyperparameter tuning to improve its accuracy.

### 3. Model Training & Evaluation
- The data was split into **training** and **test** sets using an 80-20 split.
- After training the initial model, we evaluated it using the **accuracy score** and **classification report**.
- Feature importance was calculated to understand which career statistics are most impactful in predicting Hall of Fame induction.

### 4. Hyperparameter Tuning
- The Random Forest Classifier was tuned with the following hyperparameters:
  - n_estimators=1000: Increased number of decision trees for more robust predictions.
  - criterion="entropy": Used entropy to measure the quality of splits.
  - min_samples_split=10: Increased the minimum number of samples required to split a node.
  - max_depth=14: Restricted the maximum depth of the trees to prevent overfitting.
  - random_state=42: Ensured consistent results across runs.

## Results

### Model Performance
- The Random Forest Classifier achieved high accuracy on the test set, indicating strong performance in predicting Hall of Fame induction.
- Below is a sample **classification report** for model evaluation:

          precision    recall  f1-score   support

       0       0.90      0.92      0.91       30
       1       0.88      0.85      0.87       20

accuracy                           0.89       50



## Conclusion

This project demonstrates the application of machine learning techniques to sports analytics, providing insights into the factors that influence Hall of Fame induction. The Random Forest Classifier proved to be an effective model for this classification task, and future work could explore additional models or further refine the feature set.

## Getting Started

To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/baseball-hof-prediction.git
   cd baseball-hof-prediction
