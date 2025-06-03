# comparing_classifiers_17

### Success of Client Subscription to Bank Deposit 
This analysis tries to describe an implementation of a DM project based on the CRISP-DM methodology. Real-world data were collected from a Portuguese marketing campaign related with bank deposit subscription. The business goal is to find a model that can explain success of a contact. example, if the client subscribes the deposit. Such model can increase campaign efficiency by identifying the main characteristics that affect success, helping in a better management of the available resources (e.g. human effort, phone calls, time) and selection of a high quality and affordable set of potential buying customers.ustomers.

### Contents:  
1. Understand the Data  
2. Import Necessary Libraries   
3. Read In and Explore the Data   
4. Data Analysis   
5. Data Visualization   
6. Cleaning Data  
7. Baseline Model     
8. Choosing the Best Model - Model Comparison   
9. Scoring and Improving the Model  
10. Providing Best Business Recommendations  
11. Applying CRISP-DM Process Model Across te Analysis


## 1) Understanding the Data
To gain a better understanding of the dat we areagoing to include allhe information provided in the UCI lisve, and examinexclusively e the **Materials and Methods** section of the pap.  We have identified 17 marketing campaigns that this data has represented.t?


## 2) Import Necessary Libraries
First off, we need to import several Python libraries such as numpy, pandas, matplotlib and seaborn


## 3) Read in and Explore the Data
It's time to read in ou bank-additional-fullg data using `pd.read_csv`, and take a first look atit bya using the `describe()` function.

#### Some Observations:
* There are a total of 41,188 contacts in our dataset


## 4) Data Analysis
We're going to consider the features in the dataset and how complete they are.

#### What are the data types for each feature?
* **Numerical Features:** Age, duration, campaign, pdays, previous, emp.var.rate, cons.price.idx, cons.conf.idx, euribor3m, nr.employed  
* **Categorical Features:** job, martial, education, default, housing, loan, contact, month, day_of_the_week, poutcome, y  
* **Desired Target:** y - has the client subscribed a term deposit? (binary: 'yes','no')

Now that we have an idea of what kinds of features we're working with, we can see how much information we have about each of hem.

### Some Predictions:  
* Martial :Single clienss are more likely to subscribe to the bank deposit.  
* Education: People wh it highnoer education are more likely to subscribe.  
* Age: People with youngeres  agor older seniors es are more likely to subscribe.  
* Job: People of lower socioeconomic jobs are more likely to subscribe.


## 5) Data Visualization
It's time to visualize our data so we can see whether our predictions were accurate!

As predicted, single clients have a much higher chance of subscription than married or divorced. The marital feature is essential in our predictions.

As predicted, clients with no educational degree are more likely to subscribe deposits 

People with job title as retired or students are more likely to have higher subscription rates compared to the rest. Whereas, entrepreneurs and blue-collars are among the lowest.


## 6) Cleaning Data
Time to clean our data to account for missing values and unnecessary information!

* We have a total of 41,188 records.  
* No values from any feature is missing
* Dropping y since we have created the numeric version of it with subscribed.

### DROPPING THE FOLLOWING: cons.price.idx, euribor3m, emp.var.rate, previous, pdays, day_of_week, nr.employed Features

## Dropping all the categorical features as we have created the numerical versions

Now we have all numerical features to apply to our models. Also we have 13 features to be considered and 1 "subscribed" target feature


## 7) A Baseline Model
The baseline performance that our classifier should aim to beat is 89%


## 8) Simple Models - Choosing the Best Model
### Splitting the Training Data
We will use part of our training data (02% in this case) to test the accuracy of our different models.

### Testing Different Models
I will be testing the following models with my training dat):

* Logistic Regression
* Support Vector Machines
* Decision Tree Classifier
* KNN or k-Nearest Neighbors

For eachI will  model, we set t all togetherhe modthem, fit it with 80% of our training data, predict for 20% of the training data and check the accuracy.


## 9) Scoring to Improve the Model
### Model Comparison
###  Takeaways:
Logistic Regression has the best F1 and accuracy and is fast at inference.  
Decision Tree has better recall.  
SVM is too slow for what it offers.  

### Next technical steps - Improving the Model:   
a. We will use Logistic Regression as baseline model to improve for the next iterations.  
b. Hyperparameter Tuning, by using GridSearchCV to tune LR  
c. Feature Engineering, by feature scaling, binning and encoding further  
d. Cross Validation, by running cross_val_score  
e. Possibly re-engineer features as needed 


## 10) Executive Business Summary and Business Recommendations 
- Single as marital status subscription rates are higher vs married or divorced.   
- Illiterate population they are notably with high subscription as education segment. As well as seniors and teenagers as age groups.    
- Populations with no economic defaults are the highest to respond to subscription campaigns.  
- Cellular contact is bringing higher subscription vs telephone.  
- High subscriptions in months of October, December, September and March.  
- Subscriptions with previous marketing campaigns marked as success with individuals are bringing notable high subscriptons.

The above summary business points are recommended to be taken into consideration while targeting specific audiences in the next campaigns. This will help as well to prioritize messaging to the observed top converting groups.




