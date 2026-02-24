# Rossman Store Sales

Machine Learning — Final Course Project

## Dataset Information


This dataset was originally used in a [Kaggle competition](https://www.kaggle.com/c/rossmann-store-sales) and it was provided with historical sales data for 1,115 Rossmann stores.

### Features

Most of the fields are self-explanatory. The following are descriptions for those that aren't.

* **Id** - an Id that represents a (Store, Date) duple within the test set
* **Store** - a unique Id for each store
* **Sales** - the turnover for any given day (this is what you are predicting)
* **Customers** - the number of customers on a given day
* **Open** - an indicator for whether the store was open: 0 = closed, 1 = open
* **StateHoliday** - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
* **SchoolHoliday** - indicates if the (Store, Date) was affected by the closure of public schools
* **StoreType** - differentiates between 4 different store models: a, b, c, d
* **Assortment** - describes an assortment level: a = basic, b = extra, c = extended
* **CompetitionDistance** - distance in meters to the nearest competitor store
* **CompetitionOpenSince[Month/Year]** - gives the approximate year and month of the time the nearest competitor was opened
* **Promo** - indicates whether a store is running a promo on that day
* **Promo2** - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
* **Promo2Since[Year/Week]** - describes the year and calendar week when the store started participating in Promo2
* **PromoInterval** - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store


### Pipeline

* # PHASE 1

    * ## 1.1. Loading Data
    * ## 1.2. Descriptive Statistical

* # PHASE 2

    * ## 2.1. Adding new Features
    * ## 2.2. Time-Based Train, validation and test split
    * ## 2.3. Standardization

* # PHASE 3

    * ## 3.1. BasleLine - Moving Average
    * ## 3.2. XGBoost Regressor

        * ### 3.2.1. Encoding Data
        * ### 3.2.2. Custom XGBoostRegressor
        * ### 3.2.3. Parameter Tuning
        * ### 3.2.4. XGBoost Using package (For comparison with the costum XGBoost)
        * ### 3.2.5. XGBoost Using package (fitted on entire dataset)
        * ### 3.2.6. Error Analysis
        * ### 3.2.7. Feature Importance Analysis(SHAP)

* # PHASE 4

    * ## 4.1. Multi-Step Forcasting(7 days)

        * ### 4.1.1. Recursive Multi-Step Forcasting
        * ### 4.1.2. Direct Multi-Step Forcasting

    * ## 4.2. Quantile Regression
    * ## 4.3. Classification

        * ### 4.3.1. Adding label feature and droping closed days
        * ### 4.3.2. Time-Based Split
        * ### 4.3.3. Scaling & standardization
        * ### 4.3.4. Encoding Data
        * ### 4.3.5. Preparing Data
        * ### 4.3.6. Custom XGBoost Classification model
        * ### 4.3.7. Classification Using package(XGBclassifier)

* # PHASE 5

    * ## LSTM
    * ## TCN

