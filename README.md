# Finding a good location for 'Home from Home' in England
## Introduction
In the past year, Hong Kong has been on the world's newspapers' headlines more often than the past decade combined. Unprecedented police brutality and violent conflicts in the street has unfortunately become part of everyday life. People in this vibrant metropolitan city fear the loss of Hong Kong's freedoms. Following the Chinese government’s decision to impose a new National Security Law on Hong Kong, the UK government has committed to open a new immigration route to the British National (Overseas) passport holders in Hong Kong.

Despite many well-travelled Hong Kongers have been to London for holidays, it is still a challenge to learn everything about life in the UK for an uprooting move. There are numerous videos, social media posts, blogs and forums flowing with varying subjective opinions and information of mixed quality. Therefore, there is a need to leverage good quality data and data science techniques to help them make an informed decision in selecting the right location to settle down as 'home from home'. This project will cover the following criteria:

- Property price
- Employment rate
- Education
- Crime rate
- Availability of Chinese restaurant

## Data
To make this project more manageable, I have limited the scope to England only. The approach is using County as defined by this governement source https://geoportal.statistics.gov.uk/datasets/counties-april-2019-names-and-codes-in-england plus adding in London as the unit of this project. Data will be gathered for each critieria as detailed below. The data will be merged and cleaned to fill in any gap. Then, the cleansed data will be normalised into scores for the corresponding criteria to avoid varying magnitude of data value skewing the overall scoring system. At the end, the outcome of this project is a ranking of ideal 'home from home' locations.

### Property price
The UK House Price Index published in January 2020 will be used to . https://www.gov.uk/government/publications/uk-house-price-index-england-january-2020/uk-house-price-index-england-january-2020
