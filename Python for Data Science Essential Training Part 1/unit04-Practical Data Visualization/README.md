# Practical Data Visualization
## 1. Creating standard data graphics
Standard Chart Graphics are excellent tool for conveying simple data insights in a way that anyone can understand.
### Line Chart
* Show the change in value of an attribute with respect to a x-variable(which is often _time_).
* Can be used to visually compare the values of several related attributes.
* **Example**: show how the total number of items purchased per day has increased since the change
![Line Chart](./resources/images/Line-Chart.png)

### Bar Chart
* Represent data attribute values within a particular data category by using bars of differing height.
* Bar charts represent observation counts within categories.
* **Example**: show that the number of purchases increased for customers in the 18 to 25 year old category, but decreased for customers in the higher than 44 year old category.
![Bar Chart](./resources/images/Bar-Chart.png)

### Pie Chart
* Represents data attribute values using a circle and slices that comprise it.
* A whole and entire set of categorical data is represented by the complete circle, and the proportions of observations that fall into different categories are represented by proportionate pie slices.
* **Example**: you use a pie chart to show what categories of products generate the greatest proportion of sales, and how the site changes affected that proportion before and after.
![Pie Chart](./resources/images/Pie-Chart.png)

**To summarize, you use**
* [**Line Chart**](#line-chart): To show changes overtime.
* [**Bar Chart**](#bar-chart): To show changes in categorical data.
* [**Pie Chart**](#pie-chart): To show categorical data as proportions of a whole.

### Plot Building
Two Methods for Plot Building:
* Functional Method
    * With the functional method, you build plots by calling the plotting function on a variable or a set of variables.
* Object-Oriented Method:
    * With object-oriented plotting, you build a plot by first generating a blank figure object and then populating that object with plot and plot element.

#### Popular Data Visualization Libraries in Python
* Matplotlib
* Seaborn

In the [Code Demonstration](./code/04-01.ipynb), we will use _Functional Method_ with _Matplotlib_