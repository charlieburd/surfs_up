# Module 9 - Surfs Up Analysis

## Overview of Surfs Up Analysis


#### The Surfs Up Module was to run an analysis to help us make a decision about creating a Surf and Ice Cream store in Oahu, Hawaii. Our business partner, A. Wavy, had already had one failed venture due to weather and wanted to see if the data returned supported the idea of starting another venture in this location. In the module we looked at yearly precipitation. For the analysis A. Wavy wanted to look at temperature for the months of June and Dec.


## Surfs Up Analysis Results
### Deliverable 1/2 Comparison
 * With Hawaii being the closest US state to the equator we see that there is a very small difference in temperature between June and Dec. The average temperature for June was 74.9 degrees Fahrenheit. While the average temperature for Dec as 71.0 degrees Fahrenheit. 

 * When we look at averages there is a very small different in temp between June and Dec in Oahu. The `describe()` function also give us standard deviation (std), I think this is an important statistic because it shows which month is going to have a larger range of temperatures, and in return be harder to predict how busy the store will be. The std for June is 3.25 and the std for Dec is 3.74. So the temperature swings are both minimal, but A. Wavy can expect that Dec will lead to a bit more uncertainty compared to June.

 * The minimum temperature June and Dec has a larger swing that the average did. In June it reached a low of 64.0 degrees Fahrenheit. And in Dec it reached a low of 56.0 degrees Fahrenheit. A spread of 8 degrees, compared to spread of 3.9 degrees when comparing averages. 
 
 * The maximum temperature June and Dec are almost even. In June it reached a high of 85.0 degrees Fahrenheit. And in Dec it reached a high of 83.0 degrees Fahrenheit. A spread of only 2 degrees different. It is fair to say Oahu is not very seasonal, at least temperature wise.

 
 
#### June Temperature  Statistics
![stacked_launch_outcomes](https://github.com/charlieburd/surfs_up/blob/main/june_temps.png)

#### Dec Temperature  Statistics
![stacked_launch_outcomes](https://github.com/charlieburd/surfs_up/blob/main/dec_temps.png)
#


## Surfs Analysis Summary:

#### A. Wavy wanted this analysis to determine if the store would be sustainable year-round. The differences in temperature between June and Dec are minimal. I believe this supports the verdict, that yes, the store is sustainable year-round.

#### While temperature swings will likely not affect the Surf and Ice Cream, it would be nice to know when they can expect rain. In the module we created at a yearly precipitation graph, but we can also modify our code to show the statistics description for precipitation between June and Dec. The average precipitation in June is .17 inches a day compared to an average of .22 inches a day for Dec. So A. Avery and I can clearly expect more rain in Dec, even though the average temperatures are pretty similar
##### * Additional queries can be found in SurfsUp_Challenge.ipynb

#### June Precipitation Code
`june2 = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6)`

`june_list_prcp = [prcp for prcp in june2]`

#### Dec Precipitation Code
`dec2 = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12)`

`dec_list_prcp = [prcp for prcp in dec2]`
