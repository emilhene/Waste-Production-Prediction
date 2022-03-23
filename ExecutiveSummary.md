# World Data League 2022

## Executive Summary Template
This executive summary is one of the mandatory deliverables when you submit your solution. Its structure follows the WDL evaluation criteria and it has dedicated sections where you should add information. Make sure your executive summary covers all the sections since it will be an integral part of the Insights Report and your evaluation. Make sure your content is relevant and straight to the point.
**There is no need to reach the maximum number of words.**

Instructions:

1. 🧱 Create a separate copy of this template and do not change the predefined structure
2. 👥 Fill in the Authors section with the name of each team member
3. ✏️ Write your executive summary - make sure you write to a non-technical crowd. You can refer to images that are in the Submission Notebook.
4. 📄 Fill in all the text sections
5. 🗑️ Remove this section (‘Executive Summary Template’) and any instructions inside other sections
6. ⬆️ Upload the .md file to the submission platform.

## 🎯 Challenge
Predict Waste Production for its Reduction

## 👥 Authors
* Emil Henricsson Ene
* Marc Behse
* Alessandro Consiglio
* Navid Saffari

## ✨ Introduction (250 words max)
Rapid urbanization is a fact. Cities all across the globe are growing rapidly, and with them waste and pollutions increase as well. In 2016, cities generated a total 
of 2.01 billion tons of solid waste.
For this challenge we try to find trends in waste production for identifying patterns and insights that might help optimize waste processing and, ultimately, reduce 
waste production overall.
The project has been carried out using Austin, Texas, as the subject of study, but we hope the results may be applied to the general case as well.


## 🔢 Data (250 words max)
We have used three datasets:
1. Waste-data https://data.austintexas.gov/Utilities-and-City-Services/Waste-Collection-Diversion-Report-daily-/mbnu-4wq9
  Records waste-loads in pounds by date and time. Data is categorized by type of waste, where it is dropped off and the number of the route.
  This is quite nice data but unfortuanntley many missing values. More available data generally means better models and better predictions, so it could be improved in
  that way.

2. Population data https://www.austintexas.gov/sites/default/files/files/Planning/Demographics/population_history_pub.pdf
  Total poluation per year and annual growth rate. 
  Needs to be updated for recent years, we googled to find values for most recent years.
  
3. Austin weather data https://www.kaggle.com/grubenm/austin-weather 
  Daily weather data for Austin, cointains multiple measures. We used daily temperatures per month to find average monthly temperatures.
  Only contains values for 2013-12 to 27-07. Needs to be updated with more recent values to train models on longer time periods.

## 🧮 Methods and Techniques (250 words max)
Tell us what methods and algorithms you used and the results you obtained.
1. Exploratory/Descriptive analysis
  This is where we explored the data to understand what we were working with. In this stage we transformed the data, for example from the date and time into summarized 
  monthly observations. We also performed statistcal tests to find indicators of how 'well-behaved' data was. We also plotted the data over time to find patterns such 
  as 'Seasonality' and other underlying patterns that are difficult to see otherwise.

2. Algorithms for forecasts
  This is where we built the actual models. For the Vector Autoregressive(VAR) model, we built it to make predictions of future waste production based on information 
  from previous waste- and temperature data. The model did not make accurate predictions when given a test set, however it did make predictions that aligned with 
  the patterns of the actual data. For the ARIMA (Auto Regressive Integrated Moving Average) we built the model using an auto_arima function that automatically 
  calculated the best parameters for the ARIMA (p,d,q) (P,D,Q) model, in our specific case we decided to use a seasonality P=12. Also a Naive Seasonal method have
  been used to compare the quality of the two models since the serie seems affected by seasonality. Finally, we also used a Prophet model based on an additive model to
  make a out of sample predictions since the data showed yearly seasonality.
  

## 💡 Main Insights (300 words max)
Explain what you discovered from addressing this problem, such as interesting facts or statistics.
*Write here*

## 🛠️ Product
### Definition
A schedule to reorganize the collection of the garbage during differents peiods of the year

### Users
Describe who would be the users of your product and for what purpose would they use it.
Example: Traffic controllers use the dashboard during their work to better plan where to dispatch resources

### Activities
Describe what features your product has.
Example:
* Predicts the most likely locations for traffic accidents
* Suggests the fastest route from dispatch centres

### Output
Describe what the product outputs to the users and how it does that. You can add mockups and/or visualisations.
Example: Location of the accident on a map and suggest the fastest route from the dispatch centre.

## 🌍 Social Impact Measurement
### Outcome
If the outputs are your immediate results, describe your long-term results. What do you want your product to achieve? What ''good'' are you creating?
Example: To decrease response time from dispatchers so that people in urgent need receive help faster.

### Impact Metrics
From the outcome, define **2 to 4 metrics** that measure if you are achieving that outcome or not.
Example:
* Average Dispatch Time
* Average Distance from Accident Location and Dispatch Center

### Impact Measurement
Since you cannot wait to see the impact of your product, estimate it. You can do that by either using the estimations/predictions of your model, market research, products from proxy industries and/or similar locations, etc.

Example:
* *Based on model predictions*: Our model estimates a decrease of 6 minutes of the average dispatch time and a decrease of the average distance of 200 meters
* *Based on proxy products*: Similar studies in other cities show that the dispatch time can be decreased by as much as 13 minutes, depending on the traffic intensity of that city.
