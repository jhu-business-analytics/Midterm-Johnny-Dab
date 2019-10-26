# Baltimore's Broken Brownstones: How vacant buildings affect school attendance
There are many environmental factors that affect whether a child will end up attending class or not. We looked at the role vacant buildings around schools could potentially play in decreasing the likelihood a student will not attend a school day. We found moderate evidence (r^2 = 0.2) that suggests an increase in vacant buildings around schools is related to a decrease in attendance. Therefore, we recommend that the Baltimore City Government focus it's efforts on tearing down or repurposing vacant buildings within 0.1 miles of schools.

## A City in Distress
Baltimore has a long history of facing significant educational challenges. Baltimore school's [rank among the lowest in the nation](https://www.baltimoresun.com/education/bs-md-nations-report-card-20180409-story.html) and our analysis shows that the problem is getting worse. A crucial indicator of school performance is the percentage of student's that regularly attend class. We found that across the board, attendance at all schools in Baltimore City has declined on average 3% between 2016 and 2018. In addition, Baltimore has faced a [dramatic increase in the number of vacant buildings around the city](https://publicservicescholars.umbc.edu/files/2018/09/Vacant-Housing-Final-2.pdf), with some neighborhoods doubling or tripling the number of vacancies between 2016 and 2018. Why does this matter? Because vacant buildings are often a ["breeding ground for drug abuse, crime and violence"](https://www.citylab.com/equity/2018/07/vacancy-americas-other-housing-crisis/565901/), with data showing that blocks with vacant properties can sometimes double the crime rate compared to blocks without vacancies. Therefore, the question we are trying to answer is does the presence of vacant buildings near school affect the attendance rates at schools in the City of Baltimore.
  
## Our Solution
  We found that there did appear to be a moderate association between increases in vacant housing and decreases in attendance, especially for schools that had the highest percentage increase in vacant buildings. We found that the trend was less clear for schools that either did not have a change in the number of vacancies, or had a small percentage change.
  
  We used year over year data from the [Baltimore Open Data set](https://data.baltimorecity.gov/), as well as the [Maryland School Accountability Reports](https://reportcard.msde.maryland.gov/). Due to changes in the Maryland standerdized testing system from PARCC to MCAP, it was prohibitively difficult to standardize school assessment scores over multiple years, as there were different standards in place at different schools. Therefore, we decided to focus on attendance rates as our dependent variable. Our independent observed variable was the number of vacant buildings around schools. To gather this data, we first had to find the coordinates of every school in Baltimore City. We used an excel macro linked with the Google Maps API to populate coordinates, and then used python scripts to pre-process the data. The vacant housing datasets already had coordinates for every building in the dataset. Using [geopy](https://geopy.readthedocs.io/en/stable/) we found the number of vacant buildings within 0.1 miles of each school. The distance 0.1 miles was decided based on experimental testing to prevent too much double counting of vacant buildings for schools in the inner city and also because 0.1 miles means the building is likely within visible range of a school.
  Once our data was processed, we calculated the percentage change in attendance between 2016 and 2018 as well as the percentage change in vacant buildings between 2016 and 2018. We also added binary columns representing whether attendance had gone down, and whether percentage of vacant buildings had increased. We immediately found that attendance across all Baltimore schools had decreased on average 3% and that the number of vacant buildings near schools had increased an average of 43% across all Baltimore schools. We ran regression using several methods to determine the potential impact of vacant buildings on school attendance. First, we used excel regression on all of the data points with the results below.
  
  
  
  To solve the business question we will used vacant building data that can be found at (https://data.baltimorecity.gov/) and we used excel to find the locations of every school in Baltimore. using that dat we were able to create a data set based in python and ecxel.We used a combination of linear regression in excel as well as SVM machine learning in Python to demonstrate that large drops in enrollment rates are associated with large increases in housing vacancies. Our process involved using geospatial coordinates of vacant houses as well as coordinates of schools to find the number of vacant buildings within a certain perimeter of each school in the City of Baltimore so we could then measure changes over time. 
  
### Suggestion section
  As of current, data proves that there is an inverse relation ship amongst students attendace rates and the vacany rates. Knowing this, we can bring this to the Department on Education so they will use this information for maybe future establishing of schools, finded better suited location, or getting the local governemtn to do something about the vacant buildings in the area.
 

### Additional Notes and Useful Links:

Baltimore City Government Open Data

Data Analysis
The Python scripts provided were used for pre-processing of all data

GitHub Issues and Projects
Utilize the GitHub Issues and Project feature to track your progress, collaborate with your team, and keep accounts of different resources and findings throughout your project. You can read more about submitting issues here, here, and here.

Executive Summaries
This write-up is similar to a business plan executive summary if your “service” is your business solution. While there are sentence/paragraph suggestions in each section, try to keep the written part of your executive summary to less than 2 pages typed in a Word document. Here are some good resources on business plans to learn more about why they’re important and how you should approach writing them:

Crafting a Powerful Executive Summary, HBS
Executive Summary Template, Forbes
