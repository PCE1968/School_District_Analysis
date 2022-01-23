# School_District_Analysis
## Overview
The school board has determined that there was a problem with some of the test schools from Thomas High School. Maria would like to understand the impact this has on the original school district summary.

## Purpose
The purpose of this analysis is to gage the impact of the scores for the ninth grade students at Thomas High School. This will be done by removing the scores for all ninth graders at Thomas High School, repeating the district calculations and comparing the outcomes.

## Results
To understand any changes we must first consider the orignal analysis. Here is the original summary for Thomas High School:

![Thomas High School, Original summary](Resources/Original_Thomas_summary.png)

Now that we know our starting point, let's address the Ninth grade scores at Thomas High School. To do this we will replace all of the Ninth grade scores with NaN, so their values no longer effect Thomas High Schools score averages and percentages. To do this we will employ the np.nan function from the numpy library.

We can see that we've done this correctly when we look at the student data output and see the ninth grade scores for Thomas High School students now report as NaN.

![Thomas High School, ninth grade scores replaced with NaN](Resources/Replace_Thomas9_With_Nan.png)

Having replaced the ninth grade scores with NaN, we can compare the updated Thoms High School summary to the original summary.

Original Thomas High summary:
![Thomas High School, Original summary](Resources/Original_Thomas_summary.png)

Updated summary after replacing ninth grade scores:
![Thomas High School, updated summary with NaN](Resources/Thomas_summary_with_Nans.png)




