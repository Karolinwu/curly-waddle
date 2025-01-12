# Predicting Olympic Medal Counts

## Project Overview
This project applies machine learning (ML) and deep learning (DL) techniques to predict the total number of Olympic medals won by different countries. By analyzing features like GDP, population, and sports indices, the goal is to explore the methodologies required to build effective prediction models and evaluate their performance.

---

## Dataset Description
The dataset includes the following key features:
- **iso**: Country ISO code
- **ioc**: International Olympic Committee code
- **name**: Country name
- **continent**: Continent of the country
- **population**: Population size
- **gdp**: Gross Domestic Product (GDP)
- **olympics_index**: Composite Olympic performance index
- **sports_index**: Sports infrastructure and support index
- **total**: Total medal count
- **gold**: Number of gold medals
- **silver**: Number of silver medals
- **bronze**: Number of bronze medals

---

## Workflow

### 1. Data Preprocessing
- **Missing Values**:
  - Filled missing values based on logical rules, e.g., using country name to infer continent.
- **Outlier Detection and Handling**:
  - Detected anomalies using descriptive statistics and visualizations (e.g., histograms).
  - Replaced outliers in columns like `olympics_index` and `gdp` with median values.
- **Feature Engineering**:
  - Created `GDP per capita` to capture interactions between GDP and population.
- **Data Splitting**:
  - Divided the dataset into training (80%) and testing (20%) sets.

---

### 2. Exploratory Data Analysis (EDA)
- **Statistical Analysis**:
  - Computed mean, median, and standard deviation for key features.
- **Data Visualizations**:
  - Used scatter plots to examine relationships (e.g., GDP per capita vs. total medals).
  - Created correlation matrices to identify relationships between features.
- **Feature Importance**:
  - Identified GDP and population as the strongest predictors of medal counts.

---

### 3. Model Development
#### 3.1 Machine Learning Models
- **Linear Regression**:
  - Implemented to analyze simple linear relationships.
- **Decision Tree**:
  - Applied to capture nonlinear interactions and decision-making rules.
- **Random Forest**:
  - Used to improve robustness and handle complex feature interactions.

#### 3.2 Deep Learning Model
- **Fully Connected Neural Network**:
  - Built with Keras, including two hidden layers with 128 and 64 neurons.
  - Applied L2 regularization and Dropout to mitigate overfitting.
- **Hyperparameter Tuning**:
  - Conducted random search to optimize learning rate, regularization strength, and the number of neurons.

#### 3.3 Additional Methods
- **Principal Component Analysis (PCA)**:
  - Reduced dimensionality to focus on key features while retaining variance.
- **K-Nearest Neighbors (KNN)**:
  - Implemented using PCA components as input features.

---

### 4. Model Evaluation and Comparison
- **Evaluation Metrics**:
  - Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² score were used to evaluate model performance.
- **Regularization Analysis**:
  - Studied the impact of L2 and Dropout regularization on generalization.
- **Model Comparison**:
  - Compared performance between simpler models (e.g., Linear Regression) and complex ones (e.g., Neural Networks).

---

### 5. Data Standardization and Feature Interaction Analysis
- **Standardization**:
  - Applied where necessary (e.g., for PCA, KNN) to balance feature scales.
- **Feature Interactions**:
  - Generated interaction terms using polynomial feature methods and assessed their importance using Random Forest.

---




## Key Challenges and Learnings
- **Handling Missing and Outlier Data**: Replacing anomalies while preserving interpretability.
- **Balancing Model Complexity and Generalization**: Using regularization and parameter tuning to prevent overfitting.
- **Feature Importance Analysis**: Understanding the significance of GDP and population in predicting Olympic success.

---


