##  Steps 

### 1. Import & Preprocess the Dataset
- Loaded dataset using pandas
- Checked for missing values: None found
- Explored dataset shape, types, and descriptive statistics
- Encoded categorical columns using One-Hot Encoding with `pd.get_dummies(drop_first=True)`

---

### 2. Data Visualization
- Visualized distribution of price with histogram and KDE
- Created scatter plot: `price` vs `area`
- Boxplots to examine price vs:
  - `bedrooms`
  - `bathrooms`
  - `stories`
  - `parking`

---

### 3. Train-Test Split
- Separated data into features (`X`) and target (`y`)
- Used `train_test_split(test_size=0.2, random_state=42)`

---

### 4. Fit a Linear Regression Model
- Used `LinearRegression()` from `sklearn.linear_model`
- Trained model on the training data

---

### 5. Evaluate the Model
- Evaluation metrics:
  - **Mean Absolute Error (MAE):** ~970,043.40
  - **Mean Squared Error (MSE):** ~1.75e+12
  - **R² Score:** 0.65 (explains 65% of the variance in price)

---

### 6. Plot Regression Line
- Visualized actual vs predicted values (`price` vs `area`)
- Drew regression line (keeping other features fixed at mean)

---

### 7. Interpret Model Coefficients
- Extracted and sorted model coefficients
- Visualized feature importance using a horizontal barplot

---

##  Results

###  Top Positive Predictors of Price:
- `bathrooms`
- `airconditioning_yes`
- `hotwaterheating_yes`
- `prefarea_yes`
- `stories`

###  Top Negative Predictors of Price:
- `furnishingstatus_unfurnished`
- `furnishingstatus_semi-furnished`

