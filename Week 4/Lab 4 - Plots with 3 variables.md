## Using Radiant for 3 variables
- creating a new variable to keep track of the treatment type and size of stone together.
- remember to change the variable types to `factor` prior to starting on the lab exercise.

1. Go to the **Transform** tab in Radiant
	1. Click **Create** from the `Transformation Type` dropdown
	2. Name the new variable `TS` which concatenates the variables `treatment` and `size` together, delimited by a period *(i.e. `X.Large`, `Y.Small` etc.).*

		![Lab4a-1](../assets/lab4a-1.png)

```r
TS = interaction(Treatment, Size)
```

2. *Optional:* Verify the new column has been created under **Radiant > Data > Manage**
	![Lab4a-2](../assets/Lab4a-2.png)

3. Go back to the **pivot tab** to create the pivot chart in Radiant
	1. Plot the Categorical variables of `TS` against `Outcome (factor)`
		1. may want to uncheck `percentage` if selected
		2. *optional step:* Head to **Transform** tab to first change `TS`'s type to `character`
		
	![Lab4a-3](../assets/Lab4a-3.png)

4. We can normalize the values by column and apply the `fill` property for a 100% stacked bar plot here as well.

	![Lab4a-4](../assets/Lab4a-4.png)



---
## Using Excel to construct 3-variable table



---
## Using Excel to construct 3-variable sliced graph

