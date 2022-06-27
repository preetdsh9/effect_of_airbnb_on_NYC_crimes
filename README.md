#### Motivation

**The idea behind this project is to explore and understand if the existence and rise of Airbnb has any correlation with the crime rates in New York City.** <br>


We came across articles about the increase in crimes in NYC in Q1 of 2022 which led to the article “Why do some crimes increase when Airbnbs come to town?” 

We found this particularly interesting because we saw the potential of using data to see if a short-term vacation rental company has anything to do with the crime rates in a major city such as NYC and hence, that became our hypothesis for this project.

#### Significance and Value Proposition
Airbnb has grown significantly over the last decade and has captured a significant share of the lodging market. With this market power comes a big responsibility and an increase in crimes falls under this responsibility.

If crimes are indeed increasing in NYC because of Airbnb, the government and Airbnb can be made aware of it so they can take the necessary steps to ensure the safety of tourists.

An example of a step that can be taken by Airbnb could be adding a “safety verified” feature for listings which also provides detailed information on how the verification process works.

#### Related work
The starting point for us was to explore data that will help us find some meaningful trends that could help the general public and learning about the recent increase in NYC crimes motivated us to explore issues in this realm. <br>
Link: https://www.amny.com/police-fire/new-york-city-crime-rates-january-2022/

Further research led us to the article below by the Wired:
##### "Why Do Some Crimes Increase When Airbnbs Come to Town?
Link: https://www.wired.com/story/why-some-crimes-increase-when-airbnbs-come-town/

Our hypothesis was set using the following takeaway from the report: <br>
##### Tourists neither commit nor attract crimes. But a study finds that violent offenses rose in neighborhoods where more homes were converted to short-term rentals."

According to the article, certain violent crimes — fights, robberies, reports of someone wielding a knife — tended to increase.

#### Data

The data comes from two different sources:

The NYC crime data describes all valid felony, misdemeanor, and violation crimes reported to the New York City Police Department (NYPD) from 2006 to the end of last year (2019). Each instance has a record of the date, time, location, crime details, suspect details and any other relevant information that the NYPD uses. This data is spread in one table of 35 columns and 7375993 rows. <br>
Data link: https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i/data <br><br>

**Data Cleaning**: The data itself is in a clean format. We need to drop some of the columns, change column names, remove whitespaces from certain columns, adjust the data types, and add a few columns like report_year and report_month.

The Airbnb listing data describes all the information about a particular listing including date of listing, location, amenities, neighborhood, transit, rental size, listing score, and much more from 2008 to 2019. This information comes from the following article: https://medium.com/@lilyng15/data-analysis-on-airbnb-new-york-city-60bb85560a01 and that redirected us to the following git repository: https://github.com/ioslilyng/airbnb_nyc/tree/master/data
This data is spread in one table of 81 columns and 49531 rows. <br>
Data link: https://github.com/ioslilyng/airbnb_nyc/tree/master/data<br><br>


**Data Cleaning**: The data itself is in a clean format. We need to drop some of the columns, change column names, remove whitespaces or $ symbols from certain columns and adjust the data types
<br>
As far as the datasets being used are concerned, yes, they have been used to analyze and gain insights into NYC gun crimes and to analyze and gain insights into NYC Airbnb listings separately (Links below). Our problem domain is quite different from the ones above.
<br>
NYC Shooting EDA:
https://www.linkedin.com/pulse/new-york-shooting-2006-2019-exploratory-data-analysis-magdy/ 
<br>
NYC Airbnb listings: https://medium.com/@lilyng15/data-analysis-on-airbnb-new-york-city-60bb85560a01

#### Questions

1) Have crimes increased in Airbnb hotspots?
  * What are the top 3 hotspots in each neighbourhood by count?
  * What is the growth of rate of these hotspots?
  * Have the overall crimes in NYC increased or decreased between 2006-2019? 
  * Is there a trend between the growth of Airbnb hotspots and the crimes in the respective neighbourhoods?
  * Are offense against public order (fights), dangerous weapons (knife), and robberies the most common Airbnb related crimes? If not, what are the most common crimes?
  * Have the above crimes increased or decreased over the years near the hotspots (1 km radius)?

2) How are the top 3 crimes in terms of count spread across the months of the year? Are they high during the busiest month for Airbnb hosts?

3) If the Airbnb listing description includes the word safe, what is the average rating in comparison to when it is not mentioned? 
  * Is the difference statistically significant?

#### Plan and Workflow:

*   We looked at the timeline from 2006 - 2019 for the crime data and from 2008 - 2019 for the Airbnb listing data.

*   We started the project with data cleaning on the Airbnb and Crimes datasets
    
*   Intermediate presentation:
    *   We identified Airbnb hotspots 
    *   We filtered the Airbnb clusters for top 3 neighborhoods 
    *   We identified the crimes in a one km radius within each neighborhood

*   Final presentation:
    *   We analysed the growth of Airbnbs in NYC over the years
    *   We analyzed the crimes heatmap over the year
    *   We analyzed the crimes heatmap by month
    *   We analyzed crimes v/s airbnb growth (by total count)
    *   We ran statical tests for the lower rated Airbnbs that have the word 'safe' under description
    *   We did a word cloud analysis for the Airbnb description
    *   We filtered the crimes by the crimes we identified in the Wired article and did an anlysis on those crimes within the airbnb hotspots


    #### Possible findings and implications
**Possible findings**

1) Have crimes increased in Airbnb hotspots?
- We anticipate the crimes to be higher in regions where there are clusters of Airbnb listings. The reason behind this is that maybe criminals target tourists more and if tourism is increasing, crimes would too.

2) What is the growth of rate of these hotspots?
- The growth rate of Airbnbs would reduce but still increase in count.

3) Have the overall crimes in NYC increased or decreased between 2006-2019? Have the above crimes increased or decreased over the years near the hotspots (1 km radius)?
- Yes, from research it seems like crimes have been increasing in NYC on a yearly basis.

4) Is there a trend between the growth of Airbnb hotspots and the crimes in the respective neighbourhoods?
- Yes, we anticipate a positive correlation between the two.

5) Are offense against public order (fights), dangerous weapons (knife), and robberies the most common Airbnb related crimes? 
- We do not expect them to be the top crimes. 

6) What are the most common crimes?
- Top crimes could be petit larceny or traffic violations.

2) How are the top 3 crimes in terms of count spread across the months of the year? Are they high during the busiest month for Airbnb hosts?
- We expect these numbers to be highest during the busiest month for Airbnb hosts.

3) If the Airbnb listing description includes the word safe, what is the average rating in comparison to when it is not mentioned?
Is the difference statistically significant?
- We expect this number to be statistically significant because Airbnb hosts would receive bad ratings if they mention the word safe when the listings is not in a safe neighbourhood.

**Possible Implications**

If crimes have indeed increased with Airbnb growth, especially near the Airbnb hotspots, the government and Airbnb need to be made aware of this to ensure actions are taken against this. 

NYC is a major tourist city with tourists visiting from across the globe. High crimes do scare such tourists and in order to maintain the shine of the city and also, keep the brand recognition of Airbnb intact, this information would be useful.

In addition to this, the government can add additional regulations on Airbnb so that they start taking steps towards the safety of the tourists.
