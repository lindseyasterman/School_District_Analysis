# School_District_Analysis

### Overview 
Due to the possiblity of corrupted or fraudulent data, we have been asked to create a new analysis for the school district. It appears that reading and math scores have been altered for Thomas High School 9th graders. We will replace this bad data with NaNs and compare to the original analysis.  

### Results
- District Summary: 
    The District Summary showed a 0.1% decrease in the overall passing percentage
- School Summary:
    The School Summary showed a 0.3% decrease in the overall passing percentage of Thomas High School if we are only looking at grades 10-12. If we are considering a grade of "0" for ninth graders due to fraudulent grades the passing percentages fall dramatically.
    !images - updated thomas with nans vs. only 10th-12th
- Thomas High School's performance relative to other schools:
    While removing the 9th graders very slighlty lowered math and reading scores for Thomas High School, they remained the number two performing school in the district. If we are including the 9th graders, Thomas High School overall passing % drops to 65% which would place it in the bottom half of schools.
- Math and Reading scores by grade:
    Only Thomas High school is affected.
    !image reading score by grade with nans
- Scores by school spending:
    Scores by school spending are unaffected when using the updated summary.  What is concering is the inverse relationship between spending and scores and further analysis should be preformed to determine probable causes.
    !images school spending summary
- Scores by school size:
    This metric was unaffected with the updated summary as well, but it does show quite conclusively that the largest schools are struggling with the passing percentage.
    !images school size summary
- Scores by school type:
    Once again this metric is unaffected once updated. And again, it shows an alarming descrepancy between school type with charter schools having a much higher passing percentage than district schools.

### Summary

Changes in the updated analysis include:
1. The overall district summary shows insignificant differences between analysis.
2. Thomas High School's overall performance is greatly decreased when the 9th grade population is included but scores are NaN. Conversley, using only the 10th - 12th grade has little effect on the schools total performance. 
3. The district average of 9th grade math and reading scores decreases when removing Thomas High School. By using the following code and refactoring for math,
```
reading_mean_9th = reading_scores_by_grade["9th"].astype(float).mean()
reading_mean_9th

```  
I determined the average reading score of 9th graders dropped from 82.5 to 82.4 and the average math score dropped from 80.4 to 80.1.
4. More concerning areas that require further analysis are the dicrepancies between performance when looking at school spending, school size, and school type.



