## AMES Housing Project 
<hr/>

### Problem Statement

Prospective homeowners are faced with a deluge of considerations when it comes to decisions regarding property purchase. Some of these considerations might include:
1) What is the condition of the property? <br>
2) How old is the property? <br>
3) Will the value of my property rise? Is this dependent on what kind of future development will take place near my area (e.g. Industrial/Commercial, etc.)? <br>

We want to help prospective homeowners in Ames, Iowa to make informed decisions about which property they should consider purchasing for best value. We also want to help prospective sellers to determine how to maximise the value of their sales. <br>

Specifically, our problem statement is as such:

**Which features of a property will have an effect on the sale price?** <br>

In this project, we will be building and evaluating machine learning models to help predict housing prices based on a set of features.

### Executive Summary 

We use the dataset of residential property sold in Ames, Iowa from 2006 to 2010. The data dictionary can be found [here](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt). <br>
To build the model, we did the following steps: <br>
1) Read the data into a pandas dataframe <br>
2) Grouped the data into categories and filled the null values <br>
3) Performed exploratory data analysis to examine relationships between features. (using correlation and looking at their distributions). <br>
4) Transformed other features to minimise multicollinearity by adding them together or dropping them. <br>
5) Built and evaluated Linear, Ridge and Lasso models using a preselected set of 23 features. <br>
6) Hot encoded categorical features then merged them back together with scaled numerical features. Total features used was 117.<br>
6) Selected features (64) not zeroed out by Lasso to build final production model. <br>
7) Submitted model predictions to kaggle to assess how well the model generalises against unseen data. <br>

### Findings

For the set of features that were selected to build the Linear, Lasso and Ridge regression models, we found that the Ridge regression model performed the best, achieving low RMSE and high R2 scores consistently for both train and holdout test sets. We therefore selected Ridge regression as the final production model for our submission to Kaggle. 

Our final RMSE was around 30895 (scored by Kaggle) against our own training prediction RMSE of around 25880. This seems to imply that our model generalises reasonably well on unseen data. <br>

### Conclusion and recommendations 
In our process of developing our production model for Ames property sale price predictions, we see that a few features have a huge influence in the sale price of a property: <br>
1) **Neighborhood**: The neighborhood the property is located in. <br> 
2) **Quality**: The overall finishing and material of the house. <br>
3) **Square Feet**: The size of the property. <br> 
4) **Materials e.g. Foundation, Roof** : The materials used to construct the property <br> 

Surprisingly, the age of the property did not influence the sale price as much as we initially assumed. Maintenance and remodelling of homes seemed to matter more, and could [add years to the useful life of a home.](https://www.adn.com/business-economy/2018/06/21/the-age-of-your-house-isnt-just-based-on-the-year-it-was-built-heres-why-thats-important-when-youre-selling-your-home/) <br>

Homeowners could consider doing some remodelling to increase the value of their property and maintain their homes. <br>

These neighborhoods in Ames seem like a good investment: 
1) **Stone Brook** : A few minutes drive from the [Iowa State University campus](https://www.stonebrooke.org/).  <br>
2) **Northridge Heights** : Located to thriving [Gilbert school district](https://www.hunzikerdevelopment.com/active-developments/northridge-heights/). <br> 
3) **Green Hills**: Retirement community for [Iowa State University alumni](https://greenhillsrc.com/about-us/).

We will not be able to generalise this model to other cities as the data seems to be Ames specific. To be able to generalise our model we would need more generic features to be included in the dataset such as distance to amenities, e.g. schools, malls etc. This seems to have some correlation to neighborhood as we observe from the top 3 neighborhoods for property investment in Ames.

