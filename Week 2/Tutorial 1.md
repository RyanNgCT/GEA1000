## Tutorial 1 Exercises

Name: *Ng Chin Tiong Ryan*
Matric No.: *AXXXX578N*
Tutorial Class: *D30*

---
#### Question a) State the sampling frame and determine what type of sampling was done here.

- Sampling frame: 1901 records
- Simple random sampling was carried out in this case.

#### Question b) For all the variables, except IMDb Rating, determine which are numerical and which are categorical. Were there instances where it was unclear whether to classify the variable as numerical or categorical?

| Variable          | Type of variable                                                                                                                             |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Title             | Categorical                                                                                                                                  |
| Production_Budget | Numerical                                                                                                                                    |
| Worldwide_Gross   | Numerical                                                                                                                                    |
| Release_Year      | Numerical                                                                                                                                    |
| CPI               | Numerical                                                                                                                                    |
| Duration          | Numerical (continuous in nature)                                                                                                             |
| MPAA_Rating       | Categorical                                                                                                                                  |
| Voter_Numbers     | Unable to determine as some of them are a definite value and some have a range (i.e. `M` or `k` to represent millions or thousands of votes) |
| Genre             | Categorical                                                                                                                                  |

#### Question ci) Identify the variables for which there are missing values.
`Release_Year`, `CPI`, `Duration`, `MPAA_Rating`, `IMDb_Rating`, `Voter_Numbers`, `Genre` all have blanks.

#### Question cii) Name the variables for which the number of missing values is relatively small (i.e., greater than 0 and less than 30). Given that the number of missing values for these variables is small, suggest what can be done for this form of dirty data. 

`Gender`, `CPI`, `Release_Year`

Fill them up with information where possible to make the dataset more complete. 

Drop the rows with missing data.

#### Question ciii) Name the variables for which the number of missing values is very large (i.e., more than 100). If you were to try and implement your suggestion(s) in (ii), to what extent is it feasible here?

`Duration`, cannot apply the same method to drop row records.


#### Question civ) 

---

#### Qa) State the aim of your study. 
Find out if the new instructional system would help improve the math proficiency of students aged 3 to 5 years old as compared to current methods

#### Qb) Your colleague who works with you suggests the following after having read the aforementioned research paper.  
> “Their study seems to be well conducted with clear metrics/procedures and furthermore, since it is a randomised controlled trial, it is a fair comparison since treatment and control groups are similar to each other. The researchers have already shown the effectiveness of the new instructional/assessment system. We can just implement the new instructional method to all classes in the preschool since their study has already demonstrated its effectiveness, instead of reinventing the wheel.” 
#### Explain why this would or would not be a good idea. 
Their study seems to be well conducted with clear metrics and since it is a randomised trial.

#### Qc) What design of study would ideally be suitable to compare the *effectiveness* of the new system?  

Keyword: effectiveness

Controlled experiment, can control
 
#### Qd) Based on your choice in c), give some details on how you can proceed to set up the study. Your answer should clearly state the following: 
- The measurement of the variable that will allow for determining the effectiveness of the new system.  
- Whether random assignment would be possible. 
	- *using random number generator*
- Whether blinding of subjects/assessors is possible. 
	- *blinding possible for assessors (not teachers) but maybe not for subjects*
- What would be some limitations and difficulties encountered in the process of conducting the study? 
	- *Parental consent -> unfair to treat students with improved method vs traditional method*