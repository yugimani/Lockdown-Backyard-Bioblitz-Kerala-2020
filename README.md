# Lockdown-Backyard-Bioblitz-Kerala-2020
An Analysis of Data from Observations made under Lockdwon-Backyard-Bioblitz-Kerala project in iNaturalist between March to June 2020. 

iNaturalist data can be accessed as a snapshot of research-grade only observations from [GBIF](https://www.gbif.org/publisher/28eb1a3f-1c15-4a95-931a-4af90ecb574d) or on-demand of all observations using [REST APIs](https://www.inaturalist.org/pages/api+reference). 

Below is an example to get Project specific observations. 
```curl
curl --location --request GET 'https://www.inaturalist.org/observations/project/70438?page=36&per_page=200&order_by=date_added&order=desc&license=any' \
--header 'Content-Type: application/json'
```

iNaturalist APIs serve up to 200 records per response. You would have to paginate to get all observations and that's fairly easy to do programmatically. For Python users, [pyinaturalist](https://github.com/niconoe/pyinaturalist) can be handy. 

For manual one-off experiments, the [export](https://www.inaturalist.org/observations/export) feature in iNat can be very useful. 

## Tools:
1. Postman
1. Tableau Public
1. Jupyter Notebook
1. Microsoft Excel

## APIs:
1. LocationIQ
1. iNaturalist

## Python packages:
1. pyinaturalist
1. pandas
1. location-iq

## Animation Steps:
1. Using any RESTful client, get all observations in JSON format. cURL and Python would do just fine. 
1. Create a dataset in Tableau Public and 'unionize' all observations into a table. 
1. Export just the *user_login, Observed_On, SUM([Id])* measures. 
1. Fill gaps in time series using Jupyter Notebook.
1. Calculate running total using Excel.
1. Visualize using Tableau Public

**Note** A lot of these steps could possibly be simplified with better understanding of Tableau, Python and Excel. If you do, reach out to me. 

## Visualization
[Bioblitz Animation](https://public.tableau.com/views/Lockdwon-Backyard-Bioblitz-Kerala-2020/ObserversLeaderboard?:language=en&:display_count=y&:origin=viz_share_link)

## Citations:
GBIF.org (15 June 2020) GBIF Occurrence [Download](https://doi.org/10.15468/dl.kdespa)

## Copyright
* Code and Visualization are publised under Apache License. For any information on derivative work, please contact Yugender Subramanian - checkout.yugimani@gmail.com. 
* Source data is published under multiple licenses by iNaturalist. For any information on data, please contact [iNaturalist](https://www.inaturalist.org/pages/help)

## Credits
* Visualizations were inspired from TowardsDataScience and Reddit. Thanks to respective authors. 
* Thanks to iNat community
* Thanks to Tableau community
* Thanks to LocationIQ
* Thanks to Reddit r/dataisbeautiful community
