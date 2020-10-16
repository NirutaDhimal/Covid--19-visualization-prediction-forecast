       
         Title: Covid-19 data visualization, prediction and forecasting


Description: 
    for this week's assignment we were given covid data and we had to use amazon sagemaker to visualize, predict and forecast. I had created a notebook instance called covid which is of type ml.t2.medium. I have directly  uploaded the covid19 data in csv format in the notebook instance and created a file called model and set kernel to conda_python3. I have used
matplotlib.pyplot and seaborn for data visualization, linearRegression and SVR for prediction and linear exponential smoothing i.e. holt model from time series analysis for forecasting.
First of all I have loaded our dataset to the variable df and removed rows contains location as 'International' or 'World'. I wanted to visualize world data in accordance to days so I created another dataframe called datewise which groups the data in df in accordance to the date and agregates columns total_cases, new_cases, new_cases_smoothed, new_deaths, new_deaths_smoothed,
new_tests, total_tests, new_tests_smoothed. I made barplot for new_cases, total_cases and total_deaths.
I wanted to visualize data according to week so I added another column in datewise called "WeekofYear" and made two line graphs. One shows weekly pprogress of total cases and total death cases and another shows weekly progess of new_cases, new_death_cases and new_tests .
Similarly I wanted visualized data accourding to location/county so I created another dataframe called countrywise which groups the data in df in accordance to the location and agregates columns total_cases, new_cases, new_cases_smoothed, new_deaths, new_deaths_smoothed,
new_tests, total_tests, new_tests_smoothed and sorts them in ascending order. I also another column in countrywise called "mortality_rate" which hold mortality rate for each country. I create two sub plots which shows barplot of top 15 countries as per total_cases and as per total_deaths.In addition to above I create another two sub plots which shows barplot of top 15 countries as per new_cases and as per new_deaths. I also created barplot of mortality rate in accordance to the county/location.
I also did data analysis for covid-19 for Nepal. I created barplots for total_cases, new_cases, total_deaths and new_deaths in Nepal according to date.
For prediction and forecasting I wanted to input no of days since covid-19 outbreak and output the total cases in world at that particular day. For that I added another column in datewise called "Days Since" which contains no of days since covid19 outbreak.
For prediction I seperated 95% of data for traing and 5% for validation and used linear regression and svm.
For forecating I seperated 85% of data for training and 15% for testing and used holt model.
I predicted / forcasted for 18 days after oct 12, 2020.
The result of prediction for top 5 rows is below:
	Dates	LR	SVR	Holts linear model predictions
0	2020-10-13	25970103	18156971	88847671
1	2020-10-14	26085091	18405054	89110309
2	2020-10-15	26200079	18656607	89372947
3	2020-10-16	26315068	18911666	89635585
4	2020-10-17	26430056	19170267	89898223 
 

