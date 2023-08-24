# Customer_churn
High churn rate is a good indicating that something isn't right with services rendered to customers, as they are able to better services elsewhere. This is a fundamental flaw in ways a business should operate
This repository is written to give a step by step guidance on how customer churn model is created, It contains
## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Contributing](#contributing)

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

## Modeling
In this project, multiple classification models are implemented and trained using the preprocessed telecom churn dataset. The models include:
(Logistic Regression,Random Forest, XGB Classifier,K-Nearest Neighbors, SGD Classifier,'SVC', Naive Bayes, Decision tree,
 
 
Please refer to the provided capstone model notebook in the **notebooks**  folder for detailed implementation of the modeling process.

## Evaluation
The trained models are evaluated using Accuracy, Precision, Recall and AUC_score. These metrics provide insights into the model's performance in predicting customer churn. The evaluation results are as shown below:

![Evaluation](."C:\Users\USER\Pictures\table 1.jpg" "C:\Users\USER\Pictures\Screenshots")

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
