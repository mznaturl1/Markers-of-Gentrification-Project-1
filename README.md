# Measures of Gentrification Across Counties: Kent, Oakland, and Saginaw (Michigan)

## Description

Analysis of key variables to predict communities at risk of gentrification by focusing on measures that show the migration of upper and middle income residents into traditionally low income areas. The chosen variables were the most likely to show indications of gentrification across selected counties: population size, poverty rates, unemployment rates, income, home values, and rent prices. Further analysis of the data attempting to find statistical significance across the chosen variables through the use of graphs and linear regression.

### Background
Gentrification is a process by which poorer communities are changed due to an influx of wealthier households. This process can be extremely detrimental to the community, as often the poorer inhabitants are forced out of the area due to rising costs of living. For the purpose of this project, businesses were not considered due to dataset limitations (to be discussed later). Determining what areas are in the early stages of gentrification can help social service agencies focus efforts to maintain housing stability for low income households. This can also assist lawmakers to investigate policies to protect those already living in the area.

This project seeks to utilize previous research and input Census data to analyze changes in real communities that may be at risk. Previous quantitative studies have focused on income as a primary variable; however, this project seeks to explore the potential significance of demographic data, home value, and rent prices as well. Though the scope of this project was localized in Michigan, the primary data analysis framework can be used to explore other regions by simply importing other county's zipcodes while performing initial data exploration.

### Technologies Used

Python, Jupyter Notebook, CPI, Pandas, Matplotlib, Scipy, Numpy, Census, Seaborn, Git, GitHub

## Description of Data Exploration

The data was compiled using the Census API's Python wrapper. This data was pulled into a dataframe, then all financial variables were converted to 2023 rates using an inflation module (CPI).

Additional columns were created for the percentage of the population unemployed, percentage in poverty, and some additional separations based on race. 

The years 2011 - 2020 were chosen as a full and complete decade. These could easily be changed by shifting the API to call the desired years, as well as changing some of the iterators that ran per-year.

Using the Shapiro-Wilk test, all variables per county were checked for normality. In all cases, the p-value was greater than .05, indicating that none of the variables were normally distributed. As a result, the standard measures of statistical significance could not be utilized, since they assume normality. 

Oakland County has 66 zipcodes, while Saginaw has 25 and Kent has 31. Oakland County has the highest Adjusted Median Income at almost $92,000, while Saginaw and Kent are between $60-70,000. Saginaw County has the least population per zip code--with a median of 6162--compared to around 20,000 for both Kent and Oakland Counties.

## Data Analysis

###### Adjusted Median Income

Towards 2020, Kent County sees an increase in income around the outskirts of the county, without much change near the center. 

![Kent_Income](https://user-images.githubusercontent.com/116215793/218327133-9aa3cf37-7ecf-4b12-b214-a1a2bec7cc70.gif)


Oakland County shows a significant increase in income across most of the county, minus two pockets of poverty: one in the center of the county and one in the southern-central region.

![Oakland_Income](https://user-images.githubusercontent.com/116215793/218326035-350ca797-00ca-4eab-a693-733916ba23f8.gif)


As a whole, Saginaw is a much poorer community than Oakland or Kent. Saginaw does see a few pockets of increased income over time, but with much less overall growth than the other two counties. 

![Saginaw_Income](https://user-images.githubusercontent.com/116215793/218326041-1b5436b6-bffe-45cd-96a6-0caed5b38287.gif)


###### Adjusted Median Home Values

![box_median home_value_counties](https://user-images.githubusercontent.com/117309455/218923987-e4735729-83ed-4bf2-aedc-3a9bca8a5ddb.png)

**Kent County** 
Kent County. As of the 2020 Census, the county had a population of 657,974, making it the fourth most populous county in the State of Michigan. Its county seat is Grand Rapids in West Michigan.  The county was established in 1831 and organized in 1836.  In analyzing the data for the county, here are some interesting finds:
•	Kent County endured declines in home values for each year between 2011- 2018.
•	Kent County shows a boom in home prices right before 2020, centered in the middle of the county
•	Adjusted Median Home Value and % White Poverty form a cluster with four outliers
•	Adjusted Median Home Value and Adjusted Median Income are highly correlated


![Kent_Home](https://user-images.githubusercontent.com/116215793/218327142-5c4ea4ed-2aa2-4f75-b68f-9fdff67c90c5.gif)
![kent_linregress_adj_median_home_value](https://user-images.githubusercontent.com/117309455/218925038-c7554281-aa32-42c8-8afe-c3f27f8e368a.png)


**Oakland County**
Oakland County is part of the Detroit metropolitan area, with the county seat in Pontiac. The county has a population of 1,274,395 at the 2020 Census, making it her second most populous county in the state. Founded in 1819, the county was organized in 1820.  In analyzing the data for the county, here are some interesting finds:
•	Almost the entire county of Oakland sees a major boom in home prices. 
•	The only area with virtually no change is at the center of the county. 
•	There is a small pocket of slower growth as well, in the central Southern region. 
•	Poverty count is highly determined by Adjusted Median Home Value
•	Poverty Count – Black and Adjusted Median Home Value form a cluster with one outlier


![Oakland_Home](https://user-images.githubusercontent.com/116215793/218326104-1f66a070-9e3d-49d2-af9a-3c0b6951d3f6.gif)
![oakland_linregress_adj_median_home_value](https://user-images.githubusercontent.com/117309455/218924603-dc9f335c-194a-4201-b6ea-5715020d628b.png)


**Saginaw County**
Saginaw County. Officially known as the County of Saginaw is Michigan's fifth largest metropolitan area and has the City of Saginaw (both known as Mid-Michigan) as its county seat. The county was formed on September 10, 1822, and fully incorporated on February 9, 1835. According to the 2020 Census, the county had a total population of 190,124.  In analyzing the data for the county, here are some interesting finds:
• House prices fell between 2011 and 2018
• House prices started to rise slightly by 2020
• Adjusted Median Home Value and poverty figures – Whites are split into three groups, with one outlier.
• Adjusted Median Home Value and Adjusted Income are highly correlated


![Saginaw_Home](https://user-images.githubusercontent.com/116215793/218326112-b1fd442c-abec-4abc-b1e6-6d6f79b449d7.gif)
![saginaw_linregress_adj_home_value](https://user-images.githubusercontent.com/117309455/218925238-4da84670-b57f-4774-8036-10bdebec877e.png)


###### Adjusted Median Rent Prices

Rent prices grow slightly over the decade, but with no major patterns.

![Kent_Rent](https://user-images.githubusercontent.com/116215793/218326128-688305ab-6c45-4ece-b897-b035a962aa18.gif)


Rent prices increase mostly in the Southern and Western regions of the county.

![Oakland_Rent](https://user-images.githubusercontent.com/116215793/218326138-4e9c53e1-4832-4b71-ac66-57c090a304bf.gif)


Rent prices do not change significantly throughout the decade.

![Saginaw_Rent](https://user-images.githubusercontent.com/116215793/218326145-feaff192-1b4f-45c5-9c49-00c80bbf8e31.gif)


###### Total Population

The county only sees slight growth over the decade, centered towards the middle of the county.

![Kent_Population](https://user-images.githubusercontent.com/116215793/218326157-8ce13ccd-353d-4b70-baba-313eb6e9d46e.gif)


The county sees a slight increase in population over the decade.

![Oakland_Population](https://user-images.githubusercontent.com/116215793/218326164-0ad0dc4e-a5fc-4f91-8015-540f8f67c981.gif)


Saginaw County sees a decrease in population over the decade, mostly around the center of the county.

![Saginaw_Population](https://user-images.githubusercontent.com/116215793/218326177-f09c05b5-e119-479d-acef-2a1685d6bc3f.gif)


###### Percent of Population Unemployed

Unemployment rates decrease significantly across the county throughout the decade.

![Kent_UE](https://user-images.githubusercontent.com/116215793/218327158-b23161fe-a7f3-4d22-a9db-01f8a75bf25e.gif)


As a whole, the county saw a reduction in unemployment. This reduction was less pronounced in the center of the county.

![Oakland_UE](https://user-images.githubusercontent.com/116215793/218326217-9470ea90-5025-4f5a-b097-dc34241ad8d1.gif)


The entire county showed a reduction in unemployment over the decade, with a major reduction in the center of the county.

![Saginaw_UE](https://user-images.githubusercontent.com/116215793/218326223-9a04020d-e367-4fb7-9406-6fcc40776acc.gif)


###### Percent of Population in Poverty

Poverty rates shift around the county for the first half of the decade, then drop significantly in the second half of the decade. The largest pocket of poverty remains in the center of the county. The graph showing zipcodes supports a pocket of poverty. 

![Kent_Poverty](https://user-images.githubusercontent.com/116215793/218326232-9a29aec2-b8bc-4763-a71c-381a02d28e91.gif)
![image](https://user-images.githubusercontent.com/116215793/219220667-8b139276-9e40-4319-bf7c-48401121c816.png)


Poverty rates actually grow in the center of the county for the first half of the decade, then see a slight reduction in the second half. The Southeast corner of the county sees this trend as well, but with a major reduction overall. Most zip codes do not have a large rate of poverty, although there are specific pockets within the county that more poverty.

![Oakland_Poverty](https://user-images.githubusercontent.com/116215793/218326235-00d70fd5-34c8-4837-b051-89e7332031be.gif)
![image](https://user-images.githubusercontent.com/116215793/219220429-2c162185-eb62-43a5-b125-16df7ccf3ebd.png)


There is no major overall change in poverty rates across the decade. There are, however, three major pockets of poverty within the county.

![Saginaw_Poverty](https://user-images.githubusercontent.com/116215793/218326239-dc1371a1-be88-4a80-9bb2-73d001b677f4.gif)
![image](https://user-images.githubusercontent.com/116215793/219220847-419715f0-9488-469e-9595-24057f8efc93.png)



## Limitations of the Dataset and Future Considerations

The Census data utilized is expansive and informative with time constraints of the project being its primary limitation, with more time it would be possible to delve deeper into the dataset and tease out potential relationships of significance. It also, however, had a variety of limitations which need to be considered when evaluating the results. First, the census uses Zip Code Tabulation Areas (ZCTAs), which differ slightly from postal zip codes. This creates an issue when trying to combine the dataset with other datasets, as others do not use ZCTA. Second, the dataset does not include any information on businesses, which is a major issue when considering the first issue. This resulted in the requirement to remove business evaluations from the analysis. 

The dataset is also compiled of yearly 5-year estimates. Since the data consists of estimates instead of actual measured information, there is a margin of error to be considered. 

Another limitation encountered was lack of normalized data hindering the allowance of standard measures of statistical significance. By randomizing the sample, it is possible that the data would follow a more normal distribution. This could be achieved by selecting counties from various regions across the country, selecting cities within the same population size, or selecting counties that encompass the same number of zip codes.



## Contributors
Tamica Grant @mznatural1
Rhi Sehl @rhisehl
Stephanie Wortman @steph-anie-w
Jonathan Yang @jonyang6483



## Data Source
U.S. Census Bureau's 2011-2020 American Community Survey 5-year estimates.


## Presentation Link: https://docs.google.com/presentation/d/1aP3LpN0I7wvI7JVMIW3sNT85-CmN-v7WTlT7C2ULqh4/edit?usp=sharing

