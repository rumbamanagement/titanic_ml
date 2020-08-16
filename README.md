Titanic: Machine Learning from Disaster is one of the popular ML challenges you will find over internet. This ML challenge is about predicting which passengers survived the Titanic shipwreck.This challenge asks you to build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).This ML project has helped me to learn different classification algorithms and have used few in this project. In addition, this project also gives proper insight on how the different features could be related with the passenger's survival. This project is really interesting and recommend to try if you are a beginner like me.¶

# Data Descriptions
* pclass: Ticket class
* age: Age in years
* sibsp: Number of siblings / spouses aboard the Titanic
* parch: Number of parents / children aboard the Titanic
* Survival: 0 = No, 1 = Yes
* sex
* ticket: Ticket number
* fare: Passenger fare
* cabin: Cabin number
* embarked: Port of Embarkation,C = Cherbourg, Q = Queenstown, S = Southampton

# Data Preprocessing
* The missing values in the train data are identified and analyzed.
* I have dropped few variables from the dataset as it contains the missing values. Cabin variable have 687 missing values which is 77.10 percent of total data set. I assume it would be better to delete such numbers of the missing values. Age variable have 177 missing values and it would be appropriate if it is replaced by median value. Embarked variable only contains 2 missing values and wouldn't be big deal if we delete those 2 missing values.
* I have divided Ticket variable into ticket with numbers and letters. numeric_ticket gives boolean value; 1 shows value is numeric and 0 is non-numeric.
* We have 659 tickets which have numbers only and 230 tickets which have letters.
* Simple Feature scaling, one of the data normalization methods, is used here to normalize Age and Fare variables into a similar range; 0 to 1.
* We follow the same approach to our test dataset in dealing with the missing values and data normalization.

# Exploratory Data Analysis
* Data types are checked. 
* The variables are categorized into numerical and categorical variables.
* The data distribution of the numerical variables are checked.
* Age variable seems roughly bell curved and can be assumed it is normally distributed.
* Name variable is dropped as I see it has no relevant relation in predicting survivals of the passengers.
* Using the barplot, we cans see how the catigorical variables are distributed.
* Groupby method helps to group the variables and derive the meaningful information. In the following information, we can see proportion of male and female who have lived and died due to the crash of the ship.
* The visualization of the numbers of the survivals based on fare they paid, grouped into sex; male and female 
* The visualization of the numbers of the survivals based on the passenger's age, grouped into sex; male and female
* The visualization of the numbers of the survivals based on the numbers of the passenger's siblings and the spouse, grouped into sex; male and female
* The visualization of the numbers of the survivals based on the numbers of the parents and children information, grouped into sex; male and female.
* The visualization of the numbers of the survivals based on Age, grouped into ports of Embarkation.
* The visualization of the numbers of the survivals based on the passenger's age, grouped into ticket class;Upper (1) , Middle (2) and Lower (3).
* We can see the age level of the passengers spending on the tickets, grouped into sex; male and female. The female group had spended more on the tickets, which is more than $ 100.
* The pivot table gives information on the survival of the numbers of male and female based on ticket class.

# Model Building
* Features Encoding; Convering of categorical variables into numerical variables by creating their dummy variables
* Let's split our data into train set and test set.
* Here, I have used three models for this classification project. They are Decision Tree, K Nearest Neighbors (KNN) and Logistic Regression.

# Model Evaluation
* Tuned each model so we will find the best parameters and score. I have used Grid Search algorithm to tune the models; Grid search on Logistic Regression, Grid search on KNN and Grid search on Decision Tree. 

## In this project, K Nearest Neighbors with accuracy 80.2% is the best model to predict the survivals of the passengers. 

# References

https://www.kaggle.com/kenjee/titanic-project-example : I retrieved some code from this notebook. I was not sure what to do with Ticket feature and didn't want to delete it as I think it could be one of the determining factors for the prediction project.
