## A. Lesson Objectives and Key Terms
- understand the concept and usage of the remainder of the summary statistics:
	- standard deviation
	- variance
	- Inter-Quartile Range (IQR)

- differentiate between design of studies (experiments and observational studies)
	- understand merits, feasibility and ethical concerns of each
---
## B. Standard Deviations, Medians and IQRs
### Sample Variance & Standard Deviation
- are measures of dispersion

#### Standard Deviation
- provides a way to quantify the "spread" of data about the mean.
- formula of S.D. is derived via the *variance* ($\sigma^2$).

$$
\sigma^2 = \frac{(x_1 -\bar{x})^2 + (x_2 -\bar{x})^2 + ... + (x_n -\bar{x})^2}{n-1}

$$
- `n` is the number of data points; $x_1$ to $x_n$ is the values contained within the set of inputs (values of numerical *`x`* in the data set).

**Properties**
- ∴ formula  S.D.  = $\sqrt{variance}$
	$$
		s_x = \sqrt{\frac{(x_1 -\bar{x})^2 + (x_2 -\bar{x})^2 + ... + (x_n -\bar{x})^2}{n-1}}
	$$

	- Intuition on the S.D. formula -> might make sense to: 
		- take difference between each value and mean
		- add up the differences to get the `"total spread"`
		- divide by total number of points to get `"average spread"`
		- can't do this as average spread will be `0` ❌

- standard deviation is:
	- **non-negative** (i.e. $\geq 0$).
	- **adding a constant $k$** to a dataset changes the mean $\bar{x}$, but **doesn't change** the standard deviation $s_x$.
		- will only "shift" everything by constant $k$
	- **multiplying** all data points by constant $c$ results in the S.D. being multiplied by the **absolute value of $c$**  *(i.e. $s_{x-new} = s_{x-old} \cdot |c|$)*.


**Example of S.D. calculation** (explicit calculation)
Qn. Consider a simple sample data set $x$ of just `3` points. Given that $x = \{1, 4, 7\}$, find the S.D. value of this dataset.

1. Using the formula, $s_x = \sqrt{\frac{(x_1 -\bar{x})^2 + (x_2 -\bar{x})^2 + ... + (x_n -\bar{x})^2}{n-1}}$  we need to first obtain the mean of the dataset.
2. Also given $\bar{x} = \frac{1}{n} \sum x_n$ and $n = 3$

$$
	\bar{x} = \frac{ 1 + 4 + 7 }{3} = 4
$$
$$
	s_x = \sqrt{\frac{(1 -4)^2 + (4 -4)^2 + (7 -4)^2}{3-1}}
$$
$$
	\Longleftrightarrow s_x = \sqrt{\frac{(1 -4)^2 + (4 -4)^2 + (7 -4)^2}{3-1}}
$$
$$
	\therefore s_x = 3.
$$

### Understanding EDA, mean and S.D. through Palmer Penguins dataset



### Medians

### Quartiles and Interquartile Range (IQR)

### Mode


---
## C. Study Designs



