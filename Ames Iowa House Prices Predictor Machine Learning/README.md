# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Ames Housing Data analysis

## Problem Statement
This project aims to study housing data and find the features that add the most value to a home.  
Inversely we want to look at features that will bring the value of a house down.   
We will also will look into what areas will be lucrative to sell a home based on our models predictions.  
It will give real estate agents / investors a visualization of what houses to keep an aye out for and negotiate when selling.

## Summary
- What are the top features of the house that increases its selling price and what are the features negatively impacting the house price? 
- What neighborhoods are good hotzones for house price?
- Can features that lowly impact the saleprice be combined (interaction terms) to have a stronger impact on the sale price?
- Which regression gives the better scores between Linear, LASSO, and Ridge.


## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|pid|int|Ames Housing dataset |Personal ID of the house| 
|ms_subclass|int|Ames Housing dataset |The building class| 
|lot_frontage|float|Ames Housing dataset |Linear feet of street connected to property| 
|lot_area|int|Ames Housing dataset |Lot size in square feet| 
|overall_qual|int|Ames Housing dataset |Overall material and finish quality| 
|overall_cond|int|Ames Housing dataset |Overall condition rating| 
|year_built|int|Ames Housing dataset |Original construction date| 
|year_remod/add|int|Ames Housing dataset |Remodel date (same as construction date if no remodeling or additions)| 
|mas_vnr_area|float|Ames Housing dataset |Masonry veneer area in square feet| 
|bsmtfin_sf_1|float|Ames Housing dataset |Type 1 finished square feet| 
|bsmt_unf_sf|float|Ames Housing dataset |Unfinished square feet of basement area| 
|total_bsmt_sf|float|Ames Housing dataset |Total square feet of basement area| 
|1st_flr_sf|int|Ames Housing dataset |First Floor square feet| 
|2nd_flr_sf|int|Ames Housing dataset |Second floor square feet| 
|gr_liv_area|int|Ames Housing dataset |Above grade (ground) living area square feet| 
|bsmt_full_bath|float|Ames Housing dataset |Basement full bathrooms| 
|bedroom_abvgr|int|Ames Housing dataset |Number of bedrooms above basement level| 
|kitchen_abvgr|int|Ames Housing dataset |Number of kitchens| 
|totrms_abvgrd|int|Ames Housing dataset |Total rooms above grade (does not include bathrooms)| 
|fireplaces|int|Ames Housing dataset |Number of fireplaces| 
|garage_yr_blt|float|Ames Housing dataset |Year garage was built| 
|garage_cars|float|Ames Housing dataset |Size of garage in car capacity| 
|garage_area|float|Ames Housing dataset |Size of garage in square feet| 
|wood_deck_sf|int|Ames Housing dataset |Wood deck area in square feet| 
|screen_porch|int|Ames Housing dataset |Screen porch area in square feet| 
|pool_area|int|Ames Housing dataset |Pool area in square feet| 
|misc_val|int|Ames Housing dataset |Value of miscellaneous feature| 
|yr_sold|int|Ames Housing dataset |Year Sold| 
|ms_zoning|object|Ames Housing dataset |Identifies the general zoning classification of the sale| 
|neighborhood|object|Ames Housing dataset |Physical locations within Ames city limits| 
|fireplaces*totrms_abvgrd|int|Ames Housing dataset |Interaction Term| 
|screen_porch*wood_deck_sf|int|Ames Housing dataset |Interaction Term| 


## Conclusion and Recommendations
After fitting my regression models, Linear and LASSO  got the best score and prediction for training and testing on my model.
Linear regression got an MSE on my trained data of 21,374 and on the tested data 24,580
Lasso regression got an MSE on my trained data of 21,374 and on the tested data 24,578
Ridge regression got an MSE on my trained data of 21,465 and on the tested data 24,594
All 3 of the regression models had very similar R2 scores where al 
They all were very near each other in their scores and predictions, but I went with the Linear Regression Model to conclude my findings. 

Aftering scaling and fitting my data into the regression model we can see the coefficients that greatly affect our sale price target. 
The top 5 features that give the best sale price are: 

YearBuilt, Overall Quality, 1st Floor Square Feet, 2nd Floor Square Feet, and BsmtFinSF1: Type1 finished square feet.

For every one unit increase in 1 standard deviation of Overall Quality, the Sale Price increases by about $16k.

For every one unit increase in 1 standard deviation of 2nd Floor Square Ft, the Sale Price increases by about $18k.

For every one unit increase in 1 standard deviation of 1st Floor Square Ft, the Sale Price increases by about $17k.

For every one unit increase in 1 standard deviation of BsmtFinSF1, the Sale Price increases by about $10k.

For every one unit increase in 1 standard deviation of Year Built, the Sale Price increases by about $15k.

some features that negatively impact the sale price of the house are Fireplaces and MSSubclass.  Fireplace brings down my sale price down by about $7.8k.

But when combining it with my Total Rooms Above Grade feature to make an interaciton term, it adds value to the house massively by about $10.8k.

Now the neighborhoods bringing the greatest value to the sale price of a house would be Crawford, Stone Brook and Northridge Heights.

Crawford increases the price by $4.7k, Morthridge Heights by $8k, and Stone Brooks by $6.2k.


In conclusion, you would want to sell/invest in a house around one of the three neightborhoods mentioned above. On top of that, when you 

are looking at a house to sell or invest in, search for a house with great Overall Quality, 1st Floor Square footage, 2nd Floor Square footage, the Year it was built

and a finished Basement.  

## What's next?
Future study/research:
- To build a similar model to predict houses statewide and eventually nationwide.
- Analyze housing data to see if it is affected by foreign investments 
- 
