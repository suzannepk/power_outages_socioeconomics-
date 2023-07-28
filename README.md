# Power Outages and Socioeconomics
ECP Bootcamp 

### Welcome!!

This README will guide you through the stages of this project, and by the end we will have explored and identified correlations both using visual plots and statistical tests. It is full of tips that will help you. 

### Teeing up the Problem

In June of 2016, a heatwave swept across the SW United States, causing severe loads on the power grid, and leading to large number of power outages across several counties. We are going to be exploring correlations between temperature and power outages, energy burden and poverty.

Energy justice in the United States means making sure that people have access to energy and are also not being charged disproportionately to their income for the basic energy services that are standardly provided. An energy burden is the fraction of a person’s income that goes toward paying for their electrical power.

The ability to effectively respond to and facilitate the restoration of energy systems during disasters relies on the ability of local and federal agencies and first responders to have timely, accurate, and actionable information about the status and potential impacts of energy sector disruptions. The US Department of Energy (DOE) provides information about these disruptions via its Environment for Analysis of Geo-Located Energy Information (EAGLE-I) system run by Oak Ridge National Laboratory. EAGLE-I provides capabilities for monitoring energy infrastructure assets, reporting energy outages, and displaying potential threats to energy infrastructure, and coordinating emergency response and recovery.

We want you to help us start to build tools and processes that will help us understand if underserved populations and people dealing with larger levels of poverty get the same access and service for energy for the same energy burden as more severed and wealthy populations. We have data sets with a resolution at the county level. One gives the average fraction of the population that lives below 100% and 200% of the federal poverty level in each county as well as, energy burden and demographic data. There is another set that shows how may customer were without power in 15-minute intervals from 2015-2021. We have a other set that tracks the June 2016 heat wave temperatures that we will be using to explore what happens to energy justice when the power grid is under stress. Use this data to help us begin to monitor and better understand energy justice in the United States!   

### EAGLE-I Background

EAGLE-I is the US Department of Energy’s data and information platform for real-time wide-area situational awareness of the energy sector, sponsored by the DOE Office of Cybersecurity, Energy Security, and Emergency Response. It is developed and run from Oak Ridge National Laboratory in Tennessee. 

The EAGLE-I system allows local, state, and federal government agencies, and private sector electricity and fuel providers to have access to timely, accurate, and actionable information about the status and potential impacts of energy sector disruptions and provides a modernized framework for the next set of capabilities in emergency response support.

Developed by the Office of Electricity Delivery and Energy Reliability’s (OE) Infrastructure Security and Energy Restoration (ISER) division, EAGLE-I uses data science approaches to provide a centralized platform for monitoring power distribution outages for over 133 million customers, with just over 90% coverage of the US and Territories. Oak Ridge National Laboratory provides EAGLE-I as a service to other Federal, State, and local agencies and departments and first responders aligning with DOE’s Emergency Support Function-12 (ESF-12) mission, and users come from DOE, DHS, NGA, DOD, FEMA, USDA, and state emergency responders, among others.


### Goals:

* Discuss access to electrical power and the cost burden for that access and how those issues relate to poverty.
* Understand how to use statistical tests to justify correlations.
* Understand how to create and use visualizations to show connections and correlations in big data.
* Utilize Python and Excel to explore large data frames.
* Discuss how doing tasks in parallel is more efficient than doing them in series.
* Explain the assumptions you made in your analysis. For example, if you use “total customers” for a given region to represent relative total populations between counties, acknowledge that while the members of one household are all counted as one customer and businesses are a customer too, "total customers" is still a measure of relative size of the populations of customers living in each county.


### The Big Questions for this Project:

1. Which counties were hit with the highest temperatures in 2016? Can you show it visually? (Datasets: CtyAvTemp62016.csv)

2. Can you show the average number of customers without power per county during the heatwave? Can you visualize it for the whole US? (Data sets: eaglei_outages_2016.csv, CtyAvTemp62016.csv )

3. Do counties with many people living below the poverty line have more power outages on average than wealthier counties? (Data sets: CtyAvDemog2010, aglei_outages_2016.csv) Can you use statistical tests to justify your answer? Is what you found true generally for all counties in the study? Is it still true for the counties hardest hit by the heatwave during the heatwave? Are there any other factors expressed in the data that correlate with large numbers of outages per county?

4. Do citizen living below the poverty level bear a greater share of the energy burden in most counties? Can you use statistical tests to justify your answer? What does this look like for the counties that you identified as impacted most by the heatwave? (Datasets: CtyAvDemog2010 data, eaglei_outages_2016.csv)

You are doing super well if you get through question 4! 5 and 6 are stretch goals.  

5.  Can you tell if the number of customers without power is correlated with the highest temperatures? (Datasets: eaglei_outages_2016.csv and ones you find!)

6. Done with time to spare? How is the region you are from doing with energy justice? How does it compare to other regions of the US? Defend how you define "Region". 
  And/Or

  Look for data on the internet about another natural disaster that happened between 2015 and 2021 and see if you can repeat the analysis for it.

**Note** You do not have to tackle the Big Questions with the exercises given in this guide if you have another plan in mind to work with. These are here to help you get started and are not mandatory.


### The Final Product:

You will combine your visualizations and insights from answering the big questions into a presentation that you will give on the last day of the workshop.

## Important Notes on the Big Questions:

* Not all team members need to work on all exercises and questions. It would be best to split up the work. It is fine if you cannot answer all the big questions or all their parts.

* You will need to answer basics of the first four questions to completely meet the first goal of this project.

* You will need to answer questions 1 and 2 to answer questions 3.

* Question 4 can be mostly answered by using just the CtyAvDemog2010.csv data.

* Question 5 will require you to find more data than we have provided and do a lot of interpolation. I suggest you start by googling “Hourly temperature for LA for June 20, 2016”. Remember that your eagle-I data's time is given in UTC.


#### Some reading resources:

Research Project Resources:
* Explanation of 2010 census data categories: https://screeningtool.geoplatform.gov/en/methodology
* Map of burdened communities: https://screeningtool.geoplatform.gov/en
* Articles about the 2016 heatwave:
* https://web.archive.org/web/20160622004100/
* https://weather.com/forecast/regional/news/dangerous-record-heat-southwest-plains
* https://www.huffpost.com/entry/record-heat-wildfires-west-us_n_57678bb4e4b015db1bc9be59?section=
* Nice visualization of past temperature information: https://www.timeanddate.com/weather/usa/los-angeles/historic?month=6&year=2016016/historic?month=6&year=20166&year=2016
* Medicare at risk population map: https://empowerprogram.hhs.gov/empowermap
* FIPS Codes - https://en.wikipedia.org/wiki/List_of_United_States_FIPS_codes_by_county

Python: 
* Useful Jupyter examples for this project: https://github.com/secondspass/jupyter_bootcampproject_examples/
* Pandas tutorial: https://www.activestate.com/resources/quick-reads/what-is-pandas-in-python-everything-you-need-to-know/
* Exploratory Data Analysis: https://medium.com/@gauravtopre9/questions-to-ask-while-eda-1a19f82fbc5d

General:
* Glossary of common research computing terms: https://researchcomputing.princeton.edu/learn/glossary
* Resources for Research Computing: https://researchcomputing.princeton.edu/learn/tutorials/external-resources-learning
* HPC Crash Course: https://www.olcf.ornl.gov/summer-hands-on-hpc-crash-course/


### Datasets

First things first, let's look at our data. We're going to be looking at our data using Excel (or Google Sheets) just so you're familiar with what the data should look like. All the data we need is in this google drive folder: https://drive.google.com/drive/folders/1fAaBPgWWaA_9VB2iYUAWeW8biTXJQFwZ?usp=sharing

We are going to be working with these datasets:

* eaglei_outages/eaglei_outages_2016.csv - provides the breakdown of the number of customers that were out of power in the year 2016, for each county in the US, with data for each 15 minute increment covering the entire year.

* temperaturedata/CtyAvTemp62016.csv - in the temperaturedata folder, each .csv file is the average temperature of the day for each county in the US and its territories. The numbers in the file name represent the date. For example CtyAvTemp61716.csv is the data for June 17 2016.

* CtyAvDemog2010.csv - 2010 census data with socioeconomic measures, including energy burden, health, and age demographics, averaged by county. You may need to use Google to understand what each of the headers in this data set mean.

If you want to look at the relative fraction of customers impacted per county, you need a measure of how many customers are in each county. We don't have data on the exact number of customers per county in 2016, but we do have the estimate for 2023. We also have included estimate of the total population for each county. You can chose either of these to estimate the fraction of customers per county impacted by power outages, but you will need to explain your choice.

* county_customers_2023.csv - estimated number of eagle-i customers by county as of 2023
  
* county_population_by_year.csv - population of US county by year, from 2010 to 2019. If you want to use population to fraction of population that was impacted, refer to this dataset that contains information from the 2010-2019 census.

* NOTE: Something you'll find as you work with these datasets is that there might be some data missing here and there e.g. There might not be power outage information for some county for some given day. That's just the nature of data science sometimes, that the data you have isn't perfect. So you have to make sure that you're using the data you have and making sure you're accounting for any missing data when before you make any conclusions. You may need to use Excel or your favorite method to "Clean" some of the data sets. Cleaning is the process of removing problematic data, such as ASCII letters or punctuation characters that appear where numbers should be, or reformatting one set of data, so it can be compared to another set.

### Jupyter Notebooks

The exercises and tutorials linked below are in Jupyter notebooks and will familiarize you with the provided data and prepare you to answer the the big questions.

1. [Exploring Data](1_Exploring_Datasets.ipynb)
      * Analyzing data using Google Sheets
  
2. [Python Intro](2_Python_Pandas_Intro.ipynb) 
      * Reading Excel Files, Filtering Data (Movie Dataset)
      * Plotting Data using Pandas & Matplotlib (Movie Dataset)
      * Practice with Real Data (Temperature Data)
      * Merging dataframes

3. [Time-Series Data](3_Time_Series_Data.ipynb) 
      * Representing time-series data with line-charts
      * Up-sampling data with numpy
      * Calculating average and median number of power outages
      * Merging aggregated data with regular dataframe
    
4. [Visualizations using Maps](4_Map_Visualizations.ipynb)
      * Pandas map plot
      * Geopandas interactive map
5. [Correlation Analysis](5_CorrelationAnalysis.ipynb)
      * Correlation vs Causation
      * Pearson Correlation
      * Spearman Correlation
      * P-value
      * Histogram
      * Scatterplot
      * Correlation Test
      * Interpreting Spearman Rank Score & p-value
      * Interpreting statistically significant p-value
      * Correlation Matrix
6. [MPI Intro](eaglei_mpi_scripts/6_MPI_exercises.ipynb)
      * Introduction to Message Passing Interface (MPI)
      * Load and pre-process the power outage data
      * Divide the data into chunks to distribute among MPI processes
      * Implement parallel processing using MPI
      * Analyze and interpret the results         

8. [Big Questions Working Notebook](6_Big_Questions.ipynb)
  * Working space for the addressing the Big Questions & Project Goals 

## Acknowledgements:  
Data and scientific inspiration and guidance for this project was developed by ORNL Scientists Melissa Dumas and Sarah Tennille.


