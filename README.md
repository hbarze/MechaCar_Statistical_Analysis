# MechaCar_Statistical_Analysis
 Module 15: Using R and learning statistical tests


## Deliverable 1- Linear Regression to Predict MPG

Statistical Summary:
<img width="496" alt="Screen Shot 2022-03-29 at 11 56 45 PM" src="https://user-images.githubusercontent.com/96043107/160761348-c21d5de4-d88f-476d-92c6-e19a1d167231.png">


### Q1: Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
From the statistical summary above, we can see that vehicle_length and ground_clearance have a p-value with a significance level between 0 and 0.001 (indicated by the three asterisks), suggesting that those two variables provide a non-random amount of variance to the mpg values in the dataset. 

### Q2: Is the slope of the linear model considered to be zero? Why or why not?
The p-value of the overall model is **5.35e-11**, which is a figure well below the 0.05 significance level. With this in mind, we use this p-value as evidence to **reject our null hypothesis**. This indicates that the slope of the linear model is **not zero**. 

### Q3: Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
Using the goodness of fit, or R-squared, we can determine how well our linear regression model predicted the mpg of MechaCar prototypes. Our model has a multiple R-Squared value of 0.7149, and an Adjusted R-Squared value of 0.6825. These two figures indicate that our model's proportion of variance in the dependent variable (mpg) explained by our independent variables (vehicle_length, vehicle_weight, spoiler_angle, and ground_clearance) is moderate. An R-Squared value closer to 1 would indicate that our model predicts mpg more effectively, but this model's R-Squared value of around 0.70 is still acceptable. 
