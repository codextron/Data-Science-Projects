# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Problem Statement
This project aims to study SAT scores and compare them to their counterparts.  We will be looking at the trend of SAT participation and scores from 2017 to 2019. Also, we will be looking at the major west coast states (CA, OR, WA) and compare their SAT scores and statistics to a few east coast states that are not mandated to take the SATs.  We hope to find strengths/weaknesses of the states test takers and decide which one needs help allocating resourches to improve test scores.
## Summary
- What are the participation rates looking like for the SATs from 2017-2019 and do they affect the states average SAT score?
- Which coast is better at the SATs? West or East?
- Whose scoring higher on the Math portion of the SATs and Reading/Writing portion?
- Looking at the trends, what states might need more resources for education to raise test scores?


## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|Name of states|50 states of the USA and District of Columbia| 
|participation_2017|float|SAT 2017 Data|The partipcation rate of students that took the SAT in 2017 in that state (unit is in decimal, where .50 represents %50)| 
|reading_writing_score_2017|int|SAT 2017 Data|Mean score of the reading & writing score of students that took the SAT in 2017| 
|math_score_2017|int|SAT 2017 Data|Mean score of the math score of students that took the SAT in 2017 | 
|sat_total_2017|int|SAT 2017 Data|Mean score of the students combined score of math score & reading/writing score for the SAT in 2017| 
|participation_2018|float|SAT 2018 Data|The partipcation rate of students that took the SAT in 2018 in that state (unit is in decimal, where .50 represents %50)| 
|reading_writing_score_2018|int|SAT 2018 Data|Mean score of the reading & writing score of students that took the SAT in 2018| 
|math_score_2018|int|SAT 2018 Data|Mean score of the math score of students that took the SAT in 2018 | 
|sat_total_2018|int|SAT 2018 Data|Mean score of the students combined score of math score & reading/writing score for the SAT in 2018| 
|participation_2019|float|SAT 2019 Data|The partipcation rate of students that took the SAT in 2019 in that state (unit is in decimal, where .50 represents %50)| 
|reading_writing_score_2019|int|SAT 2019 Data|Mean score of the reading & writing score of students that took the SAT in 2019| 
|math_score_2019|int|SAT 2019 Data|Mean score of the math score of students that took the SAT in 2019 | 
|sat_total_2019|int|SAT 2019 Data|Mean score of the students combined score of math score & reading/writing score for the SAT in 2019|

## Conclusion and Recommendations
As state participation increases for taking the SAT, the average score goes down. The highest average scoring states (Mississippi, North Dakota, Iowan, Wyoming, and Wisconsin) were the least participating states for the States.  Inversely, the lowest scoring states (Connecticut, Delaware, Michigan, District of Columbia, and New Hampshire) had the highest participation rates for the SATs.

# ![](https://m.media-amazon.com/images/I/71HbeKyARtL._SS500_.jpg) 

Now looking at the big west coast states versus a few east coast states. These states that were chosen are in the middle of the pack for participation in the SATs.  East coast states were chosen based on participation rates that almost matches the rates of the west coast states of CA, OR, and WA. East coast states that were chosen are NY, VA, and NC. Averaging out the east and west coasts total SAT score, they have a 1 point difference in the Sat_total_2017 score.  The competing states do not have a stark difference in scores, but east coast pulls ahead slightly against the west coast states in Math, Reading/Writing and Total SAT score.

States that are fully participating in taking the SATs could invest more into quality education to prepare students for taking them and get higher scores out of them. Looking at the battle between east coast versus west coast states, boths sides have room for improvement.  Looking at California, they are the richest state in the country.  They should invest more into education that prepares the student for SAT and college to increase the college graduation rate and also create an educated individual to prepare them for the job market.

## What's next?
Future study/research:
- Look into the correlation between test scores and family income the student comes from.
- Do high class students do better then low class students?
- Do SATs really prepare a student for college and the world beyond?
