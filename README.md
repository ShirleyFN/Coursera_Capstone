# Finding a good location for 'Home from Home' in England
## Introduction
In the past year, Hong Kong has been on the world's newspapers' headlines more often than the past decade combined. Unprecedented police brutality and violent conflicts in the street has unfortunately become part of everyday life. People in this vibrant metropolitan city fear the loss of Hong Kong's freedoms. Following the Chinese government’s decision to impose a new National Security Law on Hong Kong, the UK government has committed to open a new immigration route to the British National (Overseas) passport holders in Hong Kong.

Despite many well-travelled Hong Kongers have been to London for holidays, it is still a challenge to learn everything about life in the UK for an uprooting move. There are numerous videos, social media posts, blogs and forums flowing with varying subjective opinions and information of mixed quality. Therefore, there is a need to leverage good quality data and data science techniques to help them make an informed decision in selecting the right location to settle down as 'home from home'. This project will cover the following criteria:

- Property price
- Employment rate
- Education
- Crime rate
- Chinese restaurant

## Data
To make this project more manageable, I have limited the scope to England counties and London only. The approach is using County as defined by this governement source https://geoportal.statistics.gov.uk/datasets/counties-april-2019-names-and-codes-in-england plus adding in London as the regional unit of this project. Data will be gathered for each critieria as detailed below. The data will be merged and cleaned to fill in any gap. Then, the cleansed data will be normalised into scores for the corresponding criteria to avoid varying magnitude of data value skewing the overall scoring system. At the end, the outcome of this project is a ranking of ideal 'home from home' locations.

### Property price
The Annual Price Change by Local Authority for England data https://www.gov.uk/government/publications/uk-house-price-index-england-january-2020/uk-house-price-index-england-january-2020 will be used to get property price in January 2020. A data wrangling will take place to convert local authority data into county level data based on this table https://geoportal.statistics.gov.uk/datasets/local-authority-district-to-county-december-2018-lookup-in-england/data  

### Employment rate
The Employment data is a little tricky to find based on my desktop research. Only regional data is available from the Office for National Statistics. Nevertheless, there is nomis that provides official labour market statistics https://www.nomisweb.co.uk/reports/lmp/la/1941962882/report.aspx I haven't quite figured out a perfect way to extract all the county level data in one go, yet there is always a manual approach to construct data source using the Local Area Report option as my last resort.

### Education
To compare school performance, the 2018-2019 Final Key Stage 2 and Final Key Stage 4 results are used. https://www.compare-school-performance.service.gov.uk/download-data?currentstep=datatypes&regiontype=all&la=0&downloadYear=2018-2019&datatypes=ks2&datatypes=ks4 More data wrangling will be required to a) convert subject performance into score; b) categorise schools by local authority; c) wrangle them to match county or London regional unit; d) consolidate data into county level.

### Crime rate
Crime in England and Walse: Police Force Area data tables Year ending December 2019 will be used. https://www.ons.gov.uk/peoplepopulationandcommunity/crimeandjustice/datasets/policeforceareadatatables Similar data wrangling to convert police force area into county level is required.

### Chinese restaurant
Last but truly not least, availability of Chinese restaurant is a cure to home sick and critical to newly immigrated Hong Kongers' mental wellness. Foursquare data will be used to analyse availability of Chinese restaurant on the county level.
