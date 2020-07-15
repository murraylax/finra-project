---
title: "Data Analytics Homework"
subtitle: "Exploring the FINRA Financial Capabilities Data Set"
author: 
  - "[Place Student Name Here]"
  - "ECO 230: Data Analysis for Business"
  - "Instructor: James M. Murray, Ph.D."

output: 
  html_document:
    keep_md: yes
  pdf_document: 
#    fig_width: 7
#    fig_height: 3.5
    
params:
  output_format: 'all'
urlcolor: blue
---

# Preparing the Data Set and the R Environment


The following command loads a sample of the National Financial Capability Study 2015 survey responses. The data has been cleaned, coded, and stored in an R data frame called `df`.


```r
load("findata.RData")
```

See the code book for all the variable descriptions.

The questions below involve using the packages `tidyverse`, `Hmisc`, and `scales`. Install these, if necessary, and load into memory using, 


```r
install.packages("tidyverse")
install.packages("Hmisc")
```


```r
library("tidyverse")
library("Hmisc")
library("scales")
```

# Questions

1. What is the scale of measurement and class for the education variable, `Edu`? Give the definition for this scale of measurement. If the scale of measurement is nominal or ordinal, use R to show the possible categories. Hint: See the statistics tutorial, "Introduction to Data".


```r
# Use this area to type R code for your answer
```

*[Replace this text with a written description of your answer]*

2. Compute the mean number of correct quiz questions (variable `QuizScore`) for each educational level (variable `Edu`). Hint: See "Group and Pipe" from the "Introduction to Data" statistics tutorial.


```r
# Use this area to type R code for your answer
```

*[Replace this text with a written description of your answer]*

3. Create a bar plot showing the mean rating (scale 1-7) that people give themselves on their financial knowledge (variable `FinancialKnow`) for each level of education (variable `Edu`). Give the plot error bars to display confidence intervals for each mean. Give the plot a title, make the bars dark red in color, and make sure labels do not overlap.


```r
# Use this area to type R code for your answer
```

*[Replace this text with a written description of your answer]*

4. Create again a plot like #3, but make a multiple bar chart that includes separate bars for males and females (variable `Female` is equal to 1 for a female and is 0 otherwise). Hint: use `fill=as.factor(Female)` in the aesthetics layer.


```r
# Use this area to type R code for your answer
```

*[Replace this text with a written description of your answer]*

5. Create a bar plot of the proportion of people that contribute to their retirement (i.e. use `stat_summary()` with `fun.data=mean_sdl`), for people with each possible quiz score (0-6) (use `as.factor(QuizScore)` for the x aesthetic). Have your plot include the following:

 - Dark green bars
 
 - Make sure the scale for the y-axis is a percentage. Use `scale_y_continuous(label=percent)`.
 
 - Give the plot a title
 
 - Give error bars to visualize the confidence intervals for these estimates
 
 - Finally, give a one or two sentence description on what information is revealed in the plot about the relationship between financial literacy and making retirement contributions.
 
*Hint: When you take a mean of a binary variable (a variable equal to 0 or 1), the result is the proportion of observations equal to one. Then you can convert this to a percentage.*
 
For example, the following R code computes the mean of `RetireContribute` which is a binary variable equal to 1 if a person regularly makes contributions to his or her retirement savings:


```r
mean(df$RetireContribute, na.rm=TRUE)
```

```
## [1] 0.6754126
```

A mean equal to 0.67 means that 67\% of people contribute to their retirement savings.
 

```r
# Use this area to type R code for your answer
```

*[Replace this text with a written description of your answer]*
