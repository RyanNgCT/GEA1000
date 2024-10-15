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
- is a modified version of a `2x2` table with sub-division into groups

Drag and drop on the menu as follows.
**Filters:** `Size`
**Column:** `Outcome`
**Values:** `Count of Treatment`
**Rows:** `Treatment`

![Lab4b-1](../assets/Lab4b-1.png)

We can create a new table containing 3 variables to analyze if Simpson's Paradox is present.
![Lab4b-2](../assets/Lab4b-2.png)

Use the **Field Settings** to change the column values to percentages (i.e. `% of column total`)

![Lab4b-3](../assets/Lab4b-3.png)

Thereafter, we can use the filter on `size` to derive the rest of the values from the pivot table itself.
- remember to use the filter and toggle between the options in Field Settings to obtain the right rate and count values for each of the sub-categories.

![Lab4b-5](../assets/Lab4b-5.png)
![Lab4b-4](../assets/Lab4b-4.png)

---
## Using Excel to construct 3-variable sliced graph

1. Similar to the above, just for graphs (refer to other steps to obtain the plot)

![Lab4c-1](../assets/Lab4c-1.png)

2. Move the variable `size` from *filter* to `axis(categories)`
	- Now we have:
		- **Column:** `Outcome`
		- **Values:** `Count of Treatment`
		- **Axis Categories:** `Treatment`, `Size`

![Lab4c-2](../assets/Lab4c-2.png)

3. We can now reorder the columns if we wish to obtain sorted by treatment then followed by size
![Lab4c-3](../assets/Lab4c-3.png)


4. We can also change it back to percentages if we wish.
![Lab4c-4](../assets/Lab4c-4.png)