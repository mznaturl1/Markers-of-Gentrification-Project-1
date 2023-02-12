# Measures of Gentrification Across Oakland, Kent, and Saginaw Counties, Michigan

## Sourcing the Data

The data was compiled using the Census API's Python wrapper. The chosen variables were the most likely to show indications of gentrification across each county: population size, poverty rates, unemployment rates, income, home values, and rent prices. 

This data was pulled into a dataframe and then all financial variables were converted to 2023 rates using an inflation module.

Additional columns were created for the percentage of the population unemployed, percentage in poverty, and some additional separations based on race. 

The years 2011 - 2020 were chosen as a full and complete decade. These could easily be changed by shifting the API to call the desired years, as well as changing some of the iterators that ran per-year.


## Summary Statistics

Using the Shapiro-Wilk test, all variables per county were checked for normality. In all cases, the p-value was greater than .05, indicating that none of the variables were normally distributed. As a result, the standard measures of statistical significance could not be utilized, since they assume normality. 

Oakland County has 66 zipcodes, while Saginaw has 25 and Kent has 31. 

Oakland County has the highest Adjusted Median Income at almost $92,000, while Saginaw and Kent are between $60-70,000. 
Saginaw County has the least population per zip code, with a median of 6162, compared to around 20,000 for Kent and Oakland.

## Adjusted Median Income

![Kent_Income](https://user-images.githubusercontent.com/116215793/218327133-9aa3cf37-7ecf-4b12-b214-a1a2bec7cc70.gif)

![Oakland_Income](https://user-images.githubusercontent.com/116215793/218326035-350ca797-00ca-4eab-a693-733916ba23f8.gif)

![Saginaw_Income](https://user-images.githubusercontent.com/116215793/218326041-1b5436b6-bffe-45cd-96a6-0caed5b38287.gif)


## Adjusted Median Home Values

![Kent_Home](https://user-images.githubusercontent.com/116215793/218327142-5c4ea4ed-2aa2-4f75-b68f-9fdff67c90c5.gif)

![Oakland_Home](https://user-images.githubusercontent.com/116215793/218326104-1f66a070-9e3d-49d2-af9a-3c0b6951d3f6.gif)

![Saginaw_Home](https://user-images.githubusercontent.com/116215793/218326112-b1fd442c-abec-4abc-b1e6-6d6f79b449d7.gif)


# Adjusted Median Rent Prices

![Kent_Rent](https://user-images.githubusercontent.com/116215793/218326128-688305ab-6c45-4ece-b897-b035a962aa18.gif)

![Oakland_Rent](https://user-images.githubusercontent.com/116215793/218326138-4e9c53e1-4832-4b71-ac66-57c090a304bf.gif)

![Saginaw_Rent](https://user-images.githubusercontent.com/116215793/218326145-feaff192-1b4f-45c5-9c49-00c80bbf8e31.gif)


# Total Population

![Kent_Population](https://user-images.githubusercontent.com/116215793/218326157-8ce13ccd-353d-4b70-baba-313eb6e9d46e.gif)

![Oakland_Population](https://user-images.githubusercontent.com/116215793/218326164-0ad0dc4e-a5fc-4f91-8015-540f8f67c981.gif)

![Saginaw_Population](https://user-images.githubusercontent.com/116215793/218326177-f09c05b5-e119-479d-acef-2a1685d6bc3f.gif)


# Percent of Population Unemployed

![Kent_UE](https://user-images.githubusercontent.com/116215793/218327158-b23161fe-a7f3-4d22-a9db-01f8a75bf25e.gif)

![Oakland_UE](https://user-images.githubusercontent.com/116215793/218326217-9470ea90-5025-4f5a-b097-dc34241ad8d1.gif)

![Saginaw_UE](https://user-images.githubusercontent.com/116215793/218326223-9a04020d-e367-4fb7-9406-6fcc40776acc.gif)


# Percent of Population in Poverty

![Kent_Poverty](https://user-images.githubusercontent.com/116215793/218326232-9a29aec2-b8bc-4763-a71c-381a02d28e91.gif)

![Oakland_Poverty](https://user-images.githubusercontent.com/116215793/218326235-00d70fd5-34c8-4837-b051-89e7332031be.gif)

![Saginaw_Poverty](https://user-images.githubusercontent.com/116215793/218326239-dc1371a1-be88-4a80-9bb2-73d001b677f4.gif)





