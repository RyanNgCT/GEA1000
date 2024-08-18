## A. Lesson Objectives and Key Terms
- understand the concept and usage of the remainder of the summary statistics (S.S.):
	- standard deviation
	- variance
	- Inter-Quartile Range (IQR)

- differentiate between design of studies (experiments and observational studies)
	- understand merits, feasibility and ethical concerns of each
---
## B. Standard Deviations, Medians and IQRs
### Sample Variance & Standard Deviation
- are measures of dispersion
#### I. Sample Variance
$$
\sigma^2 = \frac{(x_1 -\bar{x})^2 + (x_2 -\bar{x})^2 + ... + (x_n -\bar{x})^2}{n-1}

$$
- `n` is the number of data points; $x_1$ to $x_n$ is the values contained within the set of inputs (values of numerical *`x`* in the data set).
#### II. Standard Deviation
- provides a way to *quantify* the "spread" of data about the mean.
- formula of S.D. is derived via the *variance* ($\sigma^2$), particularly using the square root operation.
- S.D. value of zero -> there is no spread; S.D. value $\gt{0}$ -> there is some sort of spread in the sample.

**Properties**
- ∴ formula  S.D.  = $\sqrt{variance}$
	$$
		s_x = \sqrt{\frac{(x_1 -\bar{x})^2 + (x_2 -\bar{x})^2 + ... + (x_n -\bar{x})^2}{n-1}}
	$$

	- Intuition on the S.D. formula -> might make sense to: 
		- take difference between each value and mean
		- add up the differences to get the `"total spread"`
		- divide by total number of points to get `"average spread"` 
		- can't do this as average spread will be `0` ❌, $\because$ `+ve` and `-ve` values might cancel each other out

- standard deviation is:
	- **non-negative** (i.e. $\geq 0$).
	- **adding a constant $k$** to a dataset changes the mean $\bar{x}$, but **doesn't change** the standard deviation $s_x$.
		- will only "shift" everything by constant $k$
	- **multiplying** all data points by constant $c$ results in the S.D. being multiplied by the **absolute value of $c$**  *(i.e. $s_{xNew} = s_{xOld} \cdot |c|$)*.


**Example of S.D. calculation** (explicit calculation)
Qn. Consider a simple sample data set $x$ of just `3` points. Given that $x = \{1, 4, 7\}$, find the S.D. value of this dataset.
1. Using the formula, **$s_x = \sqrt{\frac{(x_1 -\bar{x})^2 + (x_2 -\bar{x})^2 + ... + (x_n -\bar{x})^2}{n-1}}$**  we need to first obtain the mean of the dataset.
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
**Palmer Penguins Intro**
- consists of 3 species - Chinstrap, Gentoo and Adelie
- data from 342 penguins with various data points (i.e. species, bill length, bill depth, flipper length, mass, gender etc.)

**Question to answer from the dataset**
How similar are these penguins? -- compare:
1. characteristics like behaviours, habitats and living environments
2. r/s between two or more variables
3. feeding habits across species?
4. mass of the penguins - are males heavier than females within each species?
5. flipper length across species?

![penguin_mass_by_species_sum_stats](../assets/penguin_mass_by_species_sum_stats.png)

Why is it that the Adelie and Chinstrap (species) have almost the same mean mass but yet the S.D. for the Adelie species is higher?
- due to what?
	- gender
	- age, or other factors not inside the dataset?
	- location

**Comparing spread btwn variables**
- when considering to factor in the spread btwn variables, we also need to consider spread relative to the mean (a.k.a. coefficient of variation)

$$
	coefficient\:  of\:  \sigma^2 = \frac{s_x}{\bar{x}} \: \mid \bar{x} \ne{0}
$$
- larger coefficient of variance (i.e. = $\frac{s_y}{\bar{y}} \gt{\frac{s_z}{\bar{z}}}$ $\implies$ spread of $y \gt$ spread of $z$).
### Median
- *definition*: median of set of values in a dataset is the **middle value** after arranging the values of the dataset in ascending or descending order.
	- sort column -> find middle value
- 50th percentile of the data

- formula
	- note: $n$ is the number of element in the set and so $\frac{n+1}{2}$ gives the middle element for odd cases.
$$
	Med(X) = 
\begin{array}{cc}
  \Bigg \{ & 
    \begin{array}{cc}
      X \left[\frac{n+1}{2}\right] & if\: n \: is \: odd. \\
      \frac{X \left[\frac{n}{2}\right] + X \left[\frac{n+1}{2}\right]}{2} & if\: n \: is \: even.
    \end{array}
\end{array}

$$

**Overall vs Subgroup Medians**
- subgroup mean would **NOT lie closer** to the group with the larger proportion $\implies$ knowing the median of the subgroup does not tell one about overall median

**R/s btwn Mean and Median**
- For roughly symmetric distributions, $\bar{x} \approx Med(X)$.
### Quartiles and Interquartile Range (IQR)
- Quartiles allow use to defined another notion/type of dispersion measurement via IQR.
	- generally use software(s) for this computation

|                                  | in terms of percentile | # element                                  |
| -------------------------------- | ---------------------- | ------------------------------------------ |
| $Q_1$ (first quartile)           | 25th                   | $\frac{n+1}{4}$ th                         |
| $Q_2$ (second quartile / median) | 50th                   | $\frac{n+1}{2}$ th or $\frac{2n+1}{4}$ th* |
| $Q_3$ (third quartile)           | 75th                   | $\frac{3(n+1)}{4}$ th                      |
**Formula:**
1. Median: $Med(X) = Q_2$ (see above for full formula)
2. Interquartile Range: $IQR(X) = Q_3 - Q_1$
3. Quartile Deviation = $\frac{Q_3 - Q_1}{2}$

**Similarities btwn IRQ and S.D.** (in terms of properties)
1. $IQR(X) \ must \ be \geq 0, \: \because Q_3 \geq Q_1$
2. $\forall{x}$,  given $c$  is a constant, $x + c$ does not result in $\displaystyle \bigtriangleup{IQR(X)}$, for $\pm{c}$
3. Multiplying all data points by constant $k$ results in $IQR(X)$ being multiplied by $|k|$.
	1. i.e. $IQR(X)_{new} = IQR(X)_{old} \cdot k$
### Deciding which pairs of S.S. to use
- $\bar{x}$ & $s_x$ or Median & IQR -> depends on the distribution of data points.
	- symmetrical vs non-symmetrical data
### Mode
- value that appears the most frequent for a particular feature/variable in a dataset
	- "peak" of the distribution

---
## C. Study Designs



