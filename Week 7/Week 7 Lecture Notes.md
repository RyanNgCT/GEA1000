# Week 7 Lecture Notes

## A. Background and Motivation
The Plan, Data and Analysis Phases of PPDAC involved the use of specialized tools and techniques to inter-relate these three phases.

> *def:* Statistical Inference is the process of drawing conclusions from sample data.
### Key Learning Outcomes
- concepts of basic probability theory (condition probability), independent and mutually exclusive events, discrete and continuous random variables
- prosecutor's fallacy, base rate fallacy and conjunction fallacy
- statistical inference using
	- confidence intervals
	- hypothesis tests
### The Analysis Phase of PPDAC
- use of Summary Statistics (Chp 1)
- analysis of categorical variables using rates, rules of rates etc. (Chp 2)
- analysis of numerical variables using the correlation coefficient, visualizations and five-point summary stats (Chp 3)

---
## B. Introduction to Probability
**Uncertainty**
- use `"chance"` to mean that something is indefinite or not certain to occur
- when comparing likelihood of occurrence, we use terms like `more or less likely` $\implies$ common for everyday use but not precise when we deal with data @ a deeper level (need some concrete way of defining uncertainty)

> *def:* Probability is a mathematical means to reason about uncertainty.

### Classic Problem and Motivation
- determine the possible outcomes and "likelihood" of the side where a coin lands after two tosses
	$$Set(Outcomes) = sample\_space =  \{HH, HT, TH, TT\}$$

> *def:* A Probability Experiment is any procedure that can be **infinitely repeated** and has a well-defined, **precise set of outcomes**.

- probability experiment must be repeatable

> *def:* A **sample space** is the collection of *all possible outcomes* of a probability experiment
- an event is a group of element(s) / sub-collection of the sample space
$$
Event_1 = HT
$$
$$
Event_2 = HT, TH, TT
$$

> For a probability experiment with an associated sample space, the *probability of an event* of the sample space is the total probability that the outcome of the experiment is an element of the event.

$$
\begin{aligned}
Event_n \subset \mathcal{E} 
\newline \newline
\{2, 4, 5\} \subset Set(Dice \: rolls)
\end{aligned}
$$
### Probability of an Event, `P(E)`

The probability of Event $E$, denoted $P(E)$ takes on a numerical value between *zero and one* inclusive $\implies \: 0 \le P(E) \le 1$ .
- note that $P(E)$ should be the **long-run proportion** of observing $E$ with many repetitions (i.e. $N$, which is also called the sample space).
- $P(E)$ is estimated using the following formula
		$$
			P(E) = \frac{count(E)}{N}
		$$

- $P(E) = 0$ *iff* $E$ is an impossible event
- $P(E) = 1$ *iff* $E$ is a certain event

**Important Notes**
1. The estimate of $P(E)$ obtained from $N$ repetitions is likely to be **different**, if we repeat the experiment (and get estimate of $P(E)\:$) another $N$ times.

2. Such estimates of $P(E)$ get more accurate and closer to the actual true $P(E)$ value as $N$ becomes larger.

### Rules of Probabilities
- Virtually impossible to verify the true probability of an event for a given probability experiment
- $\therefore\:$ sufficient to just provide estimates as if it were the true probability

- need to ensure that some rules are observed
1. The probability of each event $E$, denoted $P(E)$, is a number between 0 and 1 inclusive.
2. If we denote the entire sample space by $S$, then $P(S)$ is 1.
3. If $E$ and $F$ are mutually exclusive events (can't happen simultaneously), then $P(E \cup F) = P(E) + P(F)$

We will stick to assumption that the sample space contains only a finite number of outcomes.

### Uniform Probability
> *def:* **Uniform probability** is the way of assigning probabilities to outcomes such that **equal probability** is assigned to *every outcome* in the *finite sample space*. Thus, if the sample space contains a total of $N$ different outcomes, then the probability assigned to each outcome is $\frac{1}{N}$.




---
## C. Prosecutor's Fallacy