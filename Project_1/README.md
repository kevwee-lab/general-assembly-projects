# Project 1: SAT & ACT Analysis
## Problem Statement
The SAT and the ACT are standardized tests widely used for college admissions in the US. Our competitors ACT have seen a steady increase in participation rates, and in 2012, surpassed the SAT for the first time in terms of total test takers. As an employee of the College Board which administers the SAT, my role is to perform exploratory data analysis on the 2017/2018 ACT and SAT data to figure out the following: <BR>
Where we can best spend money to improve SAT participation rates in the US?
## Executive Summary

The dataset contains average test scores, total mean/composite test scores and participation rates from 2017 to 2018.

#### Methodology

The workflow for the data analysis was as follows:
1) Datasets were read and converted into a **Pandas DataFrame**
2) **Data cleaning** was conducted to ensure that there were no errors in the values of the data and that all the datatypes were correctly cast.
3) All datasets were then merged into a single dataframe.
4) **Exploratory data analysis** was conducted to make estimates and observe trends in the data.
5) **Visualizations** were then made to help reinforce the observations, e.g. heatmaps, subplots, histograms, scatterplots and boxplots.
6) **Descriptive and inferential statistical analysis** was then conducted to desctibe the distributions.
7) Combined with research about the SAT and ACT from external sources, recommendations for the College Board were then compiled and presented.

#### Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT/SAT|States in the US|
|sat_2017_part_rate|float|SAT|Statewide participation rate in 2017 SAT|
|sat2017_read_write|int|SAT|2017 Mean SAT score of state for evidence-based reading and writing|
|sat2017_math|int|SAT|2017 Mean SAT score of state for math|
|sat2017_total|int|SAT|2017 Mean total SAT score of state|
|act_2017_part_rate|float|ACT|Statewide participation rate in 2017 ACT|
|act_2017_eng|float|ACT|2017 Mean ACT score of state for English|
|act_2017_math|float|ACT|2017 Mean ACT score of state for Math|
|act_2017_read|float|ACT|2017 Mean ACT score of state for Reading|
|act_2017_sci|float|ACT|2017 Mean ACT score of state for Science|
|act_2017_avgscore|float|ACT|2017 Mean composite ACT score of state| 
|sat_2018_part_rate|float|SAT|Statewide participation rate in 2018 SAT|
|sat2018_read_write|int|SAT|2018 Mean SAT score of state for evidence-based reading and writing|
|sat2018_math|int|SAT|2018 Mean SAT score of state for math|
|sat2018_total|int|SAT|2018 Mean total SAT score of state|
|act_2018_part_rate|float|ACT|Statewide participation rate in 2018 ACT|
|act_2018_eng|float|ACT|2018 Mean ACT score of state for English|
|act_2018_math|float|ACT|2018 Mean ACT score of state for Math|
|act_2018_read|float|ACT|2018 Mean ACT score of state for Reading|
|act_2018_sci|float|ACT|2018 Mean ACT score of state for Science|
|act_2018_avgscore|float|ACT|2018 Mean composite ACT score of state| 
|sat_part_change|float|SAT|change in participation rate for SAT|
|act_part_change|float|ACT|change in participation rate for ACT| 

#### Findings
1) **Public policy is a key driver to increasing SAT participation rates**: As we have seen in the case of Colorado and Illinois, working with education boards or department of education in the respective states have helped to push SAT participation rates greatly. <br> <br>
2) **Increased participation rates are negatively correlated to test scores**: One of the reasons could be due to high achieving students taking both tests to boost their college admission chances. Another possible reason could be that with sudden mandates or changes in contracts, schools need time to adjust to the new test and prep their students to take it. This is why scores could dip in the short term. More data on scores over time would be required to examine if this is true.<br><br>
3) **SAT participation rate has seen some moderate success**: More states achieved 90% to 100% participation rates for SAT in 2018, from 7 in 2017 to 10 in 2018. More can be done to increase the participation rate in other states.


## Conclusions and Recommendations
Based on the above takeaways, we recommend that the College Board consider the following strategies:

1) **Target states that have yet to mandate any tests, and are more receptive towards SAT**: Based on this [article](https://magoosh.com/hs/sat/states-that-require-the-act-or-sat/), states on the map that are greyed out are currently not legally required to take the SAT or ACT. The College Board could consider working with the state department of education to administer and mandate the SAT in states that show a more favourable reception to the SAT. This way, we could provide schools with ample lead time to change their systems (unlike the case of West Virginia and Illinois where the school systems were more aligned to ACT). This could also help to improve SAT scores. <br>
The states that fit the criteria are Washington, California, Alaska, New York, Pennsylvania, Georgia and Texas.
2) **Provide SAT School Day for schools in the abovementioned states**: The SAT costs [64.50 to take in 2018 with the optional essay component, and 47.50 without.](https://www.edmit.me/blog/how-much-does-it-cost-to-take-the-sat-how-much-does-it-cost-to-take-the-act#:~:text=SAT%20testing%20fees%20are%20set,optional%20essay%20component%20is%20%2464.50.) This could be a hefty sum for low income families. Therefore, introducing SAT School Days to offer the SAT at no cost to students could also increase the SAT participation rate.

3) **Help students become more aware of free resources, e.g. Khan Academy**: An increase in awareness of available tools and resources could help students better prepare for the SAT, and thus improve SAT scores and increase take up for SAT
