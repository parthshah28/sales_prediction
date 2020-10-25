# [sales_prediction](https://github.com/parthshah28/sales_prediction)
Predicting future daily sales based on the given features using **fbprophet**.


## Dataset

[Data Source] (https://www.kaggle.com/c/rossmann-store-sales/data)

**Sales Train Data**

almost a million observation;
1115 unique stores 

Note that sales is the target variable (that's what we are trying to predict) 
 
***Id: transaction ID (combination of Store and date),
Store: unique store ID,
Sales: sales/day, this is the target variable, 
Customers: number of customers on a given day,
Open: Boolean to say whether a store is open or closed (0 = closed, 1 = open),
Promo: describes if store is running a promo on that day or not,
StateHoliday: indicate which state holiday (a = public holiday, b = Easter holiday, c = Christmas, 0 = None),
SchoolHoliday: indicates if the (Store, Date) was affected by the closure of public schools***

![](https://github.com/parthshah28/sales_prediction/blob/main/images/1.png)

**Store Info Data**

***StoreType: categorical variable to indicate type of store (a, b, c, d),
Assortment: describes an assortment level: a = basic, b = extra, c = extended,
CompetitionDistance (meters): distance to closest competitor store,
CompetitionOpenSince [Month/Year]: provides an estimate of the date when competition was open,
Promo2: Promo2 is a continuing and consecutive promotion for some stores (0 = store is not participating, 1 = store is participating),
Promo2Since [Year/Week]: date when the store started participating in Promo2,
PromoInterval: describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store***

![](https://github.com/parthshah28/sales_prediction/blob/main/images/2.png)

## Feature Engineering

First I have filled missing variables using average values.

Then I have merged both data frames together based on **'store'**

**the average sales and number of customers per month**

<table><tr><td><img src='https://github.com/parthshah28/sales_prediction/blob/main/images/3.png'></td><td><img src='https://github.com/parthshah28/sales_prediction/blob/main/images/4.png'></td></tr></table>

## Algortithm Used

**Facebook Prophet**
Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data.

<table><tr><td><img src='https://github.com/parthshah28/sales_prediction/blob/main/images/5.png'></td><td><img src='https://github.com/parthshah28/sales_prediction/blob/main/images/6.png'></td></tr></table>



