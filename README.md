#  Smart Plant Growth Monitoring and Prediction System

## 1. Project Overview

The Smart Plant Growth Monitoring and Prediction System is a data-driven web application designed to monitor plant-related information, analyze environmental factors, visualize growth patterns, and predict plant growth-related outcomes using Machine Learning.

The system uses plant attributes such as height, leaf count, watering amount, temperature, humidity, soil moisture, fertilizer, and health score to analyze plant growth.

The project integrates five academic components: **Software Engineering, Probability and Statistics, Data Visualization, Machine Learning, and Full Stack Development.**

## 2. Project Objectives

* Store and manage plant growth records.
* Analyze plant growth and environmental data using statistical methods.
* Visualize plant growth patterns through charts.
* Build a Machine Learning model to estimate `New_Growth_Count`.
* Develop a user-friendly web application for entering plant data and viewing results.
* Integrate all five subject components into one application.

## 3. Implementation Across the Five Subject Components

### 3.1 Software Engineering (SE)

**Objective:** Plan, design, develop, and test the application systematically.

**What I will implement:**

* Define project requirements and scope.
* Prepare the Software Requirements Specification (SRS).
* Identify functional and non-functional requirements.
* Design the system architecture.
* Prepare UML diagrams, including a use-case diagram and activity diagram.
* Design the database structure.
* Test data validation, data storage, analysis, and prediction workflows.
* Document test cases and their results.

**Expected deliverables:**

* SRS document
* System architecture diagram
* UML diagrams
* Test cases and testing report

### 3.2 Probability and Statistics

**Objective:** Analyze plant growth data and understand relationships between variables.

**What I will implement:**

* Calculate mean, median, and standard deviation.
* Summarize numerical plant attributes.
* Analyze the correlation between selected variables.
* Investigate the relationship between soil moisture and new growth.
* Examine missing values and potential outliers.
* Use statistical findings to support feature selection and model evaluation.

**Expected deliverables:**

* Statistical summary
* Correlation analysis
* Outlier analysis
* Interpretation of important statistical findings

### 3.3 Data Visualization (DV)

**Objective:** Present plant growth data in a clear and understandable visual format.

**What I will implement:**

* Create a line chart to explore growth trends when suitable time-based records are available.
* Create a bar chart to compare plant growth values.
* Create a scatter plot to examine soil moisture versus `New_Growth_Count`.
* Create a histogram to understand the distribution of growth values.
* Develop a dashboard to display important plant information, charts, and prediction results.

**Tools:** Matplotlib and/or Chart.js.

**Expected deliverables:**

* Plant growth charts
* Environmental relationship charts
* Data analysis dashboard

### 3.4 Machine Learning (ML)

**Objective:** Develop and evaluate a model that estimates the number of new growth units from plant-related inputs.

**What I will implement:**

1. Load the plant growth dataset.
2. Clean missing and inconsistent values.
3. Encode categorical features.
4. Select relevant input features.
5. Separate the input features (X) and target variable (y).
6. Split the data into training and testing sets.
7. Train a baseline model using Linear Regression.
8. Generate predictions for plant inputs.
9. Evaluate the model using MAE, MSE, RMSE, and R².
10. Compare the model with a simple baseline and improve it if possible.

**Prediction target:** `New_Growth_Count`

**Expected deliverables:**

* Data preprocessing pipeline
* Trained Machine Learning model
* Prediction script
* Model evaluation report

**Important limitation:** The current dataset does not establish a reliable future height for a particular date. Therefore, the initial model targets `New_Growth_Count` rather than claiming to predict future plant height.

### 3.5 Full Stack Development

**Objective:** Develop a web application that connects data entry, storage, analysis, visualization, and prediction.

**Frontend:**

* HTML
* CSS
* JavaScript
* Plant data entry forms
* Dashboard and chart displays

**Backend:**

* Python
* Flask
* Input validation
* Data processing
* Prediction integration

**Database:**

* MySQL
* Plant records
* Growth-related information
* Prediction history

**What I will implement:**

* Create a plant data entry page.
* Validate user inputs.
* Store and retrieve plant records.
* Display statistical summaries and visualizations.
* Connect the trained ML model to the backend.
* Display the estimated `New_Growth_Count`.
* Provide a user-friendly dashboard.

**Expected deliverable:** An integrated web application connecting the frontend, backend, database, and Machine Learning model.

## 4. Dataset Information

The project uses a plant growth dataset containing **1,000 records and 17 original columns**.

Important attributes include:

* `Height_cm`
* `Leaf_Count`
* `New_Growth_Count`
* `Watering_Amount_ml`
* `Watering_Frequency_days`
* `Room_Temperature_C`
* `Humidity_%`
* `Soil_Moisture_%`
* `Fertilizer_Type`
* `Soil_Type`
* `Health_Score`

### Data Preprocessing

The preprocessing workflow includes:

* Inspecting the dataset and data types.
* Checking and handling missing values.
* Checking duplicate records.
* Converting selected categorical variables using One-Hot Encoding.

After encoding `Soil_Type`, `Fertilizer_Type`, and `Pest_Severity`, the dataset contains **1,000 rows and 29 columns**.

The number of columns increases because each categorical variable is represented by multiple indicator columns.

## 5. Overall System Workflow

```text
User
  ↓
Enter Plant Data
  ↓
Frontend
  ↓
Backend and Input Validation
  ↓
Database
  ↓
Data Analysis and Statistics
  ↓
Data Visualization
  ↓
Machine Learning Model
  ↓
Predicted New_Growth_Count
  ↓
Dashboard
```

Software Engineering principles guide the design, development, and testing of the complete workflow.

## 6. Proposed Project Structure

```text
smart-plant-growth/
│
├── README.md
├── requirements.txt
│
├── dataset/
│   ├── plant_growth_dataset.csv
│   └── cleaned_plant_growth.csv
│
├── notebooks/
│   ├── data_cleaning.ipynb
│   ├── statistical_analysis.ipynb
│   ├── data_visualization.ipynb
│   └── model_training.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── statistics_analysis.py
│   ├── visualization.py
│   └── prediction.py
│
├── backend/
│   └── app.py
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── database/
│   └── schema.sql
│
├── tests/
│   └── test_requirements.md
│
└── docs/
    ├── SRS.pdf
    ├── system_architecture.png
    └── uml_diagrams/
```

*This is the proposed repository structure. Files should be added as the corresponding modules are developed.*

## 7. Development Roadmap

| Phase   | Work                                              |
| ------- | ------------------------------------------------- |
| Phase 1 | Requirements, SRS, and system design              |
| Phase 2 | Dataset inspection, cleaning, and encoding        |
| Phase 3 | Statistical analysis and data visualization       |
| Phase 4 | Feature selection, model training, and evaluation |
| Phase 5 | Frontend, backend, and database development       |
| Phase 6 | Model integration, testing, and documentation     |

## 8. Expected Outcomes

* Structured storage of plant growth records.
* Statistical insights into plant growth data.
* Clear visualizations of growth-related patterns.
* A Machine Learning model for estimating `New_Growth_Count`.
* A web application connecting plant data, charts, and prediction results.
* Documentation and testing evidence for all five academic components.

## 9. Future Scope

* Automatic data collection through IoT sensors.
* Weather API integration.
* Mobile application support.
* Plant-care recommendations.
* Evaluation of additional Machine Learning models.
* Plant health alerts and notifications.

These are future enhancements and are not claimed as implemented features of the initial version.

## 10. Conclusion

The Smart Plant Growth Monitoring and Prediction System combines Software Engineering, Probability and Statistics, Data Visualization, Machine Learning, and Full Stack Development into a single project.

The goal is to transform plant-related data into understandable statistical insights, visualizations, and growth-related predictions through a structured and user-friendly application.

