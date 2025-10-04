This repository contains a prescriptive, step-by-step solution to a regression assignment using the California Housing dataset. It implements and compares five algorithms with clear preprocessing and evaluation:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

Gradient Boosting Regressor

Support Vector Regressor (SVR, RBF)

**TL;DR**

Open and run ML-Regression.ipynb top-to-bottom.
You’ll get a table of MSE, MAE, R² and an automatic best vs. worst model summary.

**Dataset**

Source: sklearn.datasets.fetch_california_housing(as_frame=True)

Features (8): MedInc, HouseAge, AveRooms, AveBedrms, Population, AveOccup, Latitude, Longitude

Target: MedHouseVal = median house value ($100,000s)

*Note:* The dataset typically has no missing values, but we still guard against them with a median imputer.

**How the solution is structured**
Preprocessing

Missing values: SimpleImputer(strategy="median")

Scaling: StandardScaler() for Linear Regression and SVR (scale-sensitive).
Tree models (Decision Tree, Random Forest, Gradient Boosting) do not require scaling.

**Models & Key Settings**

Linear Regression: defaults

Decision Tree Regressor: defaults, random_state=42

Random Forest Regressor: n_estimators=300, random_state=42, n_jobs=-1

Gradient Boosting Regressor: defaults, random_state=42

SVR (RBF): kernel="rbf", C=10.0, epsilon=0.1

Each model is wrapped in a Pipeline to prevent leakage (fit on train only).

**Metrics (on test set)**

MSE – lower is better

MAE – lower is better

R² – higher is better

*The notebook prints a sorted results table (highest R² first) and then prints best and worst model rows with a short justification.*
