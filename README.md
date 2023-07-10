# <center> Study of classification algorithms

## Table of contents
1. [Project Description](#Project-Description)
2. [Data description](#Data-description)
3. [Libraries](#Libraries)
4. [Project Installation](#Project-Installation)
5. [Using the project](#Using)
6. [Authors](#Authors)
7. [Conclusions](#Conclusions)

## Project Description

Some bank has asked you for help: they want to develop a loyalty campaign to retain customers. To do this, he needs to predict the probability of customer outflow and determine whether the customer will leave in the near future.

**Problem** - to build a classifier that will allow timely identification of outgoing bank customers.

**This project** the aim is to build such a model and includes:

* data cleaning (for more information about some of the cleaning methods used, see [here](https://github.com/StartrexII/DataCleaning 'GitHub link'))
* designing features
* feature conversion
* building a logistic regression model and determining the optimal parameters of the model
* building decision tree and random forest models and determining optimal model parameters
* choosing the best algorithm

**О структуре проекта:**
* [data](./data) - the folder with the original tabular data
* [plotly](./plotly) - a folder with charts for viewing them in the browser
* [dataResearch.ipynb](./dataResearch.ipynb) - jupyter-notebook containing an analysis of categorical features
* [ML-3.Practice.Classification.ipynb](./ML-3.Practice.Classification.ipynb) - jupyter-notebook containing the main project code, data processing and algorithm training
* [requirements.txt](./requirements.txt) - a file with the versions of the modules used, for reproducibility of the code

:arrow_up:[To the table of contents](#table-of-contents)

## Data description
 The dataset contains various information about the bank's customers, including the status - whether he is a customer, or has already stopped using the bank's services(**target**) 

### <center> Dataset structure
* **RowNumber** — table row number;
* **CustomerId** — client ID;
* **Surname** — client's last name;
* **CreditScore** — the client's credit rating (the higher it is, the more the client took out loans and returned them);
* **Geography** — client's country of residence (international bank);
* **Gender** — client's gender;
* **Age** — client's age;
* **Tenure** — how many years has the client been using the bank;
* **Balance** — how much money does the client have in bank accounts;
* **NumOfProduct** — number of bank services used by the client;
* **HasCrCard** — does the customer have a credit card (1 — yes, 0 — no);
* **IsActiveMember** — does the client have the status of "active client" (1 — yes, 0 — no);
* **EstimatedSalary** — estimated salary of the client;
* **Exited** — the status of the departed (1 is a departed client, 0 is a loyal client).

:arrow_up:[To the table of contents](#table-of-contents)

## Libraries
* Python (3.11.1):
    * [pandas (2.0.1)](https://pandas.pydata.org)
    * [numpy (1.24.3)](https://numpy.org)
    * [plotly (5.14.1)](https://plotly.com/python/)
    * [matplotlib (3.7.1)](https://matplotlib.org)
    * [seaborn (0.12.2)](https://seaborn.pydata.org)
    * [Category Encoders (2.6.0)](http://contrib.scikit-learn.org/category_encoders/)
    * [scikit-learn (1.2.2)](https://scikit-learn.org/stable/)

:arrow_up:[To the table of contents](#table-of-contents)

## Project Installation

```
    git clone https://github.com/StartrexII/DataScienceProjects
```

:arrow_up:[To the table of contents](#table-of-contents)                        

## Using
Information about the relationships between categorical features is presented in the jupyter-notebook [dataResearch.ipynb](./dataResearch.ipynb).
All other information, including the distribution of numerical features, is presented in the jupyter-notebook [ML-3.Practice.Classification.ipynb](./ML-3.Practice.Classification.ipynb).
If the graphs are not displayed on GitHub, you can open them in the browser, they are in the folder [`plotly/`](./plotly)

:arrow_up:[To the table of contents](#table-of-contents)

## Authors

* [Егор Орлов](https://vk.com/liquidlogic)

:arrow_up:[To the table of contents](#table-of-contents)

## Conclusions

As a result, it was possible to achieve the value of F1-measure 0.68, while trying to use logistic regression, improving it by selecting regularization parameters, adding polynomial features of degree 3, as well as selecting the probability threshold of the object's relation to a certain class. The algorithms of decision trees turned out to be the most effective, while a random forest performed better in the training selection, and its results were comparable to the results of the decision tree in the test sample. At the same time, after selecting the decision-making threshold, the final metric (F1-measure) improved, but it is worth noting that a random forest during selection, in which an optimal balance between completeness and accuracy of the algorithm is achieved, shows a much better metric compared to the decision tree (0.68 - random forest, 0.64 - decision tree).

:arrow_up:[To the table of contents](#table-of-contents)

If the information on this project seems interesting or useful to you, then I will be very grateful to you if you mark the repository and profile with ⭐️⭐️⭐️:)