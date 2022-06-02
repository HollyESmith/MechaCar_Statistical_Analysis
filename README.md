# MechaCar_Statistical_Analysis

## Deliverable 1: Linear Regression to Predict MPG

## Linear Regression to Predict MPG

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using my knowledge of R, I designed a linear model to predict the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file. 

---

Linear regression model results:

![Del 1 Step 5](https://user-images.githubusercontent.com/97558998/171662208-1225ab9f-ff11-490d-81fc-fd4c2441ac8c.png)

---

P-value and r-squared values:

![Del 1 Step 6](https://user-images.githubusercontent.com/97558998/171662360-9019856a-e5fa-4600-8914-d5cf515c4fe6.png)

---

From the above, we can determine:

1. **Vehicle length** and **ground clearance** provide a non-random amount of variance on miles per gallon (mpg). The other variables, *vehicle weight, spoiler angle,* and *all wheel drive* have p-values that indicate random variance.

2. The p-value of this model [p-value = 5.35e-11] is far less than the 0.05% significance level, indicating: a) there is sufficient evidence to reject the null hypothesis; and b) the slope of the linear regression model is not zero.

3. This linear model has an r-squared value of 0.7149, indicating that 71.5% of the variation in the output variable is explained by the input variables. Therefore this model *does* predict the mpg of MechaCar prototypes effectively.

## Deliverable 2: Create Visualizations for the Trip Analysis

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using my knowledge of R, I created 2 summary statistics tables:

1. Suspension coil PSI metrics across all manufacturing lots:

![Del 2 total_summary](https://user-images.githubusercontent.com/97558998/171692197-addc7239-3430-49ac-9f11-bcfc1cd57352.png)

2. Suspension coil PSI metrics for each individual lot:

![Del 2 lot_summary](https://user-images.githubusercontent.com/97558998/171692049-0db8b950-973f-4e60-aba7-bb974d583d41.png)

### Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. The current manufacturing lots overall meet this design specification in that the PSI variance (in total) is 62.29 PSI, well below the design standard of 100 pounds per square inch.

However, the variance is substantially different among the 3 lots when analyzed individually. Lot 1 and Lot 2's variance (0.989 and 7.47 respectively) both meet design specs. Lot 3's variance is significantly out of spec range at 170.29 PSI, skewing the total dataset.

## Deliverable 3: T-Test on Suspension Coils

Using the t.test() function I determined whether the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch:

![Del 3 Step 1](https://user-images.githubusercontent.com/97558998/171697224-a2cffa44-b289-45d3-ac3b-5e69fd2840fa.png)

Next, I wrote three more RScripts using the t.test() function and its subset() argument to determine whether the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch:

Manufacturing Lot 1:

![Del 3 Step 2 Lot 1](https://user-images.githubusercontent.com/97558998/171697244-1bc663e6-8146-4cc9-9347-944e53f94312.png)

Manufacturing Lot 2:

![Del 3 Step 2 Lot 2](https://user-images.githubusercontent.com/97558998/171697259-6e2cd572-7d55-498f-9433-33d16394929b.png)

Manufacturing Lot 3:

![Del 3 Step 2 Lot 3](https://user-images.githubusercontent.com/97558998/171697272-e2615cbe-a440-487b-8fbf-4305451c55e1.png)

### T-Tests on Suspension Coils

In the first t-test across all manufacturing lots, the p-value was 0.06028, higher than the significance level of 0.05, indicating that there is not enough evidence to reject the null hypothesis.

Results of the t-test for Lot 1 indicates that the p-value is not low enough (p-value = 1) to reject the null hypothesis.
Results of the t-test for Lot 2 indicates that the p-value is not low enough (p-value = 0.6072) to reject the null hypothesis.
Results of the t-test for Lot 3 indicates that the p-value is indeed low enough (p-value = 0.0417) to reject the null hypothesis.

## Deliverable 4: Design a Study Comparing the MechaCar to the Competition

Goal: design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

### Study Design: MechaCar vs Competition

In addition to data already analyzed, two key factors that influence a customer's choice of vehicle are reliability and safety ratings. 

Null Hypothesis (H<sub>0</sub>): MechaCar reliability and safety ratings are higher than the competition.<br>
Alternate Hypothesis (H<sub>a</sub>): MechaCar reliability and safety ratings are NOT higher than the competition.<br/>

The paired t-test will give us a p-value that will enable us to accept or reject the null hypotheses. T-tests will also demonstrate differences in means that will enable comparison of ratings of MechaCar with its competitors.

Data to be collected should be numerical and continuous, and normally distributed in a reasonably large sample size.
