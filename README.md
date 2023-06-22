# <p style="padding:10px;background-color:orange;margin:0;color:black;font-family:newtimeroman;font-size:150%;text-align:center;border: 15px 50px;overflow:hidden;font-weight:500">Credit card fraud detection</p>

<p style="text-align:center; ">
<img src="https://i.pinimg.com/736x/7d/e7/6e/7de76e1dc8e99b90eaa5ca2f94f7b92a.jpg" style='width: 500px; height: 300px;'>
</p>


<p style="text-align:justify; ">
    
The goal with this project is to create a reliable method of detecting faudulent transactions with a model. The performance of the our models will be judged based on Accuracy, Precision, Recall and F1-score. We're looking for a model with a high accuracy and F1-score. However, our selection of model would ultimately also be determined by Precision and Recall rates. For example, if the credit card company loses more money through the missed detection of false negatives over false positives then it would make sense to select a model with the higher recall rate everything else being equal
</p> 


# <p style="padding:10px;background-color:orange;margin:0;color:black;font-family:newtimeroman;font-size:100%;text-align:center;border: 15px 50px;overflow:hidden;font-weight:500">Data</p>

The [dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) has been collected and analysed during a research collaboration of Worldline and the [Machine Learning Group](http://mlg.ulb.ac.be) of ULB (Université Libre de Bruxelles) on big data mining and fraud detection. 

The dataset contains transactions made by credit cards in September 2013 by European cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

# <p style="padding:10px;background-color:orange;margin:0;color:black;font-family:newtimeroman;font-size:100%;text-align:center;border: 15px 50px;overflow:hidden;font-weight:500">Approach</p>

### Here is a breakdown of my approach to the project:

1. Exploratory data analysis (EDA)
2. Data Transformation
3. Modeling (Bootstrap Aggregation, Adaptive Boosting, Decision Trees, Random Forests)
4. Balancing the dataset with SMOTE (Synthetic Minority Over-sampling Technique) 
5. Remodeling
6. Modeling with Neural Networks
7. Post-modeling feature analysis

### I utilized 5 different models in this project:
1. Bootstrap Aggregation 
2. Adaptive Boosting
3. Decision Trees 
4. Random Forests
5. Neural Networks

### Future Considerations 

Given that our Random Forest Classifier (after using SMOTE) produced the most reliable results, i'd like to see how much better gradient boosting might (e.g. XGBboost or LightGBM) would perform. I would be curious about this since these approaches might not yeild the same level of predictive ability given that they could miss an Anomoly (fraudulent transaction) if it was significant enough
