## Radiant - one variable
1. Import the dataset, `kidneystones.csv`
2. Transform data types as factor before continuing (since we are dealing with categorical values)
3. Create **pivot table** with `Outcome` listed as single categorical variable
	1. To obtain the bar plot below, select *show plot* in the left sidebar.

![Lab3a-1](../assets/Lab3a-1.png)

4. Normalize by `total` (total counts) to create a normalized contingency table.
5. Check the `percentage` checkbox.

![Lab3a-2](../assets/Lab3a-2.png)

6. Optional: change the level of precision using the `Decimals` field
![Lab3a-2b](../assets/Lab3a-2b.png)
## Radiant - two variables
Same procedure as above, except we need to order the categorical variables (Independent first $\to$ `treatment` then dependent $\to$ `outcome`).
- make sure that the variables are in order before plotting (just add the second one then reorder them as desired)

![Lab3a-3](../assets/Lab3a-3.png)

Do the same thing as above. For stacked bar plot, check `Fill` in plot type.
- can change the normalization factor as `Column` (not shown here)
![Lab3a-4](../assets/Lab3a-4.png)

Normalize by column to show table with row proportions / percentages
![Lab3a-5](../assets/Lab3a-5.png)

---
## Excel - one variable
utilizing the following excel functionalities in creating the spreadsheets
- sort and filter function
- pivot table function

We first have to gather some statistics (counts of the two possible outcomes).

### The primitive way
Select all columns then click `Filter`, then click on a specific outcome value and observe the Count and the bottom pane. Repeat the same process for the other outcome value.

![Lab3b-1](../assets/Lab3b-1.png)

### The faster way
- Use of excel formulas
```r
# format: =COUNTIF(<column_selection>, <string_value>)
=COUNTIF(D:D, "Success")

# format: =ROUND(<target_value>, <precision>)
=ROUND(H3/COUNTA(D:D),4)
```
	
 - precision specifies the number of decimal places (i.e. `4 d.p.` in this case).

![Lab3b-2](../assets/Lab3b-2.png)

**Go to `Insert > Pivot Chart`** and then select the entire dataset with `Ctrl` +` Shift` + `→` + `↓`.

Then drag and drop `Outcome` into both the **Legend (Series)** and **Values**.

![Lab3b-3](../assets/Lab3b-3.png)

![Lab3b-4](../assets/Lab3b-4.png)

**Changing / Adding chart properties**

![Lab3b-4b](../assets/Lab3b-4b.png)
## Excel - two variables
Drag the Treatment field as rows and Outcome as columns, similar to radiant. For the value, we put the Count of treatment.

Drag and drop on the menu as follows.
**Column:** `Outcome`
**Values:** `Count of Treatment`
**Rows:** `Treatment`

![Lab3b-5](../assets/Lab3b-5.png)

Click on PivotTable Analyze > Pivot Chart

![Lab3b-6](../assets/Lab3b-6.png)

To adjust to percentage, click on one value in the table itself, the go to **Pivot Table Analyse > Field Settings > Show Values As** then select `Percentage of Row Total`.
![Lab3b-6b](../assets/Lab3b-6b.png)


![Lab3b-7](../assets/Lab3b-7.png)