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

2. The p-value of this model [p-value: 5.35e-11] is far less than the 0.05% significance level, indicating: a) there is sufficient evidence to reject the null hypothesis; and b) the slope of the model is not zero.

3. This linear model has an r-squared value of 0.7149, indicating that 71.5% of the variation in the output variable is explained by the input variables. Therefore this model *does* predict the mpg of MechaCar prototypes effectively.

## Deliverable 2: Summary Statistics on Suspension Coils

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using my knowledge of R, I created 2 summary statistics tables:

1. Suspension coil metrics across all manufacturing lots:

![Del 2 total_summary](https://user-images.githubusercontent.com/97558998/171692197-addc7239-3430-49ac-9f11-bcfc1cd57352.png)

2. Metrics for each individual lot:

![Del 2 lot_summary](https://user-images.githubusercontent.com/97558998/171692049-0db8b950-973f-4e60-aba7-bb974d583d41.png)

### Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. The current manufacturing lots overall meet this design specification in that the PSI variance (in total) is 62.29 PSI, well below the design standard of 100 pounds per square inch.

However, the variance is substantially different among the 3 lots when analyzed individually. Lot 1 and Lot 2's variance (0.989 and 7.47 respectively) both meet design specs. Lot 3's variance is significantly out of spec range at 170.29 PSI, skewing the total dataset.

## Deliverable 3: T-Test on Suspension Coils

In your MechaCarChallenge.RScript, write an RScript using the t.test() function to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.

Next, write three more RScripts in your MechaCarChallenge.RScript using the t.test() function and its subset() argument to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

### T-Tests on Suspension Coils

Briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.

## Deliverable 4: Design a Study Comparing the MechaCar to the Competition

design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

### Study Design: MechaCar vs Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

In your description, address the following questions:

What metric or metrics are you going to test?

What is the null hypothesis or alternative hypothesis?

What statistical test would you use to test the hypothesis? And why?

What data is needed to run the statistical test?
