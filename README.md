# Los Angeles City Traffic Collisions
The objective of this project is to find the relationship between traffic collisions in Los Angeles City and the victims’ age, sex, and ethnicity, as well as the geographic location and time of these traffic collisions. Traffic has always been an issue for most people traveling around Los Angeles because it can take significant amount of time to get from place to place especially during rush hours. One of the reasons that causes major traffic delay is traffic collisions. Therefore, this specific dataset from Kaggle was used to understand if there are any associations between these traffic collisions and the age, sex and ethnicity of victims. Moreover, different neighborhoods in the Los Angeles City were looked into closely to understand which areas appear to be having the most traffic collisions.

## Datasets & Variables
The main dataset, Los Angeles Traffic Collision Data, used in this project was downloaded from Kaggle (https://www.kaggle.com/cityofLA/los-angeles-traffic-collision-data), which is originated from the Los Angeles Open Data. The raw dataset contains 467,481 records and 24 columns, with date range from January 2010 to April 2019. However, as I am only interested in events happened in the recent years, the dataset is filtered to include data from 2017 and onwards. Data fields not require for the analysis were also eliminated. After data cleaning and transformation process, the final data resulted in 107,844 records and 9 columns. A brief variable dictionary is shown in the below table:

| Variable      | Description   |
| :------------ |:------------- |
| Date Occurred | Date when the traffic collision occurred|
| Time Occurred | Time when the traffic collision occurred (In 24-hour military time)|
| Area ID | The LAPD 21 Community Geographic Areas |
| Area Name | The 21 Geographic Areas are also given names designation that reference landmarks or the surrounding communities |
| Area ID | The LAPD 21 Community Geographic Areas |
| Victim Age | Age of the victim (value range from 0-98) |
| Victim Sex | Sex of the victim (F – Female; M – Male) |
| Victim Descent Simple | Descent of the victim simplify into 5 categories |
| Longitude | Longitude of the traffic collision location |
| Latitude | Latitude of the traffic collision location |

Additional datasets containing the boundaries and police station locations of 21 geographic areas which the LAPD referred to as geographic divisions within the department were downloaded from Los Angeles Times website (http://boundaries.latimes.com/sets/) and were used in creating folium maps.

## Algorithm & Analysis
Descriptive statistics, histogram, barplot, boxplot, and pie chart were utilized to compare and visualize the relationship between traffic collisions and each variable. Folium map was used to illustrate the traffic collisions in each geographic area.

One-way ANOVA (Ordinary Least Squares model) was used to analyze whether the mean victim age between the two victim sex groups are different, with H0: The mean victim age between male and female are equal & Ha: The mean victim age between male and female are different. If p-value is less than 0.05, then reject H0 at 5% significance level and conclude that the mean of victim age between male and female are different, and vice versa.

#### Victim Age & Sex
Histogram shows the distribution of victim age while boxplot shows the distribution of victim age by victim sex. The median victim age for both sex groups are around 40 years old; however, the victim age of male seems to be slightly higher than female.
