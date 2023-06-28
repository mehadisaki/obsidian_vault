
#### Granger’s Causality Test

Granger’s causality test can be used to identify the relationship between variables prior to model building. This is important because if there is no relationship between variables, they can be excluded and modeled separately. Conversely, if a relationship exists, the variables must be considered in the modeling phase.

The test in mathematics yields a p-value for the variables. If the p-value exceeds 0.05, the null hypothesis must be accepted. Conversely, if the p-value is less than 0.05, the null hypothesis must be rejected.

## Train-Validation Split

If you have worked with univariate time series data before, you’ll be aware of the train-validation sets. The idea of creating a validation set is to analyze the performance of the model before using it for making predictions.

Creating a validation set for time series problems is tricky because we have to take into account the time component. ==One cannot directly use the _train_test_split_ or _k-fold_ validation since this will disrupt the pattern in the series. The validation set should be created considering the date and time values.

Suppose we have to forecast the temperate diff, dew point, cloud percent, etc., for the next two months using data from the last two years. ==One possible method is to keep the data for the last two months aside and train the model for the remaining 22 months.

Once the model has been trained, we can use it to make predictions on the validation set. Based on these predictions and the actual values, we can check how well the model performed and the variables for which the model did not do so well. And for making the final prediction, use the complete dataset (combine the training data and validation sets).


==Aa any other ML problem, we have to divide our data into features and labels. 

In this case our feature is effectively a number of values in the series, with our label being the next value. We'll call that number of values that will treat as our feature, the window size, where we're taking a window of the data and training an ML model to predict the next value. 

So for example, if we take our time series data, say, 30 days at a time, we'll use 30 values as the feature and the next value is the label. Then over time, we'll train a neural network to match the 30 features to the single label.


# Sequence bias

Sequence bias is when the order of things can impact the selection of things. For example, if I were to ask you your favorite TV show, and listed "Game of Thrones", "Killing Eve", "Travellers" and "Doctor Who" in that order, you're probably more likely to select 'Game of Thrones' as you are familiar with it, and it's the first thing you see. Even if it is equal to the other TV shows. So, when training data in a dataset, we don't want the sequence to impact the training in a similar way, so it's ==good to shuffle them up.

## Time-series split
univariate time series you can always convert them into regression problems and solve them as in this example. However, you have to be careful about cross-validation. You cannot do random cross-validation on time-series models and you must use time-series appropriate techniques.In this example, PyCaret uses [TimeSeriesSplit](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.model_selection) from the scikit-learn library.


## Python Time series library

### Facebook Prophet

**Prophet is open-source software released by Facebook's Core Data Science team. It is available for download on CRAN and PyPI.**

Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well.

### pmdarima

Pmdarima is a statistical library designed to fill the void in Python's time series analysis capabilities. This includes:

-   The equivalent of R's auto.arima functionality
-   A collection of statistical tests of stationarity and seasonality
-   Seasonal time series decompositions
-   Cross-validation utilities
-   A rich collection of built-in time series datasets for prototyping and examples

To learn more about pmdarima, check out [this page](https://github.com/alkaline-ml/pmdarima).

### PyCaret

PyCaret is an open-source, low-code machine learning library in Python that automates machine learning workflows. With PyCaret, you spend less time coding and more time on analysis. You can train your model, analyze it, iterate faster than ever before, and deploy it instantaneously as a REST API or even build a simple front-end ML app, all from your favorite Notebook.

![PyCaret Time Series Module Architecture. Developed by Lead Developer Nikhil Gupta.](https://res.cloudinary.com/dyd911kmh/image/upload/v1645628385/image20_l0zp1q.png)

