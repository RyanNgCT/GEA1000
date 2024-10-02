## A. Overview and Learning Objectives
- understand confidence intervals and how it is used to
	- derive an interval estimate
	- understand unknown population parameters (population proportion and mean)

- understand the 4 key steps in hypothesis testing

- apply hypothesis testing in carrying out the chi-squared test and the one-sample t-test
---
## B. Statistical Inference
Important to have well-defined generalisability criteria when conducting sampling $\implies$ is the result of the study representative of the population of the sample?

- sample statistics are subject to inaccuracies (*bias* of researchers / respondents + *random error*)
	- but want to **minimize these inaccuracies** to be as close as possible to population parameter
```python
Sample Statistic = population parameter + bias + random error
```

1. Need to know the survey methodology used to generate the sample
2. Need to also know the statistical methods used to infer finding(s) from the target population in question.
	1. can statistics from the sample level be generalised / lead to similar conclusions at the population level?

> *def:* **Statistical inference** refers to the use of samples to draw **inferences or conclusions** about the population in question.

After EDA is completed, for a given sample, we need to cycle between:
1. Generating Questions
2. Visualization and Analysis of the variables in question
3. Answer Questions and if needed, refine them (fed back into point 1)

#### Advantages of Sample versus Census
1. **Cost:** census requires measurement of every unit in the population 
	1. costly, have a chance of missing out certain groups
	2. very resource intensive

2. **Feasibility:** Instead of taking a small portion for "experiment", require to take everything (i.e. go overboard)
	1. example: Doctor needing to take all of a patient's blood for blood test instead of a small sample

### Rule of Inference
> *def:* The *Fundamental Rule of Inference* states that available data can be used to make inferences about a much larger group if the data can be considered to be representative with regards to the question of interest.

- by adopting good sampling methods and good practices (i.e. having a good sampling frame), we can greatly reduce selection bias to be insignificant.