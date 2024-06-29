# Employee-Promotion
Predicting Employee Promotion  using different Machine Learning Algorithm and evaluating the results
The code provided outlines a comprehensive process for loan approval prediction using various machine learning models. The following is a detailed explanation of each section, including the steps taken for data exploration, preprocessing, model training, and evaluation.

### 1. **Importing Necessary Libraries**
Essential libraries for data manipulation, visualization, and machine learning are imported.

### 2. **Reading and Previewing the Dataset**
The dataset is read using `pandas` and initial previews such as the first and last five rows, shape, statistical summary, and data types are examined to understand the data structure.

### 3. **Exploratory Data Analysis (EDA) and Visualization**
Several visualizations are created to explore the dataset:
- **Bar plot:** Count of approved and rejected loans.
- **Histogram:** Distribution of CIBIL scores divided by loan status.
- **Boxplot:** Comparing income of approved and rejected loans.
- **Scatter plot:** Loan amount vs. bank asset value.

Additional plots explore categorical features such as employment and education:
- **Count plots:** Employment and education distribution.
- **Histograms:** For features like number of dependents, income, commercial assets, residential assets, CIBIL score, loan term, and loan amount.
- **Boxplots:** To visualize outliers for various features against loan status.
- **Scatter plots:** Showing relationships between features like CIBIL score and loan amount, commercial assets and loan amount.
- **Pie chart:** Loan status distribution.

### 4. **Data Preprocessing**
Data preprocessing steps include:
- **Label Encoding:** Converting categorical variables (`education`, `self_employed`, `loan_status`) to numerical values.
- **Correlation Matrix:** Visualizing correlations between features to understand their relationships.

### 5. **Feature Selection**
- **SelectKBest:** Selects the top 10 features based on the ANOVA F-value test.
- **SMOTE:** Balancing the dataset using Synthetic Minority Over-sampling Technique to avoid bias.

### 6. **Data Splitting and Scaling**
- **Train-Test Split:** The dataset is split into training and testing sets (80:20 ratio).
- **StandardScaler:** Scaling the features to standardize the data.

### 7. **Machine Learning Algorithms**
Multiple models are trained and evaluated:

#### **Logistic Regression**
- **Training:** Using the scaled training data.
- **Evaluation:** Accuracy, F1 score, recall, and precision on the testing data. Confusion matrix and ROC curve are plotted.
- **Hyperparameter Tuning:** Using `GridSearchCV` for finding the best parameters and cross-validation for model validation.

#### **Support Vector Machine (SVM)**
- **Training:** With a linear kernel.
- **Evaluation:** Accuracy, precision, recall, F1-score on training and testing data. Confusion matrix and ROC curve are plotted.
- **Hyperparameter Tuning:** Using `GridSearchCV` for parameter optimization and cross-validation.

#### **K-Nearest Neighbors (KNN)**
- **Training:** Using the scaled training data.
- **Evaluation:** Accuracy, F1 score, recall, precision on the testing data. Confusion matrix and ROC curve are plotted.
- **Hyperparameter Tuning:** Using `GridSearchCV` for parameter optimization and cross-validation.

#### **Random Forest**
- **Training:** Using 100 estimators.
- **Evaluation:** Accuracy, F1 score, recall, precision on the testing data. Feature importance is visualized.
- **Hyperparameter Tuning:** Using `GridSearchCV` for parameter optimization and cross-validation.

### **Conclusion**
Each model is trained and evaluated, with hyperparameter tuning performed using `GridSearchCV`. The models' performances are compared using accuracy, precision, recall, F1 score, confusion matrices, and ROC curves. Feature importance is visualized for the Random Forest model, highlighting the most significant features.

This comprehensive approach ensures robust analysis, feature selection, data balancing, and thorough evaluation of multiple machine learning models for predicting loan approval.
