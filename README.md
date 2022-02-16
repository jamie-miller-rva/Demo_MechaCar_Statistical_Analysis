# Demo_MechaCar_Statistical_Analysis
Demo of R and its statistical test capabilities

## Background
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

1. Deliverable 1: Linear Regression to Predict MPG:
    Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes

    ![Mecha Car Linear Model Summary](./Images/Mecha_lm_summary.png)

    - Q1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    - Methodology: Each Pr(>|t|) value in the summary (above) represents the probability that each coefficient contributes a random amount of variance to the linear model. 
    - A1. Using the MechaCar_mpg dataset, vehcicle_length and ground_clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model. In other words the **vehcicle_length and ground_clearance have a significant impact on mpg**.  

    - Q2. Is the slope of the linear model considered to be zero? Why or why not?
      - Methodology: Examine the Pr(>|t|) value in the summary above for the (Intercept).
      - - A2. **The intercept is statistically significant** (less than the 0.05) **and not zero**. This would indicate that the intercept term explains a significant amount of variability in the dependent variable when all independent variables are equal to zero. It could mean that the significant features (such as vehcicle_weight and ground_clearance) may need scaling or transforming to help improve the predictive power of the model; or there are other variables that can help explain the variability of our dependent variable (mpg) that have not been included in our model.

    - Q3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
        - Methodology: Examine the Multiple R-squared value to indicate how well the regression model approximates real-world data points. In most cases, the value will range between 0 and 1 and can be used as a probability metric to determine the likelihood that future data points will fit the model.
    - A3: The **Multiple R-squared value is 0.71** (while the p-value remained significant (very small) **indicating the model does an adequate job of predicting mpg**.

2. Deliverable 2: Summary Statistics on Suspension Coils
    Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots

    ![Coil PSI variance for all lots](./Images/Coil_Variance_All.png)

    ![Coil PSI Variance by Lots](./Images/Coil_Variance_by_Lots.png)

    Q1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
    - Methodology: Examine the mean, median and variance in total (total_summary) and for each lot (lot_summary) to determine if the variance is within the 100 pounds per square inch.
    - A1: **In total the specification are met with variance of 62.29 (less than 100)**. 
    - A2: **By Lots, Lots 1 & 2 are within specifications; however Lot 3 has a variance that exceeds specifications (100 PSI)**.

3. Deliverable 3: T-Test on Suspension Coils
    Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
    



4. Deliverable 4: Design a Study Comparing the MechaCar to the Competition
    Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.