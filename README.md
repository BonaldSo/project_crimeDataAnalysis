# project_crimeDataAnalysis

The variates for UScrime05 are 
• state or district abbreviated as two letters, 
• violent crime rate (number of violent crimes per 100,000 population), 
• murder rate (number of murders per 100,000 population),
• metro, being the percent of the population residing in a metropolitan areas,
• white, being the percent of the population that is white,
• HS, being the percent of the population who have graduated from high school, and
• poverty, being the percent of the population that is below the poverty level.

We begin with an exploration between the murder rate and the violent crime rate. With murder as the response variate and violent as the explanatory variate, 
fit a straight line model and assign the fitted model to the R variable fit1.
We can see significant difference between violent and murder. 
The residuals are not normally distributed after qqtest.
The assumption of homoscedasticity does not hold.
There is a decresing trend of simple estimated residual when fitted value increases.
The diagonal values of hat matrix (hii) and conclude that District of Columbia has the greatest potential to affect the fitted model.

Next, we use the logarithm of murder as the response and the logarithm of violent crime as the explanatory
variate. Again, fit a straight line model to these transformed variates and this time assign the fitted
model to the R variable fit2.
We can see the model fits the data better. 
The residuals are normally distributed after qqtest.
The assumption of homoscedasticity holds.
There is no decresing trend of simple estimated residual when fitted value increase.
The potential influence of District of Columbia has decreased after applying log transformation.

Therefore, after studying two models, we conclude that we should choose to do a log transformation for the data because it follows 
our assumptions better.

Finally, we turn to a model of the logarithm of the violent crime rate as a simple sum of
explanatory variates metro, white, HS, and poverty, and fit this model and assign the result to fit3.
Both metro and poverty are having p-value less than 0.5, showing that they are significant factors of log(violent).
The assumption of heteroscedasticity holds.
The residuals are normally distributed.
District of Columbia(51) and Hawaii(11) have the potinetial for influence the fit.
Hawaii had an actual influence on the fitted coefficient as its Cook Distance is greater than 2.

Conclusion of findings: From the plots, we can see that most data follow the linear trend for metro and white, so these two variables should be considered. 
But data does not show any additional information for the prediction fo log(violent) for HS and poverty since data does not follow the linear trend in general, 
which is as expected. In addition, Hawaii and North Dakota are labelled in all of the plots, indicating that these two states are the influential points since 
they have influence to the variables we include in the model.



