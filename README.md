# CPI Indices and Inflation Rate Time Series Analysis and Forecasting 

## Aim

The aim of this project is to analyse South African CPI and inflation rate data using time series methods and to generate forecasts of future values. The models applied include SARIMAX and Prophet, and their performance is compared to determine which provides more accurate forecasts.

## Description of Data

The data was obtained from [StatsSA](http://www.statssa.gov.za/) and is publicly available in PDF format. It consists of:  
- Monthly CPI indices from 1980 to 2025  
- Inflation rates from 1911 to 2025 for each month  

Data preprocessing steps included:  
- Converting the PDF to CSV format  
- Concatenating split tables for inflation rates  
- Correcting indexing and formatting of headings  
- Handling missing values  
- Converting values to float (replacing decimal commas with decimal points)  
- Transforming data from wide to long format for time series analysis

![Average Annual CPI Indices](images/ave_cpi_indices)
![Average Annual Inflation Rate](images/ave_inflation_rates)

## Tools
- Python 
- Jupyter Notebook



## Insights

### CPI Analysis:
Both the Prophet and SARIMAX(1,1,1)(0,1,1)[12] models provide reliable forecasts of CPI trends, capturing long-term patterns and seasonal dynamics. However, the SARIMAX model outperforms Prophet in terms of predictive accuracy. While Prophet achieves an R² of 0.74, an MAE of approximately 4.34, and a MAPE of around 4%, the SARIMAX model attains a much higher R² of 0.987, with lower errors (MAE ≈ 0.96, MAPE ≈ 1.1%). This indicates that SARIMAX more closely matches the actual CPI values and produces more precise forecasts, making it the preferred choice for accurate short- and medium-term CPI prediction.

### Inflation Rate Analysis:
While the model used in Prophet captures long-term historical patterns in the inflation rate, its predictive performance on recent data is less accurate, as actual values deviate from the forecast. Further analysis of the stationarity of the series, along with appropriate transformations or alternative modelling approaches, can be undertaken to improve the accuracy and robustness of the results.

## Project Report
[Download the project report](CPI_Inflation_Project.pdf)


## Acknowledgements
- Data provided by [StatsSA](http://www.statssa.gov.za/)  
