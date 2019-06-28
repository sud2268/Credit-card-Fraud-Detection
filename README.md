# Credit-card-Fraud-Detection
## About
Online transaction fraud detection is the biggest challenging issue for banking systems and financial institutes.This project deals with the problem of credit card fraud over online or offline transaction.  Fraud detection in credit card involves identifying of those transactions that are fraudulent into two classes  of  legit  class  and  fraud  class  transactions,  several techniques are designed and implemented to solve to credit card  fraud  detection  such  as  genetic  algorithm,  artificial neural network etc.

The credit card fraud detection techniques are classified in two general categories: fraud analysis(misuse detection) and userbehavior analysis (anomaly detection).

In this project we will use the following two machine learning algorithms which is under (anomaly detection)  -
- Local Outlier Factor
- Isolated Forest Algorithm

The  data  analysis is done by creating histograms of the variables related to the dataset and by creating co-relation matrix  of  the  variables.  

## Introduction
Fraud detection methods are being developed rapidly in order to adapt with new incoming fraudulent strategies across the world.
The task of detecting fraud transactions in an accurate and efficient manner is fairly difficult and challengeable.

### Difficulties of Credit Card Fraud Detection
- #### Imbalanced data
It means thatvery small percentages of all credit card transactions are fraudulent. This cause the detection of fraud transactions very difficult and imprecise.
- #### Different misclassification importance
in fraud detection task, different misclassification errors have different importance.Misclassification of a normal transaction as fraud is not as harmful as detecting a fraud transaction as normal. Because in the first case the mistake in classification will be identified in further investigations.
- #### Overlapping data
Many transactions may be considered fraudulent, while actually they are normal (false positive) and reversely, a fraudulent transaction may also seem to be legitiate (false negative). Hence obtaining low rate of false positive and false negative is a key
challenge of fraud detection systems

## Prerequisites
### DataSet
#### Note: you have to download datasets containing transactions made by credit cards in September 2013 by european cardholders [dataset Link](https://www.kaggle.com/mlg-ulb/creditcardfraud) 
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

#### Reading the Data Set
In the following cells, we will import our dataset from a .csv file as a Pandas DataFrame. Furthermore, we will begin exploring the dataset to gain an understanding of the type, quantity, and distribution of data in our dataset. For this purpose, we will use Pandas' built-in describe feature, as well as parameter histograms and a correlation matrix.

![credit1](https://user-images.githubusercontent.com/26832674/60330405-fd545600-99af-11e9-87a0-96064cdfc4d6.png)

- In  the  dataset  of 2,84,807  transactions,  492are  fraudulent.
- Dataset  values  are  in  numerical  form  as  PCA  (Principal  Component  Analysis) transformation  is  done  on  input  values.  This  conversion  is  done  so  that  the  user’s  personal  details remain  hidden  and  the  user’s security  is  maintained.

#### Histogram-

- Columns  having  heads  as  V1  to  V28  show  PCA  transformed  numeric  values  but  time,  amount  and  class features show their genuine values.
- Histogram  is  an  accurate  representation  of  the  distribution ofnumerical data.
- Time feature shows the elapsed time between transactions while amount shows actual transaction amount.
- Class is the result variable which gives values in the form of 0 and 1, 1 for fraudulent transactions and 0 for valid transactions.

![credit4](https://user-images.githubusercontent.com/26832674/60330498-3096e500-99b0-11e9-8d5f-db0ae954896f.png)


#### Co-Relation Matrix

- No co-relation between prediction, most fraud transaction done in large amounts.
- No strong co-relation between class, amount or class, time.

![credit3](https://user-images.githubusercontent.com/26832674/60330492-2d035e00-99b0-11e9-99af-dd69c6bdc8e4.png)

#### ALgoroithms
- ##### Local Outlier Factor
The Local Outlier Factor or LOF algorithm is an unsupervised anomaly detection method. It computes the localdeviation of a given a  data point  with respect  to  its neighbours.  Local  Outlier  Factor  considers  as  outliers  thesamples that have  a  substantially  lower density than their neighbours.

- ##### Isolation Forest Algorithm

The IsolationForest ‘isolates’ observations by randomly selecting a feature and then randomly selecting a split value between the maximum and minimum values of the selected feature.

Since recursive partitioning can be represented by a tree structure, the number of splittings required to isolate a sample is equivalent to the path length from the root node to the terminating node.

This path length, averaged over a forest of such random trees, is a measure of normality and our decision function.

Random partitioning produces noticeably shorter paths for anomalies. Hence, when a forest of random trees collectively produce shorter path lengths for particular samples, they are highly likely to be anomalies.


![credit2](https://user-images.githubusercontent.com/26832674/60330486-270d7d00-99b0-11e9-96b1-cf7bd41aed6a.png)

### Refrences

- Visit https://www.irjet.net/archives/V5/i11/IRJET-V5I11304.pdf
- Visit https://acadpubl.eu/jsi/2018-118-7-9/articles/7/31.pdf
- Visit https://arxiv.org/pdf/1811.02196.pdf
- Visit https://towardsdatascience.com/anomaly-detection-with-isolation-forest-visualization-23cd75c281e2
