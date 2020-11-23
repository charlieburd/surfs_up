# Module 9 - Surfs Up Analysis

## Overview of Surfs Up Analysis


#### The Surfs Up Module was to run an analysis to help us make a decision about creating a Surf and Ice Cream store in Oahu, Hawaii. Our business partner, A. Wavy, had already had one failed venture due to weather and wanted to see if the data returned supported the idea of starting another vanture in this location. In the module we looked at yearly percepitation. For the analysis A. Wavy wanted to look at tempature for the months of June and Dec. 


## Surfs Up Analysis Results
### Deliverable 1/2 Comparison
 * With Hawaii being the closest US state to the equator we see that there is a very small difference in tempature between June and Dec. The average tempature for June was 74.9 degrees Fahrenheit. While the average tempature for Dec as 71.0 degrees Fahrenheit. 
 
 * The minimum tempature June and Dec has a larger swing that the average did. In June it reached a low of 64.0 degrees Fahrenheit. And in Dec it reached a low of 56.0 degrees Fahrenheit. A spread of 8 degrees, compared to spread of 3.9 degrees when comparing averages.

 * The maximum tempature June and Dec are almost even. In June it reached a high of 85.0 degrees Fahrenheit. And in Dec it reached a high of 83.0 degrees Fahrenheit. A spread of only 2 degrees different. It is fair to say Oahu is not very seasonal, at least tempature wise.
 
 
#### June Tempature Statistics
![stacked_launch_outcomes](https://github.com/charlieburd/surfs_up/blob/main/june_temps.png)

#### Dec Tempature Statistics
![stacked_launch_outcomes](https://github.com/charlieburd/surfs_up/blob/main/dec_temps.png)
#


## Surfs Analysis Summary:

### How many roles will need to be filled as the "silver tsunami" begins to make an impact?
#### If we look at our "retiring_titles" tables, we get the count for each department, after we change the code to below, it will display the total amount of roles that will need to be filled. There are 90,398 roles that will need to be filled.
`SELECT COUNT (title)
FROM unique_titles;`
### Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
#### No, as I had mentioned in fourth bullet above, there will be a sever lack of mentors, given the large number of roles needed to be filled it would be a challenge to provide enough mentors for all the open roles, even if it were in groups. Some mentor to mentee ratio of departments will be as high as 1-60. To look at this table we will use the below code:
`SELECT COUNT (title), title
FROM mentorship_eligibility
GROUP BY title
ORDER BY count DESC;`
