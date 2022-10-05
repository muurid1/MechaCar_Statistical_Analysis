# MechaCar_Statistical_Analysis

Demo of R and its statistical capabilities

### The objective of this challenge is to use R in order to design and interpret a multiple linear regression analysis, calculate summary statistics and t-tests, and provide an interpretation of the results. Finally, you'll design your own statistical study to compare vehicle performance of two vehicles of the MechaCar vehicles against vehicles from other manufacturers.
## Background

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

### Linear Regression to Predict MPG
  
Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.

  ! [Mecha Car Linear Model Summary](./Images/Mecha_Car_Linear_Model_Summary.png)

###### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

Each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model
Using the MechaCar_mpg dataset, vehicle_length and ground_clearance are statistically unlikely to provide random amounts of variance to the linear model. In other words the vehicle_length and ground_clearance have a significant impact on mpg.

###### Is the slope of the linear model considered to be zero? Why or why not?

The Intercept is Statistically Signficant (less than 0.05) and not zero.
This would indicate that the intercept term explains a significant amount of variability in the dependent variable when all independent variabes are equal to zero. It could mean that the significant features (such as vehicle_weight and ground_clearance) may need scaling or transforming to help improve the predictive power of the model; ot there are other variables that can help explain the variability of our dependent variable (mpg) that have not ben included in our model.

###### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The multiple R-squared value is 0.71 (while the p-value remained significant (very small) indicating the model does an adequate job of predicting mpog.

### Summary Statistics on Suspension Coils

Collect  summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots

 ! [Coil PSI variance for all lots](./Images/Coil_PSI_variance_for_all_lots.png)

###### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

1- In total the specifications for the MechaCar are met with variance of 62.29

2- By lots, Lots 1 and 2 are within specifications; however lot 3 has a variance that exceeds specifications.

! [Coil PSI variance by lots](./Images/Coil_PSI_variance_by_lots.png)

### T-Test on Suspension Coils

<- Lot 1 is NOT signicantly different from the population mean (with a p-value of 1)

! [Lot 1 t.test](./Images/Lot1_t.test.png)

<- Lot 2 is NOT signicantly different from the population mean (with a p-value of .6072)

! [Lot 2 t.test](./Images/Lot2_t.test.png)

<- Lot 3 is signicantly different from the population mean (with a p-value of .04168)

! [Lot 3 t.test](./Images/Lot3_t.test.png)

Run t-tests to determine if the manufacturing lots are statistically different  from the mean population

### Design a Study Comparing the MechaCar to the Competition
Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you will write a summary interpretation of the findings
