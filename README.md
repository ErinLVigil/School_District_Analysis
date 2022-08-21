# School District Analysis

## Overview

  The school board is in the process of reviewing schools in the district to asses possible factors impacting the overall passing percentages of math and reading by the students. The overall budget of a school is averaged across each student to determine if the overall spend per student could drive up passing scores. The same logic is applied for school size, and type of school. 
  
  The analysis becomes a little bit more complicated when the board receives information that the 9th grade scores from Thomas High School might not be accurate and need to be removed from the analysis. This allows a more accurate assessment without worrying about untrustworthy data and skewed results. 
    
## Results 

  Before looking at the differences in the overall summaries, it is important to understand if the values for the 9th grade are very different than the values for the rest of the grades at Thomas High School. If the averages for the rest of the school are in the mid 80s, and the 9th grade is in teh 60s of the high 90s, we can assume that this is going to have a large effect on the school averages and in turn the other averages. It is also important to consider how many students are in the 9th grade. If this grade makes up 10% of the school or 60% of the school, this is also likely going to have a greater effect on our analysis. Thomas High School is the 4th least populated school as well, so not likely to make a huge impact when averaged against the rest of district.
  
  ![initial_math_scores](https://user-images.githubusercontent.com/109319148/185762795-055a888b-6d0e-4eab-b938-bf6a2dea7e49.png)

  Initial math scores before corrupted data is pulled out reveals that 9th graders at Thomas High school are performing well, but only about one tenth of a percentage point higher than the next highest grade and less than half a percentage point above the bottom grade. 

  Below, if we take the same approach, reading scores are not the highest in the school and roughly right in the middle of the results for the school.

![initial_reading_scores](https://user-images.githubusercontent.com/109319148/185762899-f8956df8-df48-4cda-926b-32676d5cd070.png)

  Lastly, the total count of 9th graders is 461 out of a school total of 1635. Roughly 25% of the school falls in this bucket, as expected. Right off the bat, I would not expect wild swings in the results.

**How are the summaries affected?**
* District summary
    There were changes in the in the average math scores but overall, the numbers stayed relatively similar. The math score went down about a tenth of a point.  
    
    This summary represents the initial district summary: 
    
    ![initial_district](https://user-images.githubusercontent.com/109319148/185797192-7979cc25-7d29-4b5a-b2bb-6ae73fd6ae43.png)

    This summary represents the updated summar:
    
    ![updated_district](https://user-images.githubusercontent.com/109319148/185797210-8d3c0b59-454c-4937-b2dc-840af287664d.png)
    
* School Summary and change to overall standings by removing 9th grade scores
    The updated results do not really change the overall rankings of the school. Thomas High School still ranks second even though the overall passing percentage went     down by about three tenths of a point.
    
    Initial School summary top 5:
    
    ![initial_school_summary](https://user-images.githubusercontent.com/109319148/185798407-ae3c4152-09d2-4e74-be4e-2808757b7dfe.png)
    
    Updated School Summary top 5:
   
   ![updated_schoolsummary](https://user-images.githubusercontent.com/109319148/185798418-0bc37d21-d772-43b1-85d2-fa1850cbf0e8.png)

 * How does replacing the ninth-grade scores affect the following:
    * Math and reading scores by grade
        Updating the scores by grades replaces the Thomas High School 9th grades with just NaN. It did not affect any of the other scores for grades of Thomas High             School
    * Scores by School spending
        Thomas High School is in the bucket of $631- 645 per student. None of the other buckets of spending would be affected. The scores were slightly different when 
        we looked at the initial results, but rounding the spending revealed that there were actually no changes overall. 
        
        Initial spending numbers:
        
        ![initial spending](https://user-images.githubusercontent.com/109319148/185798758-c90e1dd5-439d-4d9c-8c60-e8944b779f05.png)

        Updated spending:
        
        ![updated spending](https://user-images.githubusercontent.com/109319148/185798765-d4c09bb4-13a1-45fe-be3c-484ab34e5888.png)
        
    *  Scores by school size
        
        School size numbers were also not affected. Thomas High School is in the medium size school range and averaged out with the other schools in that range did 
         not change the numbers enough to change the rounded summary
         
    *  School type
        
        Thomas High School is a Charter school, so district schools will be unaffected. The charter school stores were slightly affected, but again, rounding made the         results almost exactly the same.
        
* Summary:
      When we first pulled Thomas High School 9th grade scores out of the averages, the percentages all went down significantly because the meterics were being calculated using the full student body. However, when we redid the analysis and pulled out the 9th graders for the averages, the results stabalized and came out similarly to our original analysis.
      1. The overall passing percent for Thomas High School changed and went down by around 3 tenths of a percent
      2. The overall school rankings did not change, but Thomas High School was closer to the 3rd highest school
      3. The district summary and school spending summaries were impacted, but when the formatting was applied to round to one decimal point, there was no nocicaable            change to the numbers
      4. Thomas High School now has no way to compare its 9th grade students against other schools, other charter schools, or other schools with similar spending since 
          the values are all Nan. 



