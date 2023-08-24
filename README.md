# Customer_churn
This repository is written to give a step by step guidance on how customer churn model is created.
High churn rate is a good indicating that something isn't right with services rendered to customers, as they are able to better services elsewhere. This is a fundamental flaw in ways a business should operate

This Readme file provides an overview of the project, instructionfor running the model and few additional information
## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [EDA](#eda)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Contributions](#contributing)

## Project Overview
The objective of this project is to build a supervised machine learning model that can predict Customer Churn based on certain features such as Tenure, type of contrat signed by customers, payment method, Total Charges, Phone/Internet Service. The model is trained on a labeled dataset and uses Classification /regression techniques to make predictions.

## Installation
To use the Customer Churn Prediction Model, follow these steps:

a. Clone this repository to your local machine or download the source code as a ZIP file.
b. Make sure you have Python 3 installed on your system.
c. Install the required packages to be able to run the evaluation locally.

Windows:

 ```bash
 python -m venv venv; venv\Scripts\activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt 
 ``` 
Linux & MacOs:

  ```bash
  python3 -m venv venv; source venv/bin/activate; python -m pip install -q --upgrade pip; python -m pip install -qr requirements.txt
  ```  
The both long command-lines have a same structure, they pipe multiple commands using the symbol ; but you may manually execute them one after another.

1.**Create the Python's virtual environment** that isolates the required libraries of the project to avoid conflicts;

2.**Activate the Python's virtual environment** so that the Python kernel & libraries will be those of the isolated environment;

3.**Upgrade Pip, the installed libraries/packages manager** to have the up-to-date version that will work correctly;

4.**Install the required libraries/packages** listed in therequirements.txt` file so that it will be allow to import them into the python's scripts and notebooks without any issue.

NB: For MacOs users, please install Xcode if you have an issue.

## Usage
a. Prepare your input data in a compatible format. Refer to the [Dataset](#dataset) section for more information on the input format.
b. Run the prediction script using the following command:

   python predict.py --input <path_to_input_data>

   Replace `<path_to_input_data>` with the actual path to your input data file.
c. The model will process the input data and generate Customer Churn predictions. The results will be displayed on the console.

## Dataset
The Customer Churn Prediction Model is trained on a dataset containing a collection of features related to telecom customers. The dataset includes the following features:


- gender
- SeniorCitizen
- Partner
- Dependents
- tenure
- PhoneService
- MultipleLines
- InternetService
- OnlineSecurity
- OnlineBackup
- DeviceProtection
- TechSupport
- StreamingTV
- StreamingMovies
- Contract
- PaperlessBilling
- PaymentMethod
- MonthlyCharges
- TotalCharges

Each data point in the dataset consists of these features along with the churn value. The dataset is split into training and testing sets for model evaluation.

## (EDA) Exploratory Data Analysis 📊 
Before building the churn prediction model, we performed exploratory data analysis (EDA) to gain insights into the dataset and understand the relationships between variables.

Some of the key EDA steps performed in this project include:

a.**Descriptive Statistics**
To gain a better understanding of the dataset, computed descriptive statistics was computed for the numerical variables. These statistics include measures such as mean, median, standard deviation, minimum, maximum, and quartiles for numerical variables. Also descriptive stastistics was also done categorical variables

b.**Data Visualization**
Data visualization plays a crucial role in EDA, allowing us to uncover patterns, trends, and relationships in the data. various visualizations created to uncover the patters and trends of the data, including:

Bar plots and pie charts: To understand the distribution of numerical and categorical variables, respectively.

![churn uni pie](https://github.com/adeleyestella/Customer_churn/assets/132029424/86acb8d8-fe57-47e1-8277-8028d1f01930)

![contra churn total](https://github.com/adeleyestella/Customer_churn/assets/132029424/47e0483a-b70f-48e5-9ce9-fdc1b2cb047b)

Box plots: To identify outliers and examine the distribution of numerical variables across different categories.
![m charges](https://github.com/adeleyestella/Customer_churn/assets/132029424/8d417b32-5297-4f87-989f-07069f415a2b)

Scatter plots: To explore relationships and correlations between pairs of variables.

![s plot](https://github.com/adeleyestella/Customer_churn/assets/132029424/a14514a8-097d-449e-87d7-e75d7b47d251))

Heatmaps and correlation matrices: To visualize the correlation between variables and identify potential multicollinearity.
![correlatn](https://github.com/adeleyestella/Customer_churn/assets/132029424/12618b2e-a6bb-483c-9206-52c4d8b1f9e6)




Please refer to the provided EDA notebook in the **notebooks**  folder for detailed implementation and visualizations related to the EDA process.

c. **Data Cleaning and Preprocessing**: Before diving into the analysis,  data cleaning was conductedand preprocessing steps to ensure the dataset's quality and prepare it for analysis. This process involved:

d. **Handling missing values**: missing values in the dataset was identified and was filled with mean value of the column. 

e. **Handling duplicates**: checked for aduplicated records to avoid redundancy and ensure data integrity but there was no duplicate value.

f. **Data transformation**: performed necessary transformations on the data, such as converting data types, scaling numerical features, encoding categorical variables, and creating derived features.

## Model Training
In this project, multiple classification models are implemented and trained using the preprocessed telecom churn dataset. The models include:
(Logistic Regression,Random Forest, XGB Classifier,K-Nearest Neighbors, SGD Classifier,'SVC', Naive Bayes, Decision tree,
 
Please refer to the provided capstone model notebook in the **notebooks**  folder for detailed implementation of the modeling process.

## Evaluation
The trained models are evaluated using Accuracy, Precision, Recall and AUC_score. These metrics provide insights into the model's performance in predicting customer churn. The evaluation results are as shown below:

![table 1](https://github.com/adeleyestella/Customer_churn/assets/132029424/835d355d-6f51-416d-8099-7c65b7d7435a)


All the models has accuracy not less than 72%

Since ROC(AUC) Score of Logistic Regression  XGB Classifier, Random Forest and Naïve Bayes is higher than 50% . It can be concluded that is not a mere guessing prediction even though it not up to 90%(Excellent Prediction) or 100% (Perfect Model)

**In all the models  Logistic Regression, Naive Bayes, XGB and SVC tends to be doing better**

## Contributions
Contributions and pull requests are welcome! If you would like to contribute to this project, please follow these steps:

1.Fork this repository.\
2.Create a new branch with a descriptive name\
3.Make your desired changes and commit them.\
4.Push the branch to your forked repository.\
5.Open a pull request in this repository and describe your changes.

Feel free to contribute to different areas of the project, including improving the model, exploring additional features, or enhancing the EDA.

## AUTHOR 
Olaide Stella Adeleye
