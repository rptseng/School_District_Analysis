# School_District_Analysis
## Overview of Analysis
Using data from the district school board, we will use the pandas dependency in python to arrange "students_complete.csv" data into DataFrames and identify the top schools by the percentage of students with passing grades in reading and math. Additionally, because the grades for Thomas High School students in the ninth grade may be compromised through academic dishonesty, we will continue the analysis by replacing those grades with NULL values and excluding those students from the calculation on the total passing rate.

## Results
- District Summary
    - Prior to removing the grades of 461 ninth graders at Thomas High School, the district "% of Overall Passing" was at 65%.
    ![district_summary_all](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/district_summary_all.PNG)
    - After removing the grades of 461 ninth graders at Thomas High School from the data frame, the district "% of Overall Passing" is at 64.9%.
    ![district_summary_ex_ths](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/district_summary_ex_ths.PNG)
- School Summary
    - Prior to removing the grades of 461 ninth graders at Thomas High School, the "% of Overall Passing" was at 90.95%.
    ![school_summary_all](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/school_summary_all.PNG)
    - After removing the grades of 461 ninth graders at Thomas High School from the data frame, the "% of Overall Passing" is at 90.63%.
    ![school_summary_ex_ths](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/school_summary_ex_ths.PNG)
- Effect on Top Schools Rank
    - Prior to removing the grades of 461 ninth graders at Thomas High School, the "% of Overall Passing" ranks second in the district with a value of 90.95%.
    ![school_sort_all](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/school_sort_all.PNG)
    - After removing the grades of 461 ninth graders at Thomas High School from the data frame, the "% of Overall Passing" still ranks second in the district with a value of 90.63%. Removing the grades of these students did not impact its position on the list of top schools.

    ![school_sort_ex_ths](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/school_sort_ex_ths.PNG)

- Math and reading scores by grade
    - The math and reading scores by grade are grouped by school, so the replacement of ninth-grade scores only affects Thomas High School returning a NULL value and doesn't affect the output of the other rows in the school index.
    
    ![scores_by_grade_ex_ths](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/scores_by_grade_ex_ths.PNG)

- Scores by school spending
    - The removal of 461 students' grades did not have an impact on the district summary of reading and math grades binned by spending.
    ![scores_by_spending](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/scores_by_spending.PNG)

- Scores by school size
    - The removal of 461 students' grades did not have an impact on the district summary of reading and math grades binned by population size.
    ![scores_by_size](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/scores_by_size.PNG)

- Scores by school type
    - The removal of 461 students' grades did not have an impact on the district summary of reading and math grades binned by school type.
    ![scores_by_type](https://github.com/rptseng/School_District_Analysis/blob/main/Resources/scores_by_type.PNG)


## Summary
This is the summary of changes to the District results analysis after removing the grades at Thomas High School:
- Average Math Score from 79.0 to 78.9
- Average Reading Score from 81.9 to 81.9
- % Passing Math from 75% to 74.8%
- % Passing Reading from 85.8% to 85.7%
- % Overall Passing from 65.2% to 64.9%

Based on these results, we can conclude that the 461 ninth graders at Thomas High School were on average receiving higher grades than the 38,709 other students in the entire district, because every metric above decreases when their grades are removed.