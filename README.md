# Text-files-Classification
# UBIT: shiyan
# UBIT: weibinma
# Lab 3

<br />

## Part1: Understand Titanic data
<br />
For this part we use python to analysis Titanic dataset, we use 7 methods to predict survive rate, final results were shown as follows:

![Titanic Survival Prediction Accuracy](https://github.com/weibinma/Data_Intensive_Computing-lab3/blob/master/predction%20accuracy.jpg)

<br />
Conclusion: From the final results, we find that Random Forest or Decision Tree methods can help get highest prediction accuracy up to 97 percent, while using Perceptron or SGD learning we only got about 60 percent prediction accuracy.

## Part2: Text files Classification
<br />

### Collect and clean data
<br />
In this part, we use python to collect nytimes articles which include 4 categories [politics, business, sports, science]. We collect 990 politics articles, 990 business articles, 990 sports articles and 990 science articles. Then, we clean all articles using stop_words and regular expression as filter. 
<br />
<br />

![Cleaned keywords](https://github.com/weibinma/Data_Intensive_Computing-lab3/blob/master/text%20files%20classification%20image/top%20key%20words.png)

<br />

### Feature Engineering
<br />
In this part, we choose the top 250 highest frequency words of each category combining them together as the total key words for classification. Remove the repeated words and got 484 unique key words.
<br />
<br />

![Total key words](https://github.com/weibinma/Data_Intensive_Computing-lab3/blob/master/text%20files%20classification%20image/dataframe.png)

<br />
<br />

Finally, we build a DataFrame, in which total 3960 article as row, total key words as column and adding the category label in  last column. Thus, the DataFrame is in a (3960, 484) shape. Next step, we begin to build classification model using this new data frame.
<br />
<br />

### Multi-class Classification
<br />
We build 4 classification models: KNN, Logistic Regression, Random Forest and SVM. And splitting training and test data of the DataFrame in 5:1. Finally, test predicting the accuracy as follows:
<br />
<br />

![](https://github.com/weibinma/Data_Intensive_Computing-lab3/blob/master/text%20files%20classification%20image/test%20accuracy.png)

<br />

Conclusion: From the result above, we can easily find that the Logistic Regression, Random Forest and SVM methods perform better than KNN for classification. Next part, we aim to put new articles (not included in the training data, validation data and test data) and predict the accuracy.

<br />

### Clean new articles
<br />
We clean the new articles and transform them into DataFrame same shape with the original DataFrame; Then doing normalization before predicting.
<br />
<br />

![New test dataframe](https://github.com/weibinma/Data_Intensive_Computing-lab3/blob/master/text%20files%20classification%20image/dataframe_newtest.png)

<br />

### New data prediction
<br />
We perform classification methods and predict unknown set of articles (not test set) and see the results as follows:
<br />
<br />

![Accuracy of new articles prediction](https://github.com/weibinma/Data_Intensive_Computing-lab3/blob/master/text%20files%20classification%20image/new%20articles%20test%20acc.png)

<br />

### Conclusion 
<br />
From the total results, we can easily find that when using new data to test models, the Random Forest, Logistic Regression and SVM models perform better than KNN model again. Thus, we successfully achieve a high accuracy (more than 85%)for classification model and a pretty good accuracy (more than 80%) for new data (no test data) as well.

