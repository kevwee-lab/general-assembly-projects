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
We see that a few features have a huge influence in the sale price of a property: <br>
1) **Neighborhood**: The neighborhood the property is located in. <br> <br>
2) **Quality**: The overall finishing and material of the house. <br><br> 
3) **Square Feet**: The size of the property. <br> <br>
4) **Materials e.g. Foundation, Roof** : The materials used to construct the property <br> <br>

Surprisingly, the age of the property did not influence the sale price as much as we initially assumed. It was zeroed out by lasso.

To ensure that future homeowners purchase property that is value for money, we would recommend them to consider these 4 factors before making a purchase. 
