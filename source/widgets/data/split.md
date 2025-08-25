Split
=====

Split text or categorical variables into indicator variables.

**Inputs**

- Data: data table

**Outputs**

- Data: data table with added columns

The widget splits the chosen text or categorical variable into separate variables. The newly-created variables can be categorical (Yes or No) or numeric (0 or 1) indicators, or appearance counts. The widget is typically used with survey data.

![](images/Split-stamped.png){width=40%}

1. Select the variable to split. Define the delimiter.
2. Set the type of output variables. Categorical produces categorical indicator with values Yes and No, Numerical produces a dummy numerical variable with values 0 and 1, while Counts creates a variable that contains the number of appearances of each term. The latter two options are equivalent if each value can appear only once.
3. If *Apply Automatically* is ticked, changes are communicated automatically. Alternatively, press *Apply*.

Example
-------

The workflow uses data from the Orange survey taken in 2020. The survey was done in Google Forms, which joins responses for multiple choice questions.

To use this data in the analysis, we have to split on a delimiter, a semicolon in this case. We do this using **Split**. We pass the data from the [File](../data/file.md) widget to Split and set the parameters.

Say, we wish to observe and count the reasons users like Orange. We split on *Reason* and set the delimiter to semicolon. The output will be an array of categorical variables. We can observe the results in a [Data Table](../data/datatable.md).

![](images/Split-Example.png)

The advantage of Split is that now, we can count each response individually. Say, we observe how the responses differ on the position of the respondent in [Box Plot](../visualize/boxplot.md). It seems the professors especially appreciate Orange for its visual programming approach.

![](images/Split-BoxPlot.png){width=500px}