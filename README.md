Practical Application Assignment 2 - This assignment is to analyze What Drives the Price of a Car?

Data Overview:
- The provided dataset contains information on 426K cars
- About 234k data does not have null values
- By further filtering cars priced between $1,000 & $100,000 + Odometer < 500,000 + cars after 1990 we arrive at 213k cars

Data Analysis:
By observing the dummy columns correlation values, it is clear:
1. Condition values New, Like New and Good condition have a positive impact on price (as expected).
2. Title Status column with values Salvage, Rebuilt, Missing, Parts only condition has negative impact on price (as expected)
   Also the number of cars sold with clean title is highest
3. Transmission column with value other seems to have a positive impact on price (was expecting automatic to have the most positive impact, but does not seem to be the case)
4. By grouping the cars based on Odometer reading (groups of 25000), the price of the cars reduces as the odometer increases
5. Now by adding an additional feature of the car Transmission = ‘Automatic’, the price of the car has improved (as expected) even though a nominal amount
6. The price prediction of the car with input Odometer = 50,000 & Year = 2020 & Transmission = Automatic
   With Linear regression the car was priced $29,700.05
   With LASSO regression the car was priced $28,310.03
   Which are very close

Deliverables:
What factors make a car more or less expensive? [Plots charted to indicate this influencing factors]
- More recent year cars fetch a better price [Positive Correlation]
- Cars with less odometer reading fetch a better price [Negative Correlation]
- Cars with condition 'New', 'Like new', 'Good' condition fetch a better price [Positive Correlation]
- Cars with title 'Salvage', 'Rebuilt', 'Parts only', 'Missing' have a negative price impact [Negative Correlation]
- Folks do not prefer cars with 'Manual' Transmission [Very less inventory compared to other transmission types]

If you are able to collect more of these factors, you can fetch a higher price for cars compared to cars without these parameters.
Hence the recommendation to car dealers is to capture and advertise cars with these features.

Project2.ipynb
Python notebook has the following items:
- Import vehicles.csv data file from Kaggle and filter out data that is not relevant for analysis
- Identify correlation matrix for features 'condition', title_status', 'transmission'
- Predict the price of the car with:
-    numeric features only - 'odometer' & 'year'
-    numeric and non-numeric features - 'odometer', 'year' & 'transmission'
-    with LASSO regression
- Using plots to identify patterns:
-    Scatter plot with 'year' & 'price', 'year' & 'odometer'
-    Box plot with 'condition' & 'price', 'title_status' & 'price', 'transmission' & 'price'
- The plots clearly articulate the findings from regression alaysis
