# MechaCar_Statistical_Analysis
## Overview of Project

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, I am helping Jeremy and the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, I am to  write a summary interpretation of the findings.

# Deliverable 1;
## Linear Regression to Predict MPG
### Results

![image](https://github.com/ras52017/MechaCar_Statistical_Analysis/blob/main/Images/linear%20regression%20model..jpg)

## MPG = (6.267) vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)

#### Summary

- Both vehicle ground and vehicle length are statistically reasonable to deliver non random amounts of variance to this model. The vehicle ground clearance and vehicle length have a great impact on Miles Per Gallon (MPG) on the MechaCar prototype. On the other hand, the spoiler angle , All-Wheel Drive (AWD) and vehicle weight all have p-Values that indicates a random amount of variance in the dataset.

- The p-Value for this model, p-Value: 5.35e-11, is much small when compared with the assumed significance level of 0.05%. There is therefore sufficient evidence to reject our null hypothesis, which suggest that the slope of this linear model is not zero.

- The regression model's r squared value  of 0.7149. Thia indicates approximately 71% of all MPG predictions will be determined by this model.

