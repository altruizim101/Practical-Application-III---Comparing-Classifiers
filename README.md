# Practical-Application-III: Comparing-Classifiers

## (Goal & Objective)
The goal of this exercise is to compare the performance of the classifiers we encountered in this section, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. 
We utilize a dataset related to marketing bank products over the telephone.

Data Source: ---- https://archive.ics.uci.edu/dataset/222/bank+marketing

Two available datasets: 
1) bank-additional-full.csv with all examples (41188) and 20 inputs, ordered by date (from May 2008 to November 2010), 
     very close to the data analyzed in [Moro et al., 2014]
2) bank-additional.csv with 10% of the examples (4119), randomly selected from 1), and 20 inputs.
   
## Deliverables
The final submission should include the Jupyter Notebook and other relevant files, such as the dataset provided and uploaded to a GitHub repository.

## Links to Project Deliverables
- READMe file with summary of findings >>  https://github.com/altruizim101/Practical-Application-III---Comparing-Classifiers/tree/main
- Link to Jupyter notebook here >>         https://github.com/altruizim101/Practical-Application-III---Comparing-Classifiers/blob/main/mod17_PracticalApplication_III.ipynb
- Data Analysis & Results >>               https://github.com/altruizim101/Practical-Application-III---Comparing-Classifiers/tree/main
- 
## (Data Understanding/ Understand Features)
I reveiwed features and attributes of the data, using Pandas tool and its functions. I loaded data and reviewed summary of data content using the pandas methods:
data.head(), data.info(), data.sample(), data.shape()...

I checked for possible Null (NaN) values in data for removal before analysis. Then filtered NaN data as appropriate.
Action: removed missing (NaN) data in columns

## (Engineering Features)
fo rthis secion, I encode the data using just bank information features, prepared the features and target column for modeling with the appropriate encoding and transformations.
After data prepared, I then split data into a train and test set.

## (Modeling - A Baseline Model)
The performance results for the established Baseline model for our classifier is:

- mse_baseline_train = 0.11140785959557421
- mse_baseline_test = 0.11556202961883952

## (Modeling - A Simple Model)
Next, we build a Simple model Classifier using Logidtic Regression and observed the performance compared to the Baseline model.
For the same dataset, using similar metric for comparison to Baseline model, the Simple model performed comparable to this Baseline model.

- mse_baseline_train = 0.11140785959557421
- mse_baseline_test = 0.11556202961883952

The model performed fairly well, with accuracy score of:
- accuracy =  0.8844379703811605

## (Modeling - Comparing The Model)
With Baseline established and Simple model using Logistic Regression available, I proceeded with comparing the performance of the Logistic Regression model to the KNN algorithm, Decision Tree, and SVM models. 
Using the default settings for each of the models, I also fit and score each of these models. 
Next, I compared the required "time to fit" each of the models. The data is presented in a DataFrame below:
##
Indx          Model          TrainTime(sec)          Accuracy

A) LogReg:     0.087551                0.910091
B) KNN:        0.036798                0.898681
C) DTree:      0.158389                0.888646
D) SVM:        3.816918                0.909687

From the data in Table above, in terms of Accuracy: 
- Logistic Regression and SVM performed the best and comparable
- KNN is next followed by Decision Tree

From the data in Table above, in terms of Training Time:

- KNN performed best (shortest training time.
- In second place was KNN, and folloed by Decision Tree
- SVM performed worst (longest time to train)


## (Improving The Model - Hyperparameter Finetuning)

## Next Steps & Recommendations
Using these basic models, we proceed to improve these models through exploration of Hyperparameter tuning and grid search. 
Fortunately, all of the above models have additional hyperparameters to tune:

- In KNN, the number of neighbors.
- In Decision Tree, the maximum depth of a Decision Tree.
- In SVM, the value of Gamma.
- In Logistic Regression, the type of algorithm for optimization.

The results from Hyperparameter Tuning given below:

- LogReg {'models__C': 1, 'models__solver': 'liblinear'} 0.9110334007146885
- knn {'models__n_neighbors': 7, 'models__weights': 'uniform'} 0.904269907708052
- DTree {'models__max_depth': 5, 'models__min_samples_split': 2} 0.912247233457961
- SVM {'models__C': 1, 'models__gamma': 'scale', 'models__kernel': 'linear'} 0.9042351795151056

Following a structured approach, we explored with various models for classification and evaluated peroformance taking into account trade-offs in terms of 

- Accuracy
- Training Time
- Optimization through Hyperparameter Tuning

This provided us the ability to make better informed decision as to choice of classifier to employ for a given use case and constraints.




