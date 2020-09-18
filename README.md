# UK House Price Prediction - POC

## Summary

This repository explores whether simple time series forecasting methods are able
to predict UK house prices 12 months into the future with an acceptable degree of
accuracy.

## Data

We will use UK house price data from the [Land Registry][#landregistry] website.
More specifically we will use the "Average price by type of property in United
Kingdom" between January 2005 and December 2019. The reason for this is:

- From 2005 the data is also broken down by number of sales, and average price per property type
- It contains a little complexity in the form of the 2007 financial crisis
- We will avoid the complexity of COVID-19 effects in 2020 at this stage

[#landregistry]: https://landregistry.data.gov.uk/app/ukhpi/browse?from=2000-01-01&location=http%3A%2F%2Flandregistry.data.gov.uk%2Fid%2Fregion%2Funited-kingdom&to=2020-08-01

We will use data from 2005 to 2018 as training data, and will predict the average
house price for each month of 2019

## Target

We will aim to have a Normalised Root Mean Squared Error (nRMSE) of less than 5.
We will normalise by dividing the RMSE by the mean value in 2019.