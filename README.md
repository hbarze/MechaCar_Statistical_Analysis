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

## Deliverable 2- Create Visualizations for the Trip Analysis

### Summary Statistics on Suspension Coils:

The Suspension Coil csv dataset contains the results of testing the weight capacities of different suspension coils from multiple production lots.

Summary statistics for all production lots put together: 
<img width="381" alt="Screen Shot 2022-03-30 at 9 22 06 AM" src="https://user-images.githubusercontent.com/96043107/160875304-7d48a5ae-58fe-4852-9ca2-5dd8cd73f896.png">


Summary statistics for each of the three production lots: 
<img width="502" alt="Screen Shot 2022-03-30 at 9 22 41 AM" src="https://user-images.githubusercontent.com/96043107/160875334-ca38b881-dfe2-45dc-875b-1b0cc86e67b9.png">

### Q1: The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. For all the lots combined and for each lot individually, does the current manufacturing data meet this design specification?

In the summary statistics chart for the combined production lots, there is a total variance in the PSI (Pounds per squsre inch) of 62.29, which is within the 100 PSI variance requrement. For each individual lot, in the summary statistics chart for the three lots the variance for lot 1 and 2 are within the 100 PSI variance requirement. Lot 1 has a variance of 0.98, and lot 2 has a variance of 7.47. However, lot 3 fails to meet the 100 PSI variance requrement, as the variance is 170. Lot 3 is causing the combined production lot variance figure to be much higher than it would be if it were just lot 1 and 2. 

## Deliverable 3- T-Tests on Suspension Coils
In order to determine if there is a statistical difference between the mean of this dataset and our hypothesis (using a presumed population mean of 1500), conducting a t-test is necessary. 

T-Test Summary of results across all manufacturing lots: 
<img width="408" alt="Screen Shot 2022-03-30 at 11 29 39 AM" src="https://user-images.githubusercontent.com/96043107/160896532-55d77237-c47a-4963-8ec5-ae3d6188f3dd.png">

Here we find that the true mean of the sample is 1498.78, also shown in the above summary statistics for all combined production lots. Since the p-value, 0.06028, is above the standard significance level of 0.05, we are unable to reject the null hypothesis. Therefore, the mean of the three combined lots is statistially speaking similar to the presumed population mean of 1500. 

T-Test Summary of results from Lots 1, 2, and 3:
<img width="419" alt="Screen Shot 2022-03-30 at 11 30 15 AM" src="https://user-images.githubusercontent.com/96043107/160897190-98e4988a-05e0-4e1b-85e3-d79126abb77b.png">

Assessing the p-values of the t-tests for each individual lot:
Lot 1- Lot 1's sample has a true sample mean of 1500, which means that its sample mean is equal to the presumed population mean, giving it a **p-value of 1**. Due to this, we are **unable** to reject the null hypothesis that there is no statistical difference between the observed and presumed sample means. 

Lot 2- Lot 2's sample has a very similar result to lot 1, where the sample mean is 1500.2. This sample mean results in a **p-value of 0.6072**, well above the standard significance level of 0.05. Therefore, we are again **unable** to reject the null hypothesis that there is no statistical difference between the observed and presumed sample means. 

Lot 3- Lot 3's sample has a true sample mean of 1496.14, resulting in a **p-value of 0.04168**. Due to Lot 3's p-value being below the standard significance level of 0.05, we **are able** to reject our null hypothesis that ther is no statistical difference between the observed and presumed sample mean. 

After our t-test statistical analysis, we can confirm that something in Lot 3's production process is awry, and that process needs to be reassessed for suspension coils not meeting quality standards. 

## Deliverable 4- Study Design: MechaCar vs. Coompetition:

####Q1. Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

In order to quantify how the MechaCar performs against the competition, I would create the following independent variables: Average MPG, Saftey Feature Rating, Horse Power, and Annual Maintenance Costs. My dependent variable would be the current selling price of the vehicle. 


####Q2. In your description, address the following questions:
What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?
What statistical test would you use to test the hypothesis? And why?
What data is needed to run the statistical test?

**Metrics**
* Average Miles Per Gallon (MPG) **Independent Variable**
* Saftey Feature Rating **Independent Variable**
* Horse Power **Independent Variable**
* Annual Maintenance Costs **Independent Variable**
* Current Selling Price (USD) **Dependent Variable**

**Null and Alternative Hypothesis**
* Null Hypothesis (Ho): MechaCar is correctly priced based upon key industry vehicle features.
* Alternative Hypothesis (Ha): MechaCar is incorrectly priced based upon key industry vehicle features. 

**Statistical Test of Choice**
In order to determine which independent variables have the highest correlation with our dependent variable (Current Selling Price), I would use a multiple linerar regression model. We can combine all independent variables, or only use a few to determine which ones have the largest impact on the current selling price of the vehicle. 

**Data Collection**
Data from a similar category of cars as the MechaCar would need to be collected in the following categories: Fuel efficiency (MPG), Saftey Feature Ratings, Horse Power, Maintenance Costs (on an Annual basis), and the Current Selling Price (USD). It would be best to include as many vehicles that are similar to the MechaCar as possible, and therefore any foreign cars' data may have to be converted to USD for its selling price and annual maintenance costs, and from kilometers/liter to Miles/Gallon. 



