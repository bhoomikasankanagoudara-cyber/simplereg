```markdown
# Simple Linear Regression Pipeline

A clean, modular end-to-end Machine Learning pipeline implementing Simple Linear Regression to predict employee salaries based on years of experience.

---

## Technical Overview

This repository demonstrates the step-by-step implementation of a Simple Linear Regression model using Python. The objective is to establish a linear relationship between an independent feature (**Years of Experience**) and a target variable (**Salary**).


```

[ Data Collection ] ──> [ Data Cleaning ] ──> [ Feature Selection ] ──> [ Model Training ] ──> [ Evaluation ]

```

---

## Dataset Description

The project uses `Salary_dataset.csv`, consisting of 30 records detailing employee experience levels alongside corresponding annual salary figures.

* **Independent Variable ($X$):** `YearsExperience` (Continuous feature in years)
* **Dependent Variable ($y$):** `Salary` (Continuous target variable)
* **Dataset Shape:** 30 rows $\times$ 2 features (after index column removal)

---

## Machine Learning Pipeline

1. **Data Ingestion & Inspection:** Loading raw dataset using `pandas` and analyzing structure.
2. **Data Cleaning & Preprocessing:**
   * Checking for and handling duplicate records.
   * Identifying missing/null values (`df.isnull().sum()`).
   * Dropping irrelevant structural artifacts (e.g., `Unnamed: 0` index column).
3. **Exploratory Data Analysis (EDA):** Visualizing feature relationships using `matplotlib` scatter plots.
4. **Data Splitting:** Partitioning data into training and test datasets.
5. **Model Building & Fitting:** Training a `LinearRegression` model to estimate line parameters (slope and intercept).
6. **Model Evaluation:** Assessing prediction accuracy on holdout test data.

---

## Usage & Implementation

### Prerequisites

```bash
pip install numpy pandas matplotlib scikit-learn

```

### Python Execution Script

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# 1. Load Dataset
df = pd.read_csv("Salary_dataset.csv")

# 2. Data Cleaning
df.drop(columns=["Unnamed: 0"], inplace=True, errors="ignore")

# 3. Feature & Target Isolation
X = df[["YearsExperience"]]
y = df["Salary"]

# 4. Train/Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 5. Model Training
model = LinearRegression()
model.fit(X_train, y_train)

# 6. Inference & Evaluation
y_pred = model.predict(X_test)

print(f"Model Coefficient (Slope): {model.coef_[0]:.2f}")
print(f"Model Intercept: {model.intercept_:.2f}")
print(f"R² Score: {r2_score(y_test, y_pred):.4f}")

# 7. Visualization
plt.figure(figsize=(8, 5))
plt.scatter(X, y, color="blue", label="Actual Data")
plt.plot(X_train, model.predict(X_train), color="red", label="Regression Line")
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Years Experience vs Salary")
plt.legend()
plt.show()

```

---

## Results & Insights

* **Correlation:** Demonstrates a strong positive linear relationship between `YearsExperience` and `Salary`.
* **Zero Duplicates / Zero Missing Values:** Quality checks confirm complete dataset integrity.

```

``````markdown
# Simple Linear Regression Pipeline

A clean, modular end-to-end Machine Learning pipeline implementing Simple Linear Regression to predict employee salaries based on years of experience.

---

## Technical Overview

This repository demonstrates the step-by-step implementation of a Simple Linear Regression model using Python. The objective is to establish a linear relationship between an independent feature (**Years of Experience**) and a target variable (**Salary**).


```

[ Data Collection ] ──> [ Data Cleaning ] ──> [ Feature Selection ] ──> [ Model Training ] ──> [ Evaluation ]

```

---

## Dataset Description

The project uses `Salary_dataset.csv`, consisting of 30 records detailing employee experience levels alongside corresponding annual salary figures.

* **Independent Variable ($X$):** `YearsExperience` (Continuous feature in years)
* **Dependent Variable ($y$):** `Salary` (Continuous target variable)
* **Dataset Shape:** 30 rows $\times$ 2 features (after index column removal)

---

## Machine Learning Pipeline

1. **Data Ingestion & Inspection:** Loading raw dataset using `pandas` and analyzing structure.
2. **Data Cleaning & Preprocessing:**
   * Checking for and handling duplicate records.
   * Identifying missing/null values (`df.isnull().sum()`).
   * Dropping irrelevant structural artifacts (e.g., `Unnamed: 0` index column).
3. **Exploratory Data Analysis (EDA):** Visualizing feature relationships using `matplotlib` scatter plots.
4. **Data Splitting:** Partitioning data into training and test datasets.
5. **Model Building & Fitting:** Training a `LinearRegression` model to estimate line parameters (slope and intercept).
6. **Model Evaluation:** Assessing prediction accuracy on holdout test data.

---

## Usage & Implementation

### Prerequisites

```bash
pip install numpy pandas matplotlib scikit-learn

```

### Python Execution Script

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# 1. Load Dataset
df = pd.read_csv("Salary_dataset.csv")

# 2. Data Cleaning
df.drop(columns=["Unnamed: 0"], inplace=True, errors="ignore")

# 3. Feature & Target Isolation
X = df[["YearsExperience"]]
y = df["Salary"]

# 4. Train/Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 5. Model Training
model = LinearRegression()
model.fit(X_train, y_train)

# 6. Inference & Evaluation
y_pred = model.predict(X_test)

print(f"Model Coefficient (Slope): {model.coef_[0]:.2f}")
print(f"Model Intercept: {model.intercept_:.2f}")
print(f"R² Score: {r2_score(y_test, y_pred):.4f}")

# 7. Visualization
plt.figure(figsize=(8, 5))
plt.scatter(X, y, color="blue", label="Actual Data")
plt.plot(X_train, model.predict(X_train), color="red", label="Regression Line")
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Years Experience vs Salary")
plt.legend()
plt.show()

```

---

## Results & Insights

* **Correlation:** Demonstrates a strong positive linear relationship between `YearsExperience` and `Salary`.
* **Zero Duplicates / Zero Missing Values:** Quality checks confirm complete dataset integrity.

```

``````markdown
# Simple Linear Regression Pipeline

A clean, modular end-to-end Machine Learning pipeline implementing Simple Linear Regression to predict employee salaries based on years of experience.

---

## Technical Overview

This repository demonstrates the step-by-step implementation of a Simple Linear Regression model using Python. The objective is to establish a linear relationship between an independent feature (**Years of Experience**) and a target variable (**Salary**).


```

[ Data Collection ] ──> [ Data Cleaning ] ──> [ Feature Selection ] ──> [ Model Training ] ──> [ Evaluation ]

```

---

## Dataset Description

The project uses `Salary_dataset.csv`, consisting of 30 records detailing employee experience levels alongside corresponding annual salary figures.

* **Independent Variable ($X$):** `YearsExperience` (Continuous feature in years)
* **Dependent Variable ($y$):** `Salary` (Continuous target variable)
* **Dataset Shape:** 30 rows $\times$ 2 features (after index column removal)

---

## Machine Learning Pipeline

1. **Data Ingestion & Inspection:** Loading raw dataset using `pandas` and analyzing structure.
2. **Data Cleaning & Preprocessing:**
   * Checking for and handling duplicate records.
   * Identifying missing/null values (`df.isnull().sum()`).
   * Dropping irrelevant structural artifacts (e.g., `Unnamed: 0` index column).
3. **Exploratory Data Analysis (EDA):** Visualizing feature relationships using `matplotlib` scatter plots.
4. **Data Splitting:** Partitioning data into training and test datasets.
5. **Model Building & Fitting:** Training a `LinearRegression` model to estimate line parameters (slope and intercept).
6. **Model Evaluation:** Assessing prediction accuracy on holdout test data.

---

## Usage & Implementation

### Prerequisites

```bash
pip install numpy pandas matplotlib scikit-learn

```

### Python Execution Script

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# 1. Load Dataset
df = pd.read_csv("Salary_dataset.csv")

# 2. Data Cleaning
df.drop(columns=["Unnamed: 0"], inplace=True, errors="ignore")

# 3. Feature & Target Isolation
X = df[["YearsExperience"]]
y = df["Salary"]

# 4. Train/Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 5. Model Training
model = LinearRegression()
model.fit(X_train, y_train)

# 6. Inference & Evaluation
y_pred = model.predict(X_test)

print(f"Model Coefficient (Slope): {model.coef_[0]:.2f}")
print(f"Model Intercept: {model.intercept_:.2f}")
print(f"R² Score: {r2_score(y_test, y_pred):.4f}")

# 7. Visualization
plt.figure(figsize=(8, 5))
plt.scatter(X, y, color="blue", label="Actual Data")
plt.plot(X_train, model.predict(X_train), color="red", label="Regression Line")
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Years Experience vs Salary")
plt.legend()
plt.show()

```

---

## Results & Insights

* **Correlation:** Demonstrates a strong positive linear relationship between `YearsExperience` and `Salary`.
* **Zero Duplicates / Zero Missing Values:** Quality checks confirm complete dataset integrity.

```

``````markdown
# Simple Linear Regression Pipeline

A clean, modular end-to-end Machine Learning pipeline implementing Simple Linear Regression to predict employee salaries based on years of experience.

---

## Technical Overview

This repository demonstrates the step-by-step implementation of a Simple Linear Regression model using Python. The objective is to establish a linear relationship between an independent feature (**Years of Experience**) and a target variable (**Salary**).


```

[ Data Collection ] ──> [ Data Cleaning ] ──> [ Feature Selection ] ──> [ Model Training ] ──> [ Evaluation ]

```

---

## Dataset Description

The project uses `Salary_dataset.csv`, consisting of 30 records detailing employee experience levels alongside corresponding annual salary figures.

* **Independent Variable ($X$):** `YearsExperience` (Continuous feature in years)
* **Dependent Variable ($y$):** `Salary` (Continuous target variable)
* **Dataset Shape:** 30 rows $\times$ 2 features (after index column removal)

---

## Machine Learning Pipeline

1. **Data Ingestion & Inspection:** Loading raw dataset using `pandas` and analyzing structure.
2. **Data Cleaning & Preprocessing:**
   * Checking for and handling duplicate records.
   * Identifying missing/null values (`df.isnull().sum()`).
   * Dropping irrelevant structural artifacts (e.g., `Unnamed: 0` index column).
3. **Exploratory Data Analysis (EDA):** Visualizing feature relationships using `matplotlib` scatter plots.
4. **Data Splitting:** Partitioning data into training and test datasets.
5. **Model Building & Fitting:** Training a `LinearRegression` model to estimate line parameters (slope and intercept).
6. **Model Evaluation:** Assessing prediction accuracy on holdout test data.

---

## Usage & Implementation

### Prerequisites

```bash
pip install numpy pandas matplotlib scikit-learn

```

### Python Execution Script

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# 1. Load Dataset
df = pd.read_csv("Salary_dataset.csv")

# 2. Data Cleaning
df.drop(columns=["Unnamed: 0"], inplace=True, errors="ignore")

# 3. Feature & Target Isolation
X = df[["YearsExperience"]]
y = df["Salary"]

# 4. Train/Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 5. Model Training
model = LinearRegression()
model.fit(X_train, y_train)

# 6. Inference & Evaluation
y_pred = model.predict(X_test)

print(f"Model Coefficient (Slope): {model.coef_[0]:.2f}")
print(f"Model Intercept: {model.intercept_:.2f}")
print(f"R² Score: {r2_score(y_test, y_pred):.4f}")

# 7. Visualization
plt.figure(figsize=(8, 5))
plt.scatter(X, y, color="blue", label="Actual Data")
plt.plot(X_train, model.predict(X_train), color="red", label="Regression Line")
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Years Experience vs Salary")
plt.legend()
plt.show()

```

---

## Results & Insights

* **Correlation:** Demonstrates a strong positive linear relationship between `YearsExperience` and `Salary`.
* **Zero Duplicates / Zero Missing Values:** Quality checks confirm complete dataset integrity.

```

``````markdown
# Simple Linear Regression Pipeline

A clean, modular end-to-end Machine Learning pipeline implementing Simple Linear Regression to predict employee salaries based on years of experience.

---

## Technical Overview

This repository demonstrates the step-by-step implementation of a Simple Linear Regression model using Python. The objective is to establish a linear relationship between an independent feature (**Years of Experience**) and a target variable (**Salary**).


```

[ Data Collection ] ──> [ Data Cleaning ] ──> [ Feature Selection ] ──> [ Model Training ] ──> [ Evaluation ]

```

---

## Dataset Description

The project uses `Salary_dataset.csv`, consisting of 30 records detailing employee experience levels alongside corresponding annual salary figures.

* **Independent Variable ($X$):** `YearsExperience` (Continuous feature in years)
* **Dependent Variable ($y$):** `Salary` (Continuous target variable)
* **Dataset Shape:** 30 rows $\times$ 2 features (after index column removal)

---

## Machine Learning Pipeline

1. **Data Ingestion & Inspection:** Loading raw dataset using `pandas` and analyzing structure.
2. **Data Cleaning & Preprocessing:**
   * Checking for and handling duplicate records.
   * Identifying missing/null values (`df.isnull().sum()`).
   * Dropping irrelevant structural artifacts (e.g., `Unnamed: 0` index column).
3. **Exploratory Data Analysis (EDA):** Visualizing feature relationships using `matplotlib` scatter plots.
4. **Data Splitting:** Partitioning data into training and test datasets.
5. **Model Building & Fitting:** Training a `LinearRegression` model to estimate line parameters (slope and intercept).
6. **Model Evaluation:** Assessing prediction accuracy on holdout test data.

---

## Usage & Implementation

### Prerequisites

```bash
pip install numpy pandas matplotlib scikit-learn

```

### Python Execution Script

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# 1. Load Dataset
df = pd.read_csv("Salary_dataset.csv")

# 2. Data Cleaning
df.drop(columns=["Unnamed: 0"], inplace=True, errors="ignore")

# 3. Feature & Target Isolation
X = df[["YearsExperience"]]
y = df["Salary"]

# 4. Train/Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 5. Model Training
model = LinearRegression()
model.fit(X_train, y_train)

# 6. Inference & Evaluation
y_pred = model.predict(X_test)

print(f"Model Coefficient (Slope): {model.coef_[0]:.2f}")
print(f"Model Intercept: {model.intercept_:.2f}")
print(f"R² Score: {r2_score(y_test, y_pred):.4f}")

# 7. Visualization
plt.figure(figsize=(8, 5))
plt.scatter(X, y, color="blue", label="Actual Data")
plt.plot(X_train, model.predict(X_train), color="red", label="Regression Line")
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Years Experience vs Salary")
plt.legend()
plt.show()

```

---

## Results & Insights

* **Correlation:** Demonstrates a strong positive linear relationship between `YearsExperience` and `Salary`.
* **Zero Duplicates / Zero Missing Values:** Quality checks confirm complete dataset integrity.

```

``````markdown
# Simple Linear Regression Pipeline

A clean, modular end-to-end Machine Learning pipeline implementing Simple Linear Regression to predict employee salaries based on years of experience.

---

## Technical Overview

This repository demonstrates the step-by-step implementation of a Simple Linear Regression model using Python. The objective is to establish a linear relationship between an independent feature (**Years of Experience**) and a target variable (**Salary**).


```

[ Data Collection ] ──> [ Data Cleaning ] ──> [ Feature Selection ] ──> [ Model Training ] ──> [ Evaluation ]

```

---

## Dataset Description

The project uses `Salary_dataset.csv`, consisting of 30 records detailing employee experience levels alongside corresponding annual salary figures.

* **Independent Variable ($X$):** `YearsExperience` (Continuous feature in years)
* **Dependent Variable ($y$):** `Salary` (Continuous target variable)
* **Dataset Shape:** 30 rows $\times$ 2 features (after index column removal)

---

## Machine Learning Pipeline

1. **Data Ingestion & Inspection:** Loading raw dataset using `pandas` and analyzing structure.
2. **Data Cleaning & Preprocessing:**
   * Checking for and handling duplicate records.
   * Identifying missing/null values (`df.isnull().sum()`).
   * Dropping irrelevant structural artifacts (e.g., `Unnamed: 0` index column).
3. **Exploratory Data Analysis (EDA):** Visualizing feature relationships using `matplotlib` scatter plots.
4. **Data Splitting:** Partitioning data into training and test datasets.
5. **Model Building & Fitting:** Training a `LinearRegression` model to estimate line parameters (slope and intercept).
6. **Model Evaluation:** Assessing prediction accuracy on holdout test data.

---

## Usage & Implementation

### Prerequisites

```bash
pip install numpy pandas matplotlib scikit-learn

```

### Python Execution Script

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# 1. Load Dataset
df = pd.read_csv("Salary_dataset.csv")

# 2. Data Cleaning
df.drop(columns=["Unnamed: 0"], inplace=True, errors="ignore")

# 3. Feature & Target Isolation
X = df[["YearsExperience"]]
y = df["Salary"]

# 4. Train/Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 5. Model Training
model = LinearRegression()
model.fit(X_train, y_train)

# 6. Inference & Evaluation
y_pred = model.predict(X_test)

print(f"Model Coefficient (Slope): {model.coef_[0]:.2f}")
print(f"Model Intercept: {model.intercept_:.2f}")
print(f"R² Score: {r2_score(y_test, y_pred):.4f}")

# 7. Visualization
plt.figure(figsize=(8, 5))
plt.scatter(X, y, color="blue", label="Actual Data")
plt.plot(X_train, model.predict(X_train), color="red", label="Regression Line")
plt.xlabel("Years of Experience")
plt.ylabel("Salary")
plt.title("Years Experience vs Salary")
plt.legend()
plt.show()

```

---

## Results & Insights

* **Correlation:** Demonstrates a strong positive linear relationship between `YearsExperience` and `Salary`.
* **Zero Duplicates / Zero Missing Values:** Quality checks confirm complete dataset integrity.

```

```
