---
title       : Chapter 13
subtitle    : Correlation and Regression
author      : Sherri Verdugo, M.S.
job         : Instructor, CSUF Sociology Department
framework   : deckjs        
highlighter : deck.js  
theme       : swiss
hitheme     : solarized_light      
widgets     : [mathjax, quiz, bootstrap]  
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Chapter 13

* Correlation and Regression
* Presented by: Sherri Verdugo, M.S.
* Instructor, CSUF Sociology Department
* Class: Soc 303

---

## Prologue

Regression and Correlation evaluate the strength of a relationship between variables. This time we are looking at interval or ratio levels of measurement. Our question of interest is: "What is the strength of t he relationship between the variables" for at least two variables. This time, we are looking at making a prediction. We do this using the techniques presented in Chapter 13 and Chapter 14. 

First we introduce a correlation coefficient, to ascertain the magnitude of relationship between two variables. If the value is large enough, we generate a linear regression equation. The larger our correlation coefficient, the more accurate the predictions will be. 

For example, does variable x have a relationship with variable y? Can we make a prediction about the variable from given information?

---

## Setting up 

When is correlation-regression analysis used?

Info.  | Outcome
-------|--------
Given  | $\;$ Two individual (raw score) variables measured by interval/ratio scales
Task   | $\;$ Measure the strength of the relationship between variables
Output | $\;$ If that relationship is sufficiently strong, describe the nature of the relationship between the two variables in such a way that it will be possible to predict a respondent's score on one variable if we know that person's score on the other variable

---

## Example of data used for Regression


```r
data(iris)
head(iris)
```

```
#   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
#          5.1         3.5          1.4         0.2  setosa
#          4.9         3.0          1.4         0.2  setosa
#          4.7         3.2          1.3         0.2  setosa
#          4.6         3.1          1.5         0.2  setosa
#          5.0         3.6          1.4         0.2  setosa
#          5.4         3.9          1.7         0.4  setosa
```


---

## Example from textbook pg. 445

We might be interested in other data besides Iris information. For example, we might want to look at political corruption:

Employee | x       | y 
---------|---------|---
1        | $\;$ 80 | $\;$ 160
2        | $\;$ 70 | $\;$ 95
3        | $\;$ 52 | $\;$ 97
4        | $\;$ 45 | $\;$ 85

* x = Annual income (in thousands of US dollars)
* y = Mean Monthly contribution in US dollars

* Question: does a relationship exist between annual income and mean monthly contribution?
* Question: how strong is the relationship?
* Question: can we make a prediction?
* Question: what is the prediction?

---

## Introduction of terms:

* Correlation Coefficient [page 446]: 
     * Measure of strength of a relationship in which data are not grouped in tables but are individual raw scores.
* Pearson's Product-Moment Correlation Coefficient (a.k.a. Pearson's r) [page 446]:
     * Coefficient that is used when both variables are an interval or a ratio level of measurement.
* Coefficient of Determination ($r^2$) [page 446]:
     * Indicates the proportion of variation in the dependent variable (y) that can be explained by variation in the independent variable (x).
* Regression Equation [page 447]:
     * the mechanism for estimating a y score from the respective x score.
* Correlation-regression Analysis [page 447]:
     * The presentation of correlation and regression techniques together.

---

## Graphs

### Cartesian coordinates

Sometimes we need to plot the data and we have some key terms that we need to understand:

* Cartesian Plots and Coordinates [page 447]:
     * A pictorial representation of the relationship between two or more variables under study. This method was developed by Rene Descartes.
* Origin of a Graph [page 448]:
     * The point of a graph where the two axes intersect indicating a value of zero on each axis.
* x-axis [page 448]:
     * the axis that extends horizontally.
* y-axis [page 448]:
     * the axis that extends vertically.
* Ordered Pair [page 450]:
     a set of two numbers in parentheses separated by a comma, indicating a point on a graph.
* x-coordinate [page 450]:
     * the first number in an ordered pair
* y-coordinate [page 450]:
     * the second number in an ordered pair


---

## Cartesian Coordinates Review

![cartplot1](cart_plot1.gif)

We put two number lines together in a single plot. 

* x = horizontal
* y = vertical

---

## Cartesian Coordinates Review

![cartplot1a](cartesian_coordinates.png)

* Quadrant I: x is positive and y is positive
* Quadrant II: x is negative and y is positive
* Quadrant III: x is negative and y is negative
* Quadrant IV: x is positive and y is negative

---

## Cartesian Coordinates Review

![cartplot2](coord1_quadrant.png)

Look at the origin and the coordinates.

* We have x = 6
* We have y = 4

---

## The concept of linearity

### Key terms: 

* Function [page 452]:
     * The case where a score on the dependent variable (y) may be predicted from a score on the independent variable (x). The value of (y) is obtained either graphically or by an equation.
* Linearity (linear related) [page 452]:
     * Relationship that is shown as an exact straight line.

---

## Example of a linear relationship

Respondents | $\;$ x  |  $\;$ y
------------|---------|--------
Daryl       | $\;$ 0  | $\;$ 0
Carol       | $\;$ 4  | $\;$ 2
Maggie      | $\;$ 8  | $\;$ 4
Glenn       | $\;$ 12 | $\;$ 6
Abraham     | $\;$ 16 | $\;$ 8
Rick        | $\;$ 20 | $\;$ 10

x = Education and y = Total Savings in thousands of dollars

---


```
##   row.names education savings
## 1     Daryl         0       0
## 2     Carol         4       2
## 3    Maggie         8       4
## 4     Glenn        12       6
## 5   Abraham        16       8
## 6      Rick        20      10
```


![plot of chunk linear11](assets/fig/linear11-1.png) 

---

Add a line to the graph



![plot of chunk linear2A](assets/fig/linear2A-1.png) 


---

## Linear Equations: Concepts

* Linear Equation [page 455]:
     * Equation in which the points generated will graph as a straight line rather than any other kind of graphic figure.
* A Linear Equation can be written as: $y=a+bx$
     * Constants: $a$ and $b$
     * Variables: $x$ and $y$
* Constant [page 456]:
     * Particular values of a specific linear equation that remain constant
* Variable [page 456]:
     * Particular values of a specific linear equation that vary from person to person (or unit of analysis to unit of analysis).
     
This is key to understanding how to manipulate equations for predictions...especially since we are using straight lines :)

---

## Examples of Lines and slope

* Note that $m$ is sometimes referred to as $b$ in some cases. 

![slope1](SLOPES.png)


---

## Slopes...not just for skiing

* y-intercept [page 456]:
     * the value of y at that point where the line crosses the y-axis (i.e., where $x=0$).
* Slope [page 458]:
     * The change in $y$ per unit change in $x$.

The slope is found by this equation: $\frac{y_2 - y_1}{x_2 - x_1}$


---

## Example of Slope 

![plot of chunk linear1](assets/fig/linear1-1.png) 

### How do we calculate this?

---

Respondents | $\;$ x  |  $\;$ y
------------|---------|--------
Daryl       | $\;$ 0  | $\;$ 0
Carol       | $\;$ 4  | $\;$ 2
Maggie      | $\;$ 8  | $\;$ 4
Glenn       | $\;$ 12 | $\;$ 6
Abraham     | $\;$ 16 | $\;$ 8
Rick        | $\;$ 20 | $\;$ 10

x = Education and y = Total Savings in thousands of dollars

* Step one: find two sets of scores to look at: Maggie and Abraham
* Step two: Write the ordered pairs for Maggie (8,4) and Abraham (16,8)
* Step three: $b=\frac{y_2 - y_1}{x_2 - x_1}=\frac{8-4}{16-8}=\frac{4}{8}=\frac{1}{2}=.5$
* Step four: confirm with two new pairs: Rick (20,10) and Carol (4,2)
* Step five: $b=\frac{y_2 - y_1}{x_2 - x_1}=\frac{2-10}{4-20}=\frac{-8}{-16}=\frac{-1}{-2}=.5$
* Our equation: $y=a+bx$. Visually, we saw that a = 0 and b = .5, so our equation is: $y=.5x$
* Check the results for someone other than Daryl (he has zero for both). Rick is $y=.5(20)=10$ and for Glenn $y=.5(12)=6$. This works!

---

## Relationships: Positive and Inverse

* Positive versus inverse (negative) relationship [page 459]:
     * Relationship in which one variable increases in magnitude and the other variable increases in magnitude.
     * Example: increased study time = increased grades
* Inverse or negative relationship [page 459]:
     * Relationship in which one variable increases in magnitude and the other variable decreases in magnitude.
     * Example: increased toxicity levels of dilantin results in decreased health.

---

## Introducing Linear Regression

* Curvilinear versus linear relationship [page 460]:
     * A curved versus straight-line relationship
* Curvilinear is outside of the scope for this class...we focus on linear relationships in this introductory course for statistics.
* Linear regression [page 462]:
     * Technique that finds a line that "fits" the scatter of the data points in such a way as to provide for any given value of $x$ the best estimate of the corresponding value of $y$.
* Scatter diagram/Scattergram/scatter plot [page 462]:
     * Diagram with data points that are scattered on the graph and not a perfect line or other figure.
* Least Squares Method [page463]:
     * Technique that finds the equation of the line that best fits the points of a diagram.
* Regression of $y$ on $x$ [page 463]:
     * Technique that informs us that the line we generate will be the line that enables us to most accurately predict $y$ from $x$.
* Regression Line: $\Sigma(y_i -y_i^\prime)^2$= a minimum    

---

## Lin. Regression Example 1


```
##   social.alienation religiosity
## 1                25          10
## 2                30           9
## 3                35           8
## 4                40           8
## 5                40           7
```

![plot of chunk lreg1a](assets/fig/lreg1a-1.png) 

---

## Linear Regression

### Conceptually: Minimums

* Regression Line: $\Sigma(y_i -y_i^\prime)^2$= a minimum    

![fig13_12](fig_13_12.png)

---

A worked example is:

![fig13_13](fig_13_13.png)

---

## Minimizing distances

![fig13_15](fig_13_15.png)

---

## Why do we do this?

* We need to find the line for the regression of $y$ on $x$.
* In other words, we are estimating and our linear equation becomes:
* Regression of $y$ on $x$: $\hat{y}=a_{yx}+ b_{yx}x$
* Regression of $x$ on $y$: $\hat{x}=a_{xy}+ b_{xy}y$
* Similar concept to $\hat{\sigma}$...we are estimating $y$
* Key concept behind regression: PREDICTION.
* Prediction of $y$ [page 468]:
     * The prediction or estimate of $y$ from a specific value of x as generated by the regression formula.

---

## Correlation Coefficient

In regression, we are interested in how "related" the variables are linearly. We do this by calculating Pearson's r. 

* Warning: this is a DIFFICULT equation...it has many components.

$r=\frac{n \Sigma xy - (\Sigma x)(\Sigma y)}{\sqrt{[n \Sigma x^2 - (\Sigma x)^2][n \Sigma y^2 - (\Sigma y)^2]}}$

---

## A word about correlation coefficients:

* r has a specific range of values: $-1 \leq r \leq 1$

## Example: Regression using Diamonds Data Set


```r
library(ggplot2)

data(diamonds)
head(diamonds,4)
```

```
#   carat     cut color clarity depth table price  x    y    z
#   0.23   Ideal     E     SI2  61.5    55   326 3.95 3.98 2.43
#   0.21 Premium     E     SI1  59.8    61   326 3.89 3.84 2.31
#   0.23    Good     E     VS1  56.9    65   327 4.05 4.07 2.31
#   0.29 Premium     I     VS2  62.4    58   334 4.20 4.23 2.63
```

---

## Diamond Plots

A plot of diamonds by clarity


```r
qplot(carat, price, data=diamonds, color=clarity)
```

![plot of chunk diamondsplot1](assets/fig/diamondsplot1-1.png) 


---


## Key Terms

* Correlation Coefficient [page 446]: 
     * Measure of strength of a relationship in which data are not grouped in tables but are individual raw scores.
* Pearson's Product-Moment Correlation Coefficient (a.k.a. Pearson's r) [page 446]:
     * Coefficient that is used when both variables are an interval or a ratio level of measurement.
* Coefficient of Determination ($r^2$) [page 446]:
     * Indicates the proportion of variation in the dependent variable (y) that can be explained by variation in the independent variable (x).
* Regression Equation [page 447]:
     * the mechanism for estimating a y score from the respective x score.
* Correlation-regression Analysis [page 447]:
     * The presentation of correlation and regression techniques together.
* Cartesian Plots and Coordinates [page 447]:
     * A pictorial representation of the relationship between two or more variables under study. This method was developed by Rene Descartes.
* Origin of a Graph [page 448]:
     * The point of a graph where the two axes intersect indicating a value of zero on each axis.
* x-axis [page 448]:
     * the axis that extends horizontally.
* y-axis [page 448]:
     * the axis that extends vertically.
* Ordered Pair [page 450]:
     a set of two numbers in parentheses separated by a comma, indicating a point on a graph.
* x-coordinate [page 450]:
     * the first number in an ordered pair
* y-coordinate [page 450]:
     * the second number in an ordered pair
* Function [page 452]:
     * The case where a score on the dependent variable (y) may be predicted from a score on the independent variable (x). The value of (y) is obtained either graphically or by an equation.
* Linearity (linear related) [page 452]:
     * Relationship that is shown as an exact straight line.
* Linear Equation [page 455]:
     * Equation in which the points generated will graph as a straight line rather than any other kind of graphic figure.
* Constant [page 456]:
     * Particular values of a specific linear equation that remain constant
* Variable [page 456]:
     * Particular values of a specific linear equation that vary from person to person (or unit of analysis to unit of analysis).
* y-intercept [page 456]:
     * the value of y at that point where the line crosses the y-axis (i.e., where $x=0$).
* Slope [page 458]:
     * The change in $y$ per unit change in $x$.
* Positive versus inverse (negative) relationship [page 459]:
     * Relationship in which one variable increases in magnitude and the other variable increases in magnitude.
* Inverse or negative relationship [page 459]:
     * Relationship in which one variable increases in magnitude and the other variable decreases in magnitude.
* Curvilinear versus linear relationship [page 460]:
     * A curved versus straight-line relationship
* Linear regression [page 462]:
     * Technique that finds a line that "fits" the scatter of the data points in such a way as to provide for any given value of $x$ the best estimate of the corresponding value of $y$.
* Scatter diagram/Scattergram/scatter plot [page 462]:
     * Diagram with data points that are scattered on the graph and not a perfect line or other figure.
* Least Squares Method [page463]:
     * Technique that finds the equation of the line that best fits the points of a diagram.
* Regression of $y$ on $x$ [page 463]:
     * Technique that informs us that the line we generate will be the line that enables us to most accurately predict $y$ from $x$.
* Regression of $x$ on $y$
     * Technique that informs us that the line we generate will be the line that enables us to most accurately predict $y$ from $x$.
* Prediction of $y$ [page 468]:
     * The prediction or estimate of $y$ from a specific value of x as generated by the regression formula.
* Coefficient of alienation ($1-r^2$)
* $\hat{y}$--predicted value of y
* Intra class correlation coefficient ($r_1$ or $r_i$)
* Correlation ratio [$E$ or $\eta$]

---

## Equations of Interest

* Linear Equation: $y = a + bx$
* Slope: $\frac{y_2 - y_1}{x_2 - x_1}$
* Regression Line: $\Sigma(y_i -y_i^\prime)^2$= a minimum
* Regression of $y$ on $x$: $\hat{y}=a_{yx}+ b_{yx}x$
* Regression of $x$ on $y$: $\hat{x}=a_{xy}+ b_{xy}y$
* Pearson's Correlation Coefficient: $r=\frac{n \Sigma xy - (\Sigma x)(\Sigma y)}{\sqrt{[n \Sigma x^2 - (\Sigma x)^2][n \Sigma y^2 - (\Sigma y)^2]}}$
