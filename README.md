## 🚗 CO₂ Emissions Prediction Project

This project uses machine learning to predict CO₂ emissions of automobiles based on various design and performance features. Built as a Jupyter Notebook, this tool is intended to support automobile manufacturers in designing more sustainable and environmentally friendly vehicles.

### 📌 Project Motivation
Automakers worldwide face increasing pressure to reduce vehicle emissions to meet environmental regulations and consumer demand for greener cars. This project aims to provide a data-driven tool for predicting CO₂ output based on pre-production vehicle specifications.

By inputting design features (like engine size, fuel type, number of cylinders, etc.), engineers can:
	•	Estimate emissions before production
	•	Experiment with different design choices
	•	Optimize for lower emissions
	•	Accelerate eco-conscious decision-making

### 📊 Features Used
The model uses several vehicle attributes to predict CO₂ emissions, including:
	•	Engine Size
	•	Fuel Consumption (City & Highway)
	•	Fuel Type
	•	Number of Cylinders
	•	Transmission Type
	•	…and more

These features are based on real-world vehicle data and are chosen for their known correlation with emissions.

### ⚙️ Technologies
	•	Python
	•	Jupyter Notebook
	•	Pandas, NumPy
	•	Scikit-learn
	•	Matplotlib

### 🚀 How to Use
	1.	Clone the repository, open the project's folder
    2.	Install the requirements:
        pip install -r requirements.txt
    3.	Open the notebook with your favorite IDE:
        jupyter notebook CO2_Emissions_Predictor.ipynb
    4.	Follow the notebook steps to:
	    •	Load and explore the dataset
	    •	Preprocess and visualize the data
	    •	Train and evaluate a regression model
	    •	Make predictions using your own design inputs

### 📁 Dataset
The dataset used for this project is based on publicly available emissions data. See the notebook for a detailed description and link: https://www.kaggle.com/datasets/debajyotipodder/co2-emission-by-vehicles?resource=download