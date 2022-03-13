# SAS-Example-for-Detecting-Problems-with-Regression
SAS program for detecting extreme observations and multicollinearity will be shown using an example with measurements of weights, heart girths, wither heights and rump heights of 10 young bulls
# Output explanation
The first table is the analysis of variance table. The next table is Parameter Estimates, in which the Parameter Estimate, Standard Error, t Value, P value (Pr > |t|), 
sequential sums of squares (Type I SS), partial sums of squares (Type II SS), degrees of freedom (DF) and VIF statistics (Variance Inflation) are given. For ht_w and ht_r VIF
values are greater than 10. The VIF for these variables indicates that both are not necessary in the model. There is collinearity between them. In the next table, Output statistics, for detection of extreme observations are shown. Listed are: the dependent variable (Dep Var), Predicted Value, standard error of prediction (Std Error Mean Predict), Residual, standard error of residual (Std Error Residual), studentized residuals (Student Residual), simple graphical presentations of deviations of observations from the estimated values (-2 -1 0 1 2), Cook’s distance (Cook’s D), studentized residuals estimated using s-i = MSRES not including observation i (Rstudent), h value (Hat Diag H), CovRatio, DFFITS and DFBETAS. 
SAS leaves to the researcher the decision of which observations are extreme and 
influential. For this example p = 4 and n = 10, and the calculated critical values are: 

hii ≥ 2np = 0.8 

| DFITTSi |≥ 2 n/p = 1.26

| DFBETASi |≥ 2/n = 0.63

Cook’s Di > 1 

COVRATIOi < 1− 3np = −0.2 or 

COVRATIOi > 1+ 3np = 2.2

The values in the SAS output can be compared with the computed criteria. In this output observations having exceeded the criteria are emphasized with bold letters. The studentized 
residual was greater than 2 for observation 7. No hii was greater than 0.8, that is, no high leverage was detected. The Cook’s D exceeded 1 for observation 7. The covariance ratios of observations, 1, 3, 5, 6, 9 and 10 exceeded the critical criteria which also can raise questions about the validity of the chosen model. The DFFITS for observations 2, 4 and 7 exceed the criteria. The DFBETAS exceeded the critical values for observations 2, 4 and 7. Obviously, observation 7 is an influential outlier and it should be considered for removal.
