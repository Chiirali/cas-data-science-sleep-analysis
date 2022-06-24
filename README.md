# CAS Data Science Projekt Sleep Analysis

## Data Sources

**Moon Phases**

Date: 03.04.2022
Source: `https://www.timeanddate.de/mond/phasen/` (Location: Basel). Manual download into a CSV without lunation and duration
Files: 
- `raw/moon/*`

**Sleep Data**

Date: 18.06.2022
Source: export of complete fitbit data of privat account
Files: 
- `raw/sleep/*` 
- `raw/heart/*` 
- `raw/temp/*`


## Preprocessing
- Cleaning and transformation of data
- Merge data sets on attribute 'date'


## Master DataFrame after preprocessing

| date     | temperature | overall_score | composition_score | revitalization_score | duration_score | deep_sleep_in_minutes | resting_heart_rate | restlessness | bpm       | Moon Phase    |
|----------|-------------|---------------|-------------------|----------------------|----------------|-----------------------|--------------------|--------------|-----------|---------------|
| 04.03.22 | -2.494845   | 67            | 17                | 15                   | 35             | 66                    | 60                 | 0.073479     | 68.873969 | New Moon      |
| 19.04.22 | -2.374779   | 75            | 16                | 17                   | 42             | 62                    | 52                 | 0.071966     | 62.836604 |               |
| 10.03.22 | -3.100641   | 88            | 21                | 22                   | 45             | 126                   | 60                 | 0.054695     | 67.206731 | First Quarter |
| 25.04.22 | -3.082295   | 56            | 15                | 15                   | 26             | 23                    | 56                 | 0.100186     | 67.187992 | Third Quarter |
| 08.06.22 | -2.983674   | 75            | 20                | 19                   | 36             | 69                    | 55                 | 0.087816     | 69.163313 | First Quarter |
| 01.01.22 | -2.14144    | 68            | 19                | 18                   | 31             | 69                    | 60                 | 0.081197     | 61.607115 | New Moon      |
| 15.01.22 | -0.019856   | 61            | 17                | 10                   | 34             | 70                    | 57                 | 0.14459      | 68.972063 |               |
| 14.01.22 | -1.975761   | 77            | 21                | 20                   | 36             | 82                    | 59                 | 0.089701     | 68.562845 |               |
| 09.06.22 | -2.748225   | 76            | 22                | 16                   | 38             | 88                    | 54                 | 0.07064      | 59.214786 | First Quarter |
| 24.04.22 | -2.648158   | 68            | 16                | 15                   | 37             | 49                    | 54                 | 0.079038     | 76.126033 | Third Quarter |



### Impact Moon

The moon phases do not seem to have a significant influence on my sleep:

![moon](images/impact-moon.png)



-> first did some general preparation of the data for linear regression

### Linear Regression (Sklearn)


**Sklearn Validation Set Measured vs Fitted**

MSE: 10

![validation](images/sklearn_validation.png)


**Sklearn Test Set Measured vs Fitted**

Test Set MSE: 4

![test](images/sklearn_test.png)


### Linear Regression (Statsmodels)

MSE: 32.5

![statsmodels](images/statsmodels.png)



