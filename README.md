# Flight-Delay-prediction-using-Pycaret
Here is an update in my previous project. I have used PyCaret library to select the best algorithm to predict Flight delay
This dataset has 13 variables.
- # The description of the data is as below.

w : This column is a number of a month in an year.

DayofMonth: This column has the values of number of a day in a month.

DayOfWeek: This column has the value of a day of a week starting from Monday

DepTime: The actual departure time (local, hhmm)

CRSDepTime: scheduled departure time. (CRS is Computarized Reserved System)

ArrTimeCRSArrTime: Arrival time as per  Computerized Reservations Sysytems

ActualElapsedTime: The physical time that has elapsed since the CRS time

CRSElapsedTime: CRS Elapsed Time of Flight (estimated elapse time), in minutes

ArrDelay: Difference in minutes between scheduled and actual arrival time.

Early arrivals show negative numbers, in minutes

Distance: Distance between airports (miles)

DepDelay: Difference in minutes between scheduled and actual departure time.
Early departures show negative numbers(in minute)
_________________________________________________________________________________________________________________________________________________________________________________
From a technical point of view, the main aspects of python covered throughout the notebook are:

visualization: matplolib, seaborn, basemap
data manipulation: pandas, numpy,pycaret
modeling: sklearn
class definition: Logistic Regression

- # Exploratory Data Analysis

During EDA,the data has around 1 million records. We have treated the missing values by dropping the records with missing data. 
The Federal Aviation Administration (FAA) considers a flight to be delayed when it is 15 minutes later than its scheduled time. Hence in the "DepDelay" column,
we have mutated the data such as , if the flight is delayed by more than 15 minutes, it is considered as delayed(1), otherwise it is not delayed(0).
After EDA part, we have sampled the data randomly into train dataset and test dataset(X_train, y_train, X_test, y_test). The ratio of train to test is 0.8/0.2 .

- # Pycaret library
From Pycaret library we have imported all the libraries.
Then we compare the classification algorithms on the dataset. 
Among the 15 classification algorithms, the best of 3 are Extreme Gradient Boosting, Logistic Regression and Decision tree Algorithm.
We have chosen Logistic regression algorithm to build our model, because I am more familier with that algorithm.
The mean accuracy of 10 fold cross validation is 99.30%
