# PyCity School District Analysis 

## Overview:
We are asked by Maria and the PyCity School board to run district wide High Schools Math and Reading scores analysis to help them plan for next school year.  Our initial PyCity School District Analysis report created for Maria and the school board included: 

* A high-level snapshot of the district's key metrics, presented in a table format
* An overview of the key metrics for each school, presented in a table format
* Tables presenting each of the following metrics:
* Top 5 and bottom 5 performing schools, based on the overall passing rate
* The average math score received by students in each grade level at each school
* The average reading score received by students in each grade level at each school
* School performance based on the budget per student
* School performance based on the school size 
* School performance based on the type of school

Later, we were informed that the school board has notified Maria and her supervisor that the csv file that we used (students_complete.csv) shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Maria has asked us to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once these grades are changed to NaNs, then run the school anylysis again based on the changed analysis criteria.  


## Procedures and Results:

We used Python and its Pandas library to run our analysis. Pandas allows Python programmers the ability to work with two data types, Series and DataFrames, which are structured lists with many built-in convenience methods that allow for quick and easy manipulation of data.

We installed Anaconda that provides toolslike Jupyter Notebook needed to create a developmental environment to match the school district programmers' virtual environment.  Then we ran our initial district analysis for math and reading scores based on given criteria.  Later, when Maria asked us to change the Thomas High School's 9th graders math and reading scores to NaN's, we changed the student_data_df for 9th graders by using Pandas loc() function to NaNs. The image below from Jupyter Notebook Output shows that change:

![Screen Shot 2022-03-15 at 1 36 28 PM](https://user-images.githubusercontent.com/98566486/158438008-ead48bbf-1cee-4db9-a2f0-20acb5f5b6c0.png)

After that change, we ran the following analysis:

### The district summary

 We recalculated the total student count by subtracting the number of ninth-grade students in Thomas High School from the total student count, then we recalculated the passing math and passing reading percentages, and the overall passing percentage with the recalculated total student count. The overall numbers got changed by less than a percent for the district wide test scores and perecentages as shown in the images below from original analysis vs revised analysis table:
 
  __Original District Analysis DataFrame__
 ![Screen Shot 2022-03-15 at 2 04 57 PM](https://user-images.githubusercontent.com/98566486/158443151-f08ba6f4-714c-4050-b07a-399cb7f0a71e.png)

 
  __Revised District Analysis DataFrame__
![Screen Shot 2022-03-15 at 2 05 06 PM](https://user-images.githubusercontent.com/98566486/158443219-2da690fa-c354-4723-b256-313e52c83ca6.png)
 

### The school summary
We executed the code from this module that created and formated the School Summary DataFrame, then wecupdated the school summary using the 10th-12th graders from Thomas High School by calculating the number of 10th-12th graders in Thomas High School. We Created three new DataFrames for the 10th-12th graders from Thomas High School: students who passed math, students who passed reading, and students who passed both math and reading.
Using these DataFrames, we recalculated the percentage of students who passed math, passed reading, and passed both math and reading for Thomas High School only.
Finally, we replaced the % Passing Math, % Passing Reading, and % Overall Passing scores in the current School Summary DataFrame with the new passing percentages for Thomas High School.
The revised analysis for Thomas School showed that overall passing score was changed slightly from 90.94% to 90.63%. However, the ranking per school based on budget dropped significately from around 91% to 65%. 

### The top 5 and bottom 5 performing schools, based on the overall passing rate
 

* The average math score for each grade level from each school
* The average reading score for each grade level from each school
* The scores by school spending per student, by school size, and by school type





Summary:

There is a statement summarizing four changes to the school district analysis after reading and math scores have been replaced (5 pt).
Challenge
