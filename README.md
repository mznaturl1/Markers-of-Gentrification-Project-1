# Measures of Gentrification Across Oakland, Kent, and Saginaw Counties, Michigan

## Background

## Technologies Used


## Description of Data Exploration

The data was compiled using the Census API's Python wrapper. The chosen variables were the most likely to show indications of gentrification across each county: population size, poverty rates, unemployment rates, income, home values, and rent prices. 

This data was pulled into a dataframe and then all financial variables were converted to 2023 rates using an inflation module.

Additional columns were created for the percentage of the population unemployed, percentage in poverty, and some additional separations based on race. 

The years 2011 - 2020 were chosen as a full and complete decade. These could easily be changed by shifting the API to call the desired years, as well as changing some of the iterators that ran per-year.


Using the Shapiro-Wilk test, all variables per county were checked for normality. In all cases, the p-value was greater than .05, indicating that none of the variables were normally distributed. As a result, the standard measures of statistical significance could not be utilized, since they assume normality. 

Oakland County has 66 zipcodes, while Saginaw has 25 and Kent has 31. 

Oakland County has the highest Adjusted Median Income at almost $92,000, while Saginaw and Kent are between $60-70,000. 
Saginaw County has the least population per zip code, with a median of 6162, compared to around 20,000 for Kent and Oakland.

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
Kent County endured declines in home values for each year between 2011- 2018.  Leading into 2020, home values began to surge, centered in the middle of the county. Of the three counties observed, Kent County has the alternate loftiest values, With an Adjusted Median Home Value of$179928.63. 

![Kent_Home](https://user-images.githubusercontent.com/116215793/218327142-5c4ea4ed-2aa2-4f75-b68f-9fdff67c90c5.gif)
![kent_linregress_adj_median_home_value](https://user-images.githubusercontent.com/117309455/218925038-c7554281-aa32-42c8-8afe-c3f27f8e368a.png)


**Oakland County**
Nearly the entire county of Oakland realizes a major increases in home values. The only area with nearly no change is at the center of the county. The Central Southern Region of the county holds an area of slower growth compared to the remainder of the county. Of the three counties, Oakland has a median Acclimated Median Home Value of $255,798.19.

![Oakland_Home](https://user-images.githubusercontent.com/116215793/218326104-1f66a070-9e3d-49d2-af9a-3c0b6951d3f6.gif)
![oakland_linregress_adj_median_home_value](https://user-images.githubusercontent.com/117309455/218924603-dc9f335c-194a-4201-b6ea-5715020d628b.png)


**Saginaw County**
Saginaw, interestingly, shows a loss of home value over time (2011-2018). Home values begin to increase steadily in leading to 2019 and 2020. The Adjusted Median Home Value is $184,227.49 for the 2011-2020 time frame.

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

Poverty rates shift around the county for the first half of the decade, then drop significantly in the second half of the decade. The largest pocket of poverty remains in the center of the county.

![Kent_Poverty](https://user-images.githubusercontent.com/116215793/218326232-9a29aec2-b8bc-4763-a71c-381a02d28e91.gif)

Poverty rates actually grow in the center of the county for the first half of the decade, then see a slight reduction in the second half. The Southeast corner of the county sees this trend as well, but with a major reduction overall.

![Oakland_Poverty](https://user-images.githubusercontent.com/116215793/218326235-00d70fd5-34c8-4837-b051-89e7332031be.gif)


There is no major overall change in poverty rates across the decade. 

![Saginaw_Poverty](https://user-images.githubusercontent.com/116215793/218326239-dc1371a1-be88-4a80-9bb2-73d001b677f4.gif)


## Limitations of the Dataset and Future Considerations

## Contributors
Tamica Grant @mznatural1
Rhi Sehl @rhisehl
Stephanie Wortman @steph-anie-w
Jonathan Yang


## Data Source
U.S. Census Bureau's 2011-2020 American Community Survey 5-year estimates.




