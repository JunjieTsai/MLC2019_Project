# Property price evaluation for Manhattan 2019
For MLC class 2019

## Data wrangling
<br> 

## Preprocessing
### Extremum filter
### Gaussian distribution Test
Chi-Square distribution
### Feature Selection
- Correlation: when two features have high correlation (>0.9), we drop one of the two features.
- P-value: remove irrelevant features  
Reference: https://towardsdatascience.com/feature-selection-correlation-and-p-value-da8921bfb3cf  
### Anomaly Detection
Isolate forest sacrifices 5.6% accuracy of the out of sample, but improve the robustness of the model by 11.0%.
### Standardize
### PCA / Whitening (optional)
### Train & Test random split
66% train & 33% test
<br> 

## Model Selection

### Multivariate linear regression model
achieve out of sample r-squared 0.73, with Cross-validation r-squared 0.32

After PCA, out of sample r-squared 0.49, with Cross-validation r-squared 0.42
PCA makes the model more robust.

After feature selection, out of sample r-squared 0.73, with Cross-validation r-squared 0.38.

### Lasso
Tune hyperparameters with LassoCV  
achieve out of sample r-squared 0.67  
After PCA, out of sample r-squared 0.47  
After feature selection, out of sample r-squared 0.67

### Ridge
Tune hyperparameters with GirdsearchCV  
achieve out of sample r-squared 0.73  
After feature selection, out of sample r-squared 0.73

### Decision Tree
Tune hyperparameters with GirdsearchCV  
Out of sample r-squared 0.02

### Random forest
Tune hyperparameters with GirdsearchCV  
Out of sample r-squared 0.06

### Adaboost
Out of sample r-squared 0.02

### GradientBoosting
Tune hyperparameters with GirdsearchCV  
Out of sample r-squared 0.88, with Cross-validation r-squared 0.55.

### KNN (K Nearest Neighbors Regression)
Out of sample r-squared 0.15

<br> 

## Missed Models
### XGBoost
### LightGBM
### SVM (missed)
### Bayesian Methods
### Bayesian Networks
### Gaussian Processes
### Clustering (optional)
<br> 

## Modeling
Develop models for different landuses.
- tuning
- K-Fold cross validation

## Bias & Limitation
- Data size limited: 8885
- Error not reported
- Overfitting
- Robustness

## Future work
- Optimize the hyperparameters and refine the anomaly detections to improve the accuracy and robustness of the model.
- Add more potential property transaction data
- Try more models
- Website Application
- Temporal prediction
