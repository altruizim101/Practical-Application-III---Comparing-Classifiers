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
- READMe file with summary of findings >>  [https://github.com/altruizim101/ ... /edit/main/README.md](https://github.com/altruizim101/Practical-Application-III---Comparing-Classifiers/blob/main/README.md)
- Link to Jupyter notebook here >>         https://github.com/altruizim101/Practical-Application-III---Comparing-Classifiers/blob/main/mod17_PracticalApplication_III.ipynb
- Data Analysis & Results >>               [https://github.com/altruizim101/ ... /edit/main/README.md](https://github.com/altruizim101/Practical-Application-III---Comparing-Classifiers/blob/main/README.md)

 
## (Data Understanding/ Understand Features)
I reveiwed features and attributes of the data, using Pandas tool and its functions. I loaded data and reviewed summary of data content using the pandas methods:
data.head(), data.info(), data.sample(), data.shape()...

Checked for Null (NaN) values possibly captured in data to remove before analysis. Removed NaN data as appropriate.
Action: removed missing (NaN) data in columns

## (Engineering Features)
Build a basic model to get started. First, encode the data. Using just the bank information features, prepare the features and target column for modeling with appropriate encoding and transformations.
After data prepared, split data into a train and test set.

## (Modeling - A Baseline Model)
Before building first model, we establish a baseline and observe its performance that our classifier should aim to beat.
mse_baseline_train = 0.11140785959557421
mse_baseline_test = 0.11556202961883952

## (Modeling - A Simple Model)

## (Modeling - Comparing The Model)

## (Improving The Model - Hyperparameter Finetuning)

## Next Steps & Recommendations
Overall, the following observations and recommendations are noted:
