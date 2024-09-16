## A. Learning Outcomes and Key Concepts
- introduces EDA techniques and concepts for analyzing and interpreting numerical data

**What is Numerical Data?**
- It is data predominantly analyzed using regression analysis (regression is a major part of statistics)
- the chapter covers
	- univariate data analysis
	- bivariate data analysis - correlation of variables and related concepts

- Introduces Simple linear regression concepts 
	- how this technique is being used for real data sets

**Modelling or Plotting Numerical data**
- use of *histograms, boxplots and scatter plots*
- can be done for both univariate and bivariate data sets
---
## B. Motivation
- attempt to solve issue problem using real housing data collected in Singapore

- Dataset (`housing-raw.csv`): Sales of HDB Resale flat information between Jan 2017 to Jun 2021

**Problem: What factors may affect the popularity and pricing of resale flats sold in Singapore?**

**Plan: Narrow down the factors in the Problem state (by shortlisting)**
- Age? (of the resale flats at the point of sale)
- Floor Area?
- Time Period?

**Data: Clean and prepare the data**
- Remove irrelevant columns from 11 down to 4 in the cleaned dataset (have just `month`, `floor_area_sqm`, `age` and `relae_price` left)
- Filter the months to include just Jan to Jun 2021
- create the `age` column using calculation

---
## C. Univariate Data Analysis
> *def:* A **distribution** is an *orientation of data points* broken down by their observed number of frequency of occurrence.

can present / relate the variables `age` with its frequency (which can be called `freq_of_ages`)
- may not be very useful to see the patterns in the data
### Histogram
- graphical display of the distribution

**Steps for Creation of the histogram plot**
- divide frequency table into smaller bins containing a range of values (i.e. distinct age counts of `2, 3, 4, 5, 6, 7, ...` become `0-2`, `2-4`, `4-6` etc.)
	- bins exclude the lower end-point and include the upper end-point of the interval

- Construct bars for each bin on the x-axis

- deciding bin range: often unclear and requires iterations
	- is an important factor since data gets grouped differently after adjusting the bin sizes and can affect our description/judgement based on the data
	- affects how we "estimate" the central tendency and skew of the distributions

**Considerations / Best practices**
- avoid histograms with **large bin widths** that group data to a limited number of bins (no variability in description of data)
- avoid histograms with **small bin widths** that group data into too many bins (also affects one perception of distribution)
- don't confuse histograms with bar plots (one shows distribution across numerical bins/ranges while the other compares categories of the same variable, one has breakages or gaps while the other doesn't)

	![histogram-by-age-sample](../assets/histogram-by-age-sample.png)

**Advantages**
- presents the same info as a frequency table but is easier to understand
- useful for large(r) data sets $\implies$ impractical to show the value of individual observations

### Describing distributions
When graphing a distribution of a quantitative variable we look out for the:
- **Overall pattern** (Shape, Centre and Spread)
- **Deviations/Exceptions from the general pattern** (Outliers)

#### 1. Shape
We look out for the shape of the distributions via its *peaks and skewness* (a.k.a. descriptors)
- unimodal distribution: have one distinct peak
- bimodal distribution: have two peaks
- multimodal distribution: have multiple peaks

Characteristics Unimodal/Bimodal distributions

![shapesOfDistributions](../assets/shapesOfDistributions.jpg)
*Classifications*
- Symmetrical: Left and right halves are approximate mirror images, peak is in the centre
- Left-skewed: long left tail, peak to the right
- Right-skewed: long right tail, peak to the left

#### 2. Measures of Central Tendency (or centre)
- use mean, median and mode ad the measures of skewness

![central-tendency-skewness](../assets/mean-median-mode-skewness.png)
#### 3. Spread
- **variability** of the distribution around their measures of central tendency using the measures of range and standard deviation
- "spread" across a wider range or higher frequency at the centre?

> *def:* the **range** of a data variable is the difference between the highest and lowest recorded data points
- may be misleading at times (give the wrong impression if we don't consider the distribution)

#### 4. Outliers
> *def:* Outliers are observations that fall well above or well below the overall bulk of the data
- use our judgement or more precise calculation/plotting methods (i.e. using a box plot)
**Why examine outliers?**
1. to identify strong skew in a distribution
2. for identifying possible data collection and/or entry errors
3. providing interesting insights to the data

**Key considerations**
- mean may be affected as a result of outliers that it does not become a good measure of central tendency
- median and mode are called **robust statistics** (since outliers don't have effects on these)

- may be worth repeating data analysis twice (to evaluate/provide some justifications to whether they should be dropped)
	- with outliers
	- without outliers (with them removed)

### Boxplots
- use a five-number summary to construct the box plot
	- Minimum (Q0)
	- Quartile 1 (Q1)
	- Median (Q2)
	- Quartile 3 (Q3)
	- Maximum (Q4)

- $IQR$ is calculated using $Q3 - Q1$

**Outlier definition in stats**
$Q3 + 1.5(IQR) \lt outlier \lt Q1 - 1.5(IQR)$

**Steps in constructing box plots**


---
## D. Bivariate Data Analysis

### Deterministic Relationships

### Association between two variables

### Scatter plots