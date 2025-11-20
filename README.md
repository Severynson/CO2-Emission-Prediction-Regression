## 🚗 CO₂ Emissions Prediction Project

A two-notebook machine learning workflow for both explainability and high-accuracy prediction

This project explores and predicts CO₂ emissions of automobiles using machine learning.
It now consists of two separate notebooks, each serving a different purpose:

### 🧠 Notebook 1 — **dataset_analytics.ipynb**
Exploring the dataset + explainable modeling

This notebook focuses on understanding the structure, relationships, and underlying patterns of the CO₂ dataset.
Its goal is not to maximize predictive performance, but to use a highly interpretable model (Lasso regression) to uncover:
- Which features most strongly influence CO₂ emissions
- How engine size, vehicle class, fuel type, and transmission contribute to emissions
- Whether regularization helps or harms interpretability
- Whether the dataset contains noise or whether relationships are clean and stable

It includes:
- ✔ Data exploration
- ✔ Cleaning and leakage removal
- ✔ Categorical code decoding (transmission & fuel type)
- ✔ ColumnTransformer with one-hot encoding + numeric normalization
- ✔ Lasso models for multiple α values
- ✔ Coefficient analysis & visualizations
- ✔ Interpretation of real mechanical relationships

This notebook answers the why behind emissions patterns and provides an engineering-level understanding of the dataset.

### 🔧 Notebook 2 — **emissions_prediction.ipynb**

Training the best model for design-stage CO₂ prediction

This notebook focuses on building the most accurate predictive model for estimating emissions during the vehicle design stage.
Here, explainability is less important — the goal is robust accuracy.

It includes:

- ✔ Data preprocessing
- ✔ Train–test split
- ✔ ColumnTransformers for:
  - Linear + MLP models (one-hot + scaling)
  - Tree-based models (ordinal encoding)
- ✔ A unified Pipeline + GridSearchCV exploring:
  - Linear Regression (with polynomial features)
  - Ridge
  - SVR
  - Decision Trees
  - Random Forests
  - Gradient Boosting
  - MLP Neural Networks

✔ Cross-validated R² and RMSE comparisons
✔ Visualization of model performance
✔ Selection of the best-performing model
✔ Final evaluation on the test set
✔ Single-instance prediction example

Currently, RandomForestRegressor produces the strongest performance across both CV metrics and test evaluation.

This notebook answers the how:
How can we build the most accurate model for emissions prediction?

### 📌 Project Motivation
Automakers face increasing pressure to reduce emissions to meet regulatory standards and consumer demand for sustainable vehicles.
This project aims to provide a data-driven decision support tool that can be used even before a prototype is built.
- Using these notebooks, engineers can:
	- Estimate emissions from early design specifications
	- Experiment with design alternatives
	- Optimize components to reduce emissions
	- Make more informed and eco-conscious decisions

### 📊 Features Used
Across both notebooks, the core features used for training include:
- Engine Size (L)
- Number of Cylinders
- Vehicle Class
- Transmission Type
- Fuel Type

Fuel consumption columns are intentionally removed because they create data leakage: manufacturers cannot know these values prior to production.

### ⚙️ Technologies
- Python
- Jupyter Notebook
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

### 🚀 How to Use
#### 1.	Clone the repository
```
git clone <your-repository-url>
cd <project-folder>
```
#### 2.	Install the requirements:
```
pip install -r requirements.txt
```
#### 3.	Open the notebook. Use Jupyter Notebook or VS Code::
```
jupyter notebook
```
#### 4.	Choose your workflow

##### 🔍 If you want to understand the dataset and interpret coefficients
##### Open:
**dataset_analytics.ipynb**
You will be able to:
- Explore the dataset
- Understand relationships between features
- Analyze coefficients of a simple, explainable Lasso model

##### 🤖 If you want to train the best predictive model
##### Open:
**emissions_prediction.ipynb**
You will be able to:
- Train & compare multiple ML models
- Visualize performance
- Select the best model
- Predict emissions for new vehicle prototypes

### 📁 Dataset
The project uses the CO₂ Emissions dataset collected by Canadian government, posted on Kaggle:
https://www.kaggle.com/datasets/debajyotipodder/co2-emission-by-vehicles?resource=download