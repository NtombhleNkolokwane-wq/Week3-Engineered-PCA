# Steel Plant Energy Consumption Prediction using PCA and Flask

## Project Overview

This project was completed as **Week 3** of the AI/ML Internship Program. It builds upon the work completed during Week 2 by applying **Principal Component Analysis (PCA)** for dimensionality reduction and deploying the trained machine learning model through a **Flask web application**.

The project demonstrates a complete machine learning workflow, beginning with data preprocessing and feature engineering, followed by dimensionality reduction, model evaluation, and finally deployment of the best-performing model as a web application for predicting industrial energy consumption.

---

## Objectives

The objectives of this project were to:

- Apply Principal Component Analysis (PCA) to reduce feature dimensionality.
- Compare model performance before and after dimensionality reduction.
- Analyze explained variance and determine the optimal number of principal components.
- Evaluate whether PCA improves computational efficiency while maintaining prediction accuracy.
- Deploy the trained Random Forest model using the Flask web framework.
- Build an interactive web dashboard capable of displaying visualizations and predicting energy consumption.

---

## Dataset

The project uses the **Steel Industry Energy Consumption Dataset**, containing operational measurements collected from a steel manufacturing plant.

The dataset includes variables such as:

- Usage of electrical energy
- Lagging current reactive power
- Leading current reactive power
- Power factor
- CO₂ emissions
- Load type
- Week status
- Day of the week
- Hour of the day
- NSM (Number of Seconds from Midnight)

Additional engineered features created during Week 2 were also used for model training.

---

## Project Workflow

### Part 1 – Principal Component Analysis (PCA)

The following tasks were completed:

- Loaded the engineered dataset from Week 2.
- Applied StandardScaler for feature scaling.
- Performed PCA using all available features.
- Plotted the explained variance ratio.
- Plotted cumulative explained variance.
- Identified the number of components required to preserve approximately 95% of the total variance.
- Retrained the Random Forest model using:
  - Original engineered features
  - Three principal components
  - Components explaining 95% of the variance
- Compared model performance using RMSE and R².
- Created a PCA loading heatmap.
- Documented findings regarding dimensionality reduction.

---

### Part 2 – Flask Dashboard

A Flask web application was developed to deploy the trained machine learning model.

The application includes:

- Home page
- Dashboard page
- Prediction page

The dashboard displays visualizations generated during Week 2, while the prediction page allows users to enter feature values and receive predicted energy consumption values using the trained Random Forest model.

---

## Machine Learning Model

The following regression models were evaluated during Week 2:

- Linear Regression
- Ridge Regression
- Decision Tree Regressor
- Random Forest Regressor

Random Forest achieved the best predictive performance and was therefore selected for deployment.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Flask
- Jupyter Notebook
- Visual Studio Code

---

## Project Structure

```
Week3_Project/
│
├── app.py
├── model.joblib
├── README.md
├── requirements.txt
├── .gitignore
│
├── Data/
│
├── Notebook/
│   └── Week3_PCA.ipynb
│
├── static/
│   ├── energy_hour.png
│   ├── load_type.png
│   ├── correlation_heatmap.png
│
└── templates/
    ├── index.html
    ├── dashboard.html
    └── predict.html
```

---

## Installation

Clone the repository:

```bash
git clone <repository_link>
```

Navigate to the project folder:

```bash
cd Week3_Project
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the Flask application:

```bash
python app.py
```

Open your browser and visit:

```
http://127.0.0.1:5000/
```

---

## Results

The PCA analysis demonstrated that most of the dataset's information could be retained using a reduced number of principal components. Model comparisons showed that Random Forest remained the best-performing algorithm, balancing predictive accuracy and robustness.

The Flask deployment successfully transformed the machine learning model into an interactive web application capable of generating real-time energy consumption predictions.

---

## Learning Outcomes

Through this project, the following skills were developed:

- Principal Component Analysis (PCA)
- Dimensionality Reduction
- Feature Scaling
- Model Evaluation
- Random Forest Regression
- Model Serialization using Joblib
- Flask Web Development
- Machine Learning Deployment
- Git and GitHub Version Control

--

AI/ML Internship Program – Week 3
