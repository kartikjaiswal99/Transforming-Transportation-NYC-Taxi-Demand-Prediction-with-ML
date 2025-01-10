# NYC Taxi Demand Prediction

## Overview
This project focuses on predicting NYC yellow taxi demand, specifically the number of pickups in a region at a particular time. Using machine learning models and historical data, the aim is to forecast taxi demand for better operational efficiency and improved service delivery.

## Objective
The primary objective is to predict the number of pickups in a specified region and its surrounding areas for a given time interval. The predictions are made using data from January 2015 to forecast demand in January 2016.

## Data Information
- **Source**: [NYC Taxi & Limousine Commission Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
- **Period**: January 2015 and January 2016
- **Taxi Type**: Yellow Medallion Taxicabs
  - Yellow taxis provide transportation exclusively through street-hails. They operate within the constraints of medallions issued by the TLC, and pickups are not pre-arranged.

## Problem Formulation
The problem is modeled as a combination of time-series forecasting and regression, aiming to:
- Predict the number of pickups based on location coordinates (latitude and longitude) and time.
- Use historical data from 2015 to forecast demand for 2016.

## Methodology

### Baseline Models
- **Moving Averages**
- **Weighted Moving Averages**
- **Exponential Moving Averages**

### Advanced Models
- **Linear Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**

## Evaluation Metric
- **Mean Absolute Percentage Error (MAPE)**:
  - Measures the percentage error between actual and predicted pickups.
  - Example: If actual pickups = 102 and predicted = 100, MAPE = 2%.

## Results
| Model                              | Train MAPE  | Test MAPE   |
|------------------------------------|-------------|-------------|
| Baseline Model                     | 0.1323      | 0.1447      |
| Exponential Moving Averages        | 0.1261      | 0.1385      |
| Linear Regression                  | 0.1259      | 0.1395      |
| Random Forest Regression           | 0.0904      | 0.1409      |

**Selected Model**: Exponential Moving Averages performed the best with minimal errors and high reliability for real-world predictions.

## Conclusion
This project successfully demonstrated the use of time-series forecasting and regression to predict taxi demand. The Exponential Moving Averages model provided the most accurate results, meeting the constraints of low latency and error tolerance.



