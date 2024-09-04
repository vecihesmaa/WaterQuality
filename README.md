# Water Potability Prediction

 ### Project Overview

This project focuses on analyzing water quality data to predict potability using machine learning models. The dataset contains various chemical properties of water samples and a target variable indicating whether the water is potable (safe to drink) or not. The goal is to build and evaluate classification models that can accurately distinguish between potable and non-potable water samples.

### Dataset

The dataset used in this project is **water_potability.csv**.
 - [Download here](https://www.kaggle.com/datasets/adityakadiwal/water-potability)

It contains 3,276 entries with 10 columns:

- ph: pH value of the water (0 to 14).
- Hardness: Calcium and magnesium in ppm.
- Solids: Total dissolved solids in ppm.
- Chloramines: Chloramines in ppm.
- Sulfate: Sulfates in ppm.
- Conductivity: Electrical conductivity in μS/cm.
- Organic_carbon: Organic carbon in ppm.
- Trihalomethanes: Trihalomethanes in μg/L.
- Turbidity: Measure of light reflected by particles in water (NTU).
- Potability: Binary label (0: Non-potable, 1: Potable).
- Data Preprocessing
  
### Handling Missing Values

ph, Sulfate, and Trihalomethanes columns had missing values which were filled with their respective mean values.

### Normalization

Features were normalized using min-max scaling to bring all values into the range [0, 1].
Exploratory Data Analysis (EDA)
Distribution Analysis:
Visualized the distribution of features for potable and non-potable water samples using KDE plots.
Correlation Analysis:
Used a clustermap to visualize correlations between features and identify potential multicollinearity.
Missing Data Visualization:
Visualized missing data using the missingno library to better understand the extent and pattern of missing values.
Model Building
Two machine learning models were implemented and evaluated:

### Decision Tree Classifier

A simple decision tree with a maximum depth of 3 was used.
Achieved a precision score of approximately **0.61**.

### Random Forest Classifier

An ensemble method that aggregates multiple decision trees.
Achieved a precision score of approximately **0.60**.

### Results
The models were evaluated using precision scores and confusion matrices. Both models provided similar results, with the Decision Tree slightly outperforming the Random Forest in terms of precision.

### Visualizations

- Pie Chart: Showed the distribution of potable and non-potable samples in the dataset.
- KDE Plots: Compared feature distributions between potable and non-potable samples.
- Correlation Clustermap: Highlighted feature correlations.
- Confusion Matrices: Visualized model performance on the test set.
- Decision Tree Plot: Visualized the structure of the trained decision tree.

### Dependencies
The following Python libraries are required to run the code:

- numpy
- pandas
- matplotlib
- seaborn
- plotly
- missingno
- scikit-learn



### Copy Code
pip install numpy pandas matplotlib seaborn plotly missingno scikit-learn

### How to Run

Clone the repository.
Ensure you have the required dependencies installed.
Open the Jupyter notebook or script containing the code.
Run the cells or script to reproduce the analysis and model training.

### Conclusion
This project demonstrates how to preprocess and analyze water quality data to build predictive models for water potability. The results indicate that basic machine learning models can provide a reasonable baseline for this task, but further optimization and advanced models might improve performance.

### License
This project is licensed under the MIT License.
