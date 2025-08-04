# Exercise 6: Introduction to Machine Learning Lab Report

## SECTION A: REGRESSION ALGORITHMS AND APPLICATIONS

### Task 1: Explore Regression Algorithms (Excluding Simple & Multiple Linear Regression)

#### 1. **Polynomial Regression**
```python
from sklearn.preprocessing import PolynomialFeatures
from sklearn.linear_model import LinearRegression
from sklearn.pipeline import Pipeline

# Implementation
poly_reg = Pipeline([
    ('poly', PolynomialFeatures(degree=2)),
    ('linear', LinearRegression())
])
poly_reg.fit(X_train, y_train)
```

#### 2. **Ridge Regression**
```python
from sklearn.linear_model import Ridge

ridge_reg = Ridge(alpha=1.0)
ridge_reg.fit(X_train, y_train)
```

#### 3. **Lasso Regression**
```python
from sklearn.linear_model import Lasso

lasso_reg = Lasso(alpha=1.0)
lasso_reg.fit(X_train, y_train)
```

#### 4. **ElasticNet Regression**
```python
from sklearn.linear_model import ElasticNet

elastic_reg = ElasticNet(alpha=1.0, l1_ratio=0.5)
elastic_reg.fit(X_train, y_train)
```

#### 5. **Support Vector Regression (SVR)**
```python
from sklearn.svm import SVR

svr_reg = SVR(kernel='rbf', C=100, gamma=0.1)
svr_reg.fit(X_train, y_train)
```

#### 6. **Random Forest Regression**
```python
from sklearn.ensemble import RandomForestRegressor

rf_reg = RandomForestRegressor(n_estimators=100, random_state=42)
rf_reg.fit(X_train, y_train)
```

#### 7. **Gradient Boosting Regression**
```python
from sklearn.ensemble import GradientBoostingRegressor

gb_reg = GradientBoostingRegressor(n_estimators=100, learning_rate=0.1)
gb_reg.fit(X_train, y_train)
```

#### 8. **Decision Tree Regression**
```python
from sklearn.tree import DecisionTreeRegressor

dt_reg = DecisionTreeRegressor(random_state=42)
dt_reg.fit(X_train, y_train)
```

#### 9. **K-Nearest Neighbors Regression**
```python
from sklearn.neighbors import KNeighborsRegressor

knn_reg = KNeighborsRegressor(n_neighbors=5)
knn_reg.fit(X_train, y_train)
```

#### 10. **XGBoost Regression**
```python
import xgboost as xgb

xgb_reg = xgb.XGBRegressor(n_estimators=100, learning_rate=0.1)
xgb_reg.fit(X_train, y_train)
```

### Task 2: Identify Real-World Regression Problems

#### 1. **House Price Prediction**
**Why it's regression**: Predicts continuous house prices in currency units (e.g., $200,000, $350,000).

#### 2. **Stock Price Forecasting**
**Why it's regression**: Predicts continuous stock prices (e.g., $45.67, $123.89).

#### 3. **Temperature Prediction**
**Why it's regression**: Predicts continuous temperature values (e.g., 25.3°C, 78.9°F).

#### 4. **Sales Revenue Forecasting**
**Why it's regression**: Predicts continuous revenue amounts (e.g., $45,000, $120,500).

#### 5. **Energy Consumption Prediction**
**Why it's regression**: Predicts continuous energy usage in kWh (e.g., 1,245.67 kWh).

#### 6. **Customer Lifetime Value**
**Why it's regression**: Predicts continuous monetary value of customers (e.g., $1,250.45).

#### 7. **Website Traffic Prediction**
**Why it's regression**: Predicts continuous number of visitors (e.g., 12,456 visitors).

#### 8. **Crop Yield Estimation**
**Why it's regression**: Predicts continuous yield in tons per hectare (e.g., 8.5 tons/ha).

#### 9. **Delivery Time Estimation**
**Why it's regression**: Predicts continuous time in minutes/hours (e.g., 45.2 minutes).

#### 10. **Insurance Premium Calculation**
**Why it's regression**: Predicts continuous premium amounts (e.g., $1,234.56 annually).

---

## SECTION B: CLASSIFICATION ALGORITHMS AND APPLICATIONS

### Task 3: Explore Classification Algorithms (Excluding Logistic Regression)

#### 1. **Decision Tree Classification**
```python
from sklearn.tree import DecisionTreeClassifier

dt_clf = DecisionTreeClassifier(random_state=42)
dt_clf.fit(X_train, y_train)
```

#### 2. **Random Forest Classification**
```python
from sklearn.ensemble import RandomForestClassifier

rf_clf = RandomForestClassifier(n_estimators=100, random_state=42)
rf_clf.fit(X_train, y_train)
```

#### 3. **Support Vector Machine (SVM)**
```python
from sklearn.svm import SVC

svm_clf = SVC(kernel='rbf', C=1.0, gamma='scale')
svm_clf.fit(X_train, y_train)
```

#### 4. **K-Nearest Neighbors Classification**
```python
from sklearn.neighbors import KNeighborsClassifier

knn_clf = KNeighborsClassifier(n_neighbors=5)
knn_clf.fit(X_train, y_train)
```

#### 5. **Naive Bayes Classification**
```python
from sklearn.naive_bayes import GaussianNB

nb_clf = GaussianNB()
nb_clf.fit(X_train, y_train)
```

#### 6. **Gradient Boosting Classification**
```python
from sklearn.ensemble import GradientBoostingClassifier

gb_clf = GradientBoostingClassifier(n_estimators=100, learning_rate=0.1)
gb_clf.fit(X_train, y_train)
```

#### 7. **AdaBoost Classification**
```python
from sklearn.ensemble import AdaBoostClassifier

ada_clf = AdaBoostClassifier(n_estimators=50, learning_rate=1.0)
ada_clf.fit(X_train, y_train)
```

#### 8. **Neural Network (MLP)**
```python
from sklearn.neural_network import MLPClassifier

mlp_clf = MLPClassifier(hidden_layer_sizes=(100,), max_iter=500)
mlp_clf.fit(X_train, y_train)
```

#### 9. **XGBoost Classification**
```python
import xgboost as xgb

xgb_clf = xgb.XGBClassifier(n_estimators=100, learning_rate=0.1)
xgb_clf.fit(X_train, y_train)
```

#### 10. **Extra Trees Classification**
```python
from sklearn.ensemble import ExtraTreesClassifier

et_clf = ExtraTreesClassifier(n_estimators=100, random_state=42)
et_clf.fit(X_train, y_train)
```

### Task 4: Identify Real-World Classification Problems

#### 1. **Email Spam Detection**
**Why it's classification**: Categorizes emails into discrete classes: "Spam" or "Not Spam".

#### 2. **Medical Diagnosis**
**Why it's classification**: Classifies patients into discrete categories: "Healthy", "Disease A", "Disease B".

#### 3. **Image Recognition**
**Why it's classification**: Categorizes images into discrete classes: "Cat", "Dog", "Bird", etc.

#### 4. **Sentiment Analysis**
**Why it's classification**: Classifies text into discrete sentiment categories: "Positive", "Negative", "Neutral".

#### 5. **Credit Approval**
**Why it's classification**: Categorizes loan applications: "Approved" or "Rejected".

#### 6. **Customer Churn Prediction**
**Why it's classification**: Predicts discrete customer behavior: "Will Churn" or "Will Stay".

#### 7. **Fraud Detection**
**Why it's classification**: Classifies transactions into discrete categories: "Fraudulent" or "Legitimate".

#### 8. **Quality Control**
**Why it's classification**: Categorizes products: "Pass", "Fail", or "Needs Review".

#### 9. **Voice Recognition**
**Why it's classification**: Classifies audio into discrete speaker categories or command types.

#### 10. **Market Segmentation**
**Why it's classification**: Groups customers into discrete segments: "High Value", "Medium Value", "Low Value".

---

## Summary

This exercise demonstrates the fundamental difference between regression (predicting continuous values) and classification (predicting discrete categories). Each algorithm has its strengths and is suitable for different types of data and problem complexity.