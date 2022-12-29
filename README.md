# MechaCar_Statistical_Analysis
## Overview of Project

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, I am helping Jeremy and the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, I am to  write a summary interpretation of the findings.

# Deliverable 1:
## Linear Regression to Predict MPG
### Results

![image](https://github.com/ras52017/MechaCar_Statistical_Analysis/blob/main/Images/linear%20regression%20model..jpg)

## MPG = (6.267) vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)

#### Summary

- Both vehicle ground and vehicle length are statistically reasonable to deliver non random amounts of variance to this model. The vehicle ground clearance and vehicle length have a great impact on Miles Per Gallon (MPG) on the MechaCar prototype. On the other hand, the spoiler angle , All-Wheel Drive (AWD) and vehicle weight all have p-Values that indicates a random amount of variance in the dataset.

- The p-Value for this model, p-Value: 5.35e-11, is much small when compared with the assumed significance level of 0.05%. There is therefore sufficient evidence to reject our null hypothesis, which suggest that the slope of this linear model is not zero.

- The regression model's r squared value  of 0.7149. Thia indicates approximately 71% of all MPG predictions will be determined by this model.


# Deliverable 2:
## Summary Statistics on Suspension Coils
### Overview
The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using your knowledge of R, you’ll create a summary statistics table to show:

- The suspension coil’s PSI continuous variable across all manufacturing lots.

- The following PSI metrics for each lot: mean, median, variance, and standard deviation.

### Results

### Total Summary

![image](https://github.com/ras52017/MechaCar_Statistical_Analysis/blob/main/Images/total_summary.jpg)

### Lot Summary

![image](https://github.com/ras52017/MechaCar_Statistical_Analysis/blob/main/Images/lot_summary.jpg)


### Summary

- The whole population dataset of the production lot shows a variance of the coils as 62.3 PSI and this is within the 100 PSI variace requirement.
- Lot 1 and 2 also show a variance of approximately 1 and 7.5 PSI respectively. These lots are within the 100 PSI  variance requirement. However, Lot 3 shows a larger variance of 170.29 which is greater than the PSI requirement.

![image](https://github.com/ras52017/MechaCar_Statistical_Analysis/blob/main/Images/PSI%20each%20indicdiual%20Lot.jpg)


# Deliverable 3:
## T-Tests on Suspension Coils
### Overview

Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

Follow the instructions below to complete Part 3.

Technical Analysis
- In your MechaCarChallenge.RScript, write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.

- Next, write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.
- 
    - An RScript is written for t-test that compares all manufacturing lots against mean PSI of the population
    - An RScript is written for three t-test that compares each manufacturing lots against mean PSI of the population
    - There is a summary of the t-test results across all manufacturing lots and for each lot
    
The next step is to conduct a t-test on the suspension coil data to determine whether there is a statistical difference between the mean of this provided sample dataset and a hypothesized, potential population dataset. Using the presumed population mean of 1500, we find the following:

 
> t.test(lot1$PSI,mu=1500)

	One Sample t-test

data:  lot1$PSI
t = 0, df = 49, p-value = 1
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.719 1500.281
sample estimates:
mean of x 
     1500 

> t.test(lot2$PSI,mu=1500)

	One Sample t-test

data:  lot2$PSI
t = 0.51745, df = 49, p-value = 0.6072
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.423 1500.977
sample estimates:
mean of x 
   1500.2 

> t.test(lot3$PSI,mu=1500)

	One Sample t-test

data:  lot3$PSI
t = -2.0916, df = 49, p-value = 0.04168
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1492.431 1499.849
sample estimates:
mean of x 
  1496.14 

### Summary

#### One Sample t-test
From the one sample t-test above, the true mean of the sample was 1498.78. It showed a p-Value of 0.06, higher than the common significance level of 0.05. There is NOT sufficient evidence to support rejecting the null hypothesis. This implies the mean of all three of these manufacturing lots is statistically comparable or similar to the presumed population mean of 1500.

#### Lot 1 t-test
Lot 1 generated a true sample mean of 1500. With a p-Value of 1, the null hypothesis cannot be rejected. There is no statistical difference between the observed sample mean and the presumed population mean (1500).

A sample mean of 1496.14 with a p-Value of 0.04. The p-Value is lower than the common significance level of 0.05. The null hypothesis must be rejected implying this sample mean and the presumed population mean are not statistically different. Lot 3 obviously had an abnormal situation in the manufacturing/production process that accounted for the results obtained.


# Deliverable 4:
## Study Design: MechaCar vs Competition
### Overview

#### Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

• A statistical test to test the hypothesis
• A metric to be tested 
• A null hypothesis or an alternative hypothesis 


### Results

#### Statistical Tests
A multiple linear regression. This can establish the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price.

##### Data needed to run the statistical test will be:
##### Data on MechaCar and its comparable models across several different manufacturers over the last 3 years. Data will include:
• Comparable models from competitors.

• Cars that will be competing with MechaCar head-to-head.

• Factors that will determine the relevant selling price.

#### Metrics
The following metrics will be tested:
• Safety Feature Rating: Independent Variable

• MPG (Gasoline Efficiency): Independent Variable

• Current Price (Selling): Dependent Variable 

• Engine (Electric, Hybrid, Gasoline / Conventional): Independent Variable

• Drive Package : Independent Variable 

• Resale Value: Independent Variable 

• Average Annual Cost of ownership (Maintenance): Independent Variable 


#### Hypothesis: Null and Alternative
After determining which factors are key for the MechaCar's genre:

• Alternative Hypothesis: MechaCar is NOT priced correctly based on performance of key factors for its genre.

• Null Hypothesis: MechaCar is priced correctly based on its performance of key factors for its genre.





    
