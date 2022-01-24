# School_District_Analysis
## Overview
The school board has determined that there was a problem with some of the test schools from Thomas High School. Maria would like to understand the impact this has on the original school district summary.

## Purpose
The purpose of this analysis is to gage the impact of the scores for the ninth grade students at Thomas High School. This will be done by removing the scores for all ninth graders at Thomas High School, repeating the district calculations and comparing the outcomes.

## Analysis

### Starting Point
To understand any changes we must first consider the orignal analysis. Here is the original summary for Thomas High School:

![Thomas High School, Original summary](Resources/Original_Thomas_summary.png)

### Updating the Thomas High School ninth grade scores
Now that we know our starting point, let's address the Ninth grade scores at Thomas High School. To do this we will replace all of the Ninth grade scores with NaN, so their values no longer effect Thomas High Schools score averages and percentages. To do this we will employ the np.nan function from the numpy library.

#### Replace Thomas High School ninth grade scores with NaN
We can see that we've done this correctly when we look at the student data output and see the ninth grade scores for Thomas High School students now report as NaN.

![Thomas High School, ninth grade scores replaced with NaN](Resources/Replace_Thomas9_With_Nan.png)

Having replaced the ninth grade scores with NaN, we can compare the updated Thoms High School summary to the original summary.

Original Thomas High School summary:

![Thomas High School, Original summary](Resources/Original_Thomas_summary.png)

Updated summary after replacing ninth grade scores:

![Thomas High School, updated summary with NaN](Resources/Thomas_summary_with_Nans.png)

Since changing the scores doesn't change the number of students, first five columns are identical. When we get to the scores we can see the impact.
- Average Math Score has drop slightly
- Average Reading Score has gone up slightly
- % Passing Math, % Passing Reading and % Overall Passing have all dropped significantly

The current updated summary no longer has the scores for the ninth grade students, effectively setting their scores to zero, which is significantly skewing the percentages.

#### Normalizing the Thomas High School scores
We must account for the lack of scores for the Thomas High School ninth grade students, by not considering them when calculating the Thomas High School score averages and percentages.

Now we can compare the resulting Thomas High School summary to the original.

Original Thomas High School summary:

![Thomas High School, Original summary](Resources/Original_Thomas_summary.png)

Normalized Thomas High School summary:

![Thomas High School, Normalized summary](Resources/Normalized_Thomas_summary.png)

The Average Math Score is still slightly lower and the Average Reading Score is still slightly higher, but now:
- % Passing Math is only slightly lower
- % Passing Reading is also only slightly lower
- leading to an % Overall Passing this is only slightly lower

### Impact on Top Schools list
Thomas High School was originally second on the list of top schools as illustrated below.

![Original Top School list](Resources/Original_TopSchools.png)

Looking at the updated Top School list we see that Thomas High School has a slightly lower % Overall Passing score, but not low enough to move them from their position on the list, as illustrated below.

![District summary after Thoms High School ninth grade score adjust,emt](Resources/Thomas9NaN_TopSchools.png)

### Impact on Scores by school spending

Thomas High School is in the $630-644 per student range. Here is a look at the original summary and the updated summary.

#### Original Scores by school spending summary
![Original Scores by school spending summary](Resources/Original_scores_by_spending.png)

#### Updated Scores by school spending
![Updated Scores by school spending](ths9_scores_by_spending.png)

These are virtually identical. To see any impact you would have to go out to the hundereths digit, which is insignificant to these calculations.

### Impact on Scores by school size

Thomas High School has an enrollment of 1635 students. Any impact would be observed in the Medium(1000-2000) range scores. Here is a look a the original summary and the updated summary.

#### Original Scores by school size summary
![Original Scores by school size summary](Resources/Original_scores_by_size.png)

#### Updated Scores by school size summary
![Updated Scores by school size summary](Resources/ths9_scores_by_size.png)

Again, these are virtually identical. To see any impact you would have to go out to the hundereths digit, which is insignificant to these calculations.

### Impact on Scores by Type

Thomas High School is a charter school. Any impact would effect the Charter scores. Here is a look a the original summary and the updated summary.

#### Original Scores by school type summary
![Original Scores by school type summary](Resources/Original_scores_by_type.png)

#### Updated Scores by school type summary
![Updated Scores by school type summary](Resources/ths9_scores_by_type.png)

Again, these are virtually identical. To see any impact you would have to go out to the hundereths digit, which is insignificant to these calculations.

## Summary
