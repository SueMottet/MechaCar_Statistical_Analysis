# MechaCar Statistical Analysis

Statistical analysis was performed on MechaCar production data for insights to the MechaCare management that may help the manufacturing team

## Resources: RScript, RStudio, RMarkdown, .csv data files of car data. 

Some population and specifications data was provide separately:
* The specifications from the MechaCare suspension coils indicated that the variance of the suspension coils must not exceed 100 pounds per square inch
* The population mean psi = 1500

## MechaCar Statistical Analysis Overview

1. Linear Regression to Predict MPG - Multiple linear regression analysis has been performed to identify which variables in the dataset predict the mpg of MechaCar prototypes.

2. Summary Statistics on Suspension Coils - Summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots has been collected.

3. T-Test on Suspension Coils - T-tests have been run to determine if the manufacturing lots are statistically different from the mean population.

4. Design a Study Comparing the MechaCar to the Competition - A statistical study has been designed and performed to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. 


## MechaCar Statistical Analysis Results

For each statistical analysis a summary interpretation of the findings is provided in the results section.

## Linear Regression to Predict MPG Results Summary:

The mpg linear regression:
![mpg linear reg image](/resources/linear_reg.png)


The mpg linear regression summary:
![mpg linear reg image](/resources/linear_reg_summary.png)

* Vehicle weight, vehicle height, ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the mpg values in the dataset. 
* The slope of the linear model is not considered to be zero because the p-value of the linear model was much smaller than the significance level which provides sufficient statistical evidence that the null hypothesis is not true.
* The R-square value is 0.7149 which means there is a 71.5% chance that future data points will fit the model. This means the linear model does predict the mpg of the prototypes effectively.

## Summary Statistics on Suspension Coils

The specifications from the MechaCare suspension coils indicated that the variance of the suspension coils must not exceed 100 pounds per square inch.

Two data frames were created with summary statistics on the suspension coil psi across all manufactoring lots and then for each lot to analyze the variance manufacturing lots for this design specification.
 
The total summary table for psi:

![total summary stat image](/resources/total_summary_psi.png)

* The analyzed manufacturing data indicates the design is meeting this design specification for all the manufacturing lots in total.

The lot summary table for psi:

![lot summary stat image](/resources/lot_summary_psi.png)

* The variance of the suspension coils in Lot 1 and Lot 2 also do not exceed 100 pounds per square inch and indicate that the suspension coils in these lots meet this design specification.
* Lot 3 has a variance which exceeds the 100 pounds per square inch design specification. 

## T-Test on Suspension Coils

T-test were performed to determine if all manufactuirng lot and each lot independently were different from the population:

* The null hypothesis was that there is no statistical difference 
* The alternate hypothesis was that there is a statistical difference.

With t-tests:
* A p-value is a measure of the probability that a difference could have occurred by random chance.
* The lower the p-value, the greater the statistical significance of the difference.

The population mean compared against was 1,500 pounds per square inch.

### All manufacturing lots t- test:

A t-test was performed on the MechaCar manufacturing lots to determine if all the manufacturing lots were statistically different from the population mean of 1,500 pounds per square inch.

The t-test results for all manufacturing lots:

![t test summary image](/resources/t_test_all_2_pop.png)

With a p-value of .06, the psi mean for all lots is not statistically different from the population mean of 1,500 psi and indicates that there is not enough statistical evidence to reject the null hypothesis. 

### Lot t-tests: 
A t-test was also performed on each lot individually to determine if each lot was statistically different than the population mean.

The t-test results for lot 1:
	
![t test lot 1 image](/resources/t_test_lot1_2_pop.png)

With a p-value of .46, the mean psi for lot 1 is not statistically different from the population mean of 1,500 psi and indicates that there is not enough statistical evidence to reject the null hypothesis for the lot.


The t-test results for lot 2:
	
![t test lot 2 image](/resources/t_test_lot2_2_pop.png)

With a p-value of .94, the mean psi for lot 2 is not statistically different from the population mean of 1,500 psi and indicates that there is not enough statistical evidence to reject the null hypothesis for the lot.

The t-test results for lot 3:
	
![t test lot 3 image](/resources/t_test_lot3_2_pop.png)

With a p-value of .03, the mean psi for lot 3 is statistically different from the population mean of 1,500 psi and indicates that there is enough statistical evidence to reject the null hypothesis for the lot.

## MechaCar Statistical Analysis Summary

## Study Design: MechaCar vs Competition
MechaCar could perform an ANOVA test to compare the MechaCar to its competition: cost, city and highway fuel efficiency, horse power, safety rating, maintenance cost.

An ANOVA test tests whether the means from multiple samples are significantly similar or different. 

This test could be used to compare the averages of different cars in the categories to the MecaCar category averages. 

* If the resulting p-value is greater than 0.05, then MecaCar has the same or similar performance within the categories (the null hypothesis). 

* If the resulting p value is less than 0.05, then MecaCar is significantly different within the categories. 

* If the test shows a significant difference, then looking at the average of the MecaCar is the next step. If MecaCar's average is either below or above the other averages, the analysis could indicate how it is performing against the competitors.

