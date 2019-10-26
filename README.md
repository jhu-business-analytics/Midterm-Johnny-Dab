# Baltimore's Broken Brownstones: How vacant buildings affect school attendance
There are many environmental factors that affect whether a child will end up attending class or not. We looked at the role vacant buildings around schools could potentially play in decreasing the likelihood a student will not attend a school day. We found moderate evidence (r^2 = 0.2) that suggests an increase in vacant buildings around schools is related to a decrease in attendance. Therefore, we recommend that the Baltimore City Government focus it's efforts on tearing down or repurposing vacant buildings within 0.1 miles of schools.

## A City in Distress
Baltimore has a long history of facing significant educational challenges. Baltimore school's [rank among the lowest in the nation](https://www.baltimoresun.com/education/bs-md-nations-report-card-20180409-story.html) and our analysis shows that the problem is getting worse. A crucial indicator of school performance is the percentage of student's that regularly attend class. We found that across the board, attendance at all schools in Baltimore City has declined on average 3% between 2016 and 2018. In addition, Baltimore has faced a [dramatic increase in the number of vacant buildings around the city](https://publicservicescholars.umbc.edu/files/2018/09/Vacant-Housing-Final-2.pdf), with some neighborhoods doubling or tripling the number of vacancies between 2016 and 2018. Why does this matter? Because vacant buildings are often a ["breeding ground for drug abuse, crime and violence"](https://www.citylab.com/equity/2018/07/vacancy-americas-other-housing-crisis/565901/), with data showing that blocks with vacant properties can sometimes double the crime rate compared to blocks without vacancies. Therefore, the question we are trying to answer is does the presence of vacant buildings near school affect the attendance rates at schools in the City of Baltimore.
  
## Our Solution
  We found that there did appear to be a moderate association between increases in vacant housing and decreases in attendance, especially for schools that had the highest percentage increase in vacant buildings. We found that the trend was less clear for schools that either did not have a change in the number of vacancies, or had a small percentage change.
  
  We used year over year data from the [Baltimore Open Data set](https://data.baltimorecity.gov/), as well as the [Maryland School Accountability Reports](https://reportcard.msde.maryland.gov/). Due to changes in the Maryland standerdized testing system from PARCC to MCAP, it was prohibitively difficult to standardize school assessment scores over multiple years, as there were different standards in place at different schools. Therefore, we decided to focus on attendance rates as our dependent variable. Our independent observed variable was the number of vacant buildings around schools. To gather this data, we first had to find the coordinates of every school in Baltimore City. We used an excel macro linked with the Google Maps API to populate coordinates, and then used python scripts to pre-process the data. The vacant housing datasets already had coordinates for every building in the dataset. Using [geopy](https://geopy.readthedocs.io/en/stable/) we found the number of vacant buildings within 0.1 miles of each school. The distance 0.1 miles was decided based on experimental testing to prevent too much double counting of vacant buildings for schools in the inner city and also because 0.1 miles means the building is likely within visible range of a school.
  Once our data was processed, we calculated the percentage change in attendance between 2016 and 2018 as well as the percentage change in vacant buildings between 2016 and 2018. We also added binary columns representing whether attendance had gone down, and whether percentage of vacant buildings had increased. We immediately found that attendance across all Baltimore schools had decreased on average 3% and that the number of vacant buildings near schools had increased an average of 43% across all Baltimore schools. We ran regression using several methods to determine the potential impact of vacant buildings on school attendance. First, we used excel regression on all of the data points with the results below.
  
  
 However we quickly realized that the trend didn't hold well for schools where vacant housing didnt change or was 0 to begin with, and schools that didn't have significant attendance changes. We filtered the data and looked at only the schools with the highest increases in vacant housing and found a much clearer trend with an r^2 of 0.4.
 
 
 
 Finally, we obtained a correlation of 0.7 between vacant housing increases and attendance decreases.
 
  
  
  
## Suggestion section
  Based on our analysis, we recommend that the Baltimore City Government target vacant buildings near schools in order to combat the potentially harmful effects that they have on attendance. Further study into the specific psychological or crime effects of vacant buildings near schools could bolster our understanding of how to better turnaround failing schools. one viable option for cities is to [turn vacant buildings into greenspace](https://urbanland.uli.org/economy-markets-trends/from-vacant-properties-to-green-space/).

## Additional Notes and Useful Links:

Data Analysis
The Python scripts provided were used for pre-processing of all data as well as the geomapping.
Excel was used for regression and additional pre-processing

Presentation Slides
https://docs.google.com/presentation/d/e/2PACX-1vTbGSYouew1V3A_kAHXAT_qblix5dKx5sd6qeZtXGUHf1Kk69C8Ill5sSq1kr2Immc-2zOi0yEhoZz4/pub?start=false&loop=false&delayms=3000
