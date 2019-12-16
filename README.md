# NYC-Graffiti-Analysis
Group project completed in data science class to analyze the data from NYC Graffiti

## Thesis
In the City of New York, the average number of days to resolve incidents of graffiti differs between boroughs with statistical significance.
## Background / Summary
The data to justify the above argument is provided by the New York City Deparmtent of Sanitation which handles instances of graffiti in the city’s five boroughs: Manhattan, Brooklyn, The Bronx, Queens, and Staten Island. The data set has 21304 observations, each representing an instance of graffiti.
Within the datat set, there are a multitude of variables, but we focus on the follwing: the borough, the date the case was opened, the date the case was closed (if the case is closed) and latitude and longitude.
As previously mentioned, not all the cases are closed. Of the 21304 observations 7669, or about 36% do not have a closed date– some of these incidents were filed over a year ago and have not since been closed. While not a part of our primary argument, we analyze open cases between the boroughs as well.
## Primary Results
Of the five boroughs, the borough with the smallest mean (fastest average case resolution time) was The Bronx, followed by Brooklyn, Manhattan, Queens, and lastly Staten Island.
In addition to comparing the boroughs with a boxplot, a faceted density plot of the number of days to close a case shows the following graph. We can see most cases are resolved around 100 days with spikes at or around the 30-day mark.

#### Open Cases
To address open cases, we classified an open case as either issue or nonissue depending on the number of days the case was currently open. If the case was ‘older’ than the length of time it takes to resolve 95% of closed cases, that case was flagged as an issue case. The following graph shows the proportion of open cases that are issue cases by borough. The size of the dot represents the size of the mean number of days to close a case of closed cases.

## Description of Evidence
To determine if there is a difference between the average length of time to close a graffiti case between all boroughs, we conducted an ANOVA test. Our alternate hypothesis was that there was a difference between the average length of time to close a graffiti case between boroughs. Our null hypothesis was that the means were same between boroughs. The resulting p-value is 1.214099e-45. Since this p-value is ~0.0 we can prove with a high degree of statistical certainty that the alternate hypothesis is true, and the means are different between boroughs.
Utilizing t-tests we can see that the the p-value when comparing the mean length of Manhattan with Brooklyn is 0.003880954, or 0.388% which assuming an alpha of 0.05 is well within the limits for being statistically signifigant. With respect to The Bronx and Queens, we see a p-value of 5.631018e-21 which is 0.0000000000000000005631018% or effectively 0.0% which also is statistically signifigant.
