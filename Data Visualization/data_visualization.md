
# Data Visualization

### Summary Statistics vs. Visualizations:
Summary statistics like the mean and standard deviation can be great for attempting to quickly understand aspects of a dataset, but they can also be misleading if you make too many assumptions about how the data distribution looks.


## Exploratory vs. Explanatory Analyses:

There are two main reasons for creating visuals using data:

- **Exploratory analysis** is done when you are searching for insights. These visualizations don't need to be perfect. You are using plots to find insights, but they don't need to be aesthetically appealing. You are the consumer of these plots, and you need to be able to find the answer to your questions from these plots.

- **Explanatory analysis** is done when you are providing your results for others. These visualizations need to provide you the emphasis necessary to convey your message. They should be accurate, insightful, and visually appealing.

### The five steps of the data analysis process:
- Extract - Obtain the data from a spreadsheet, SQL, the web, etc.
- Clean - Here we could use exploratory visuals.
- Explore - Here we use exploratory visuals.
- Analyze - Here we might use either exploratory or explanatory visuals.
- Share - Here is where explanatory visuals live.

## Python Data Visualization Libraries:

- **Matplotlib:** a versatile library for visualizations, but it can take some code effort to put together common visualizations.
- **Seaborn:** built on top of matplotlib, adds a number of functions to make common statistical visualizations easier to generate.
- **pandas:** while this library includes some convenient methods for visualizing data that hook into matplotlib, we'll mainly be using it for its main purpose as a general tool for working with data.

All together, these libraries will allow you to visualize data in a balance of productivity and flexibility, for both exploratory as well as explanatory analyses.

## The Four Levels of Measurement:

In order to choose an appropriate plot type or method of analysis for your data, you need to understand the types of data you have. One common method divides the data into four levels of measurement:

**Qualitative or categorical types (non-numeric types)**
- **1. Nominal data:** pure labels without inherent order (no label is intrinsically greater or less than any other)
- **2. Ordinal data:** labels with an intrinsic order or ranking (comparison operations can be made between values, but the magnitude of differences are not be well-defined)

**Quantitative or numeric types**
- **3. Interval data:** numeric values where absolute differences are meaningful (addition and subtraction operations can be made)
- **4. Ratio data:** numeric values where relative differences are meaningful (multiplication and division operations can be made)

All quantitative-type variables also come in one of two varieties: discrete and continuous.

- **Discrete** quantitative variables can only take on a specific set values at some maximum level of precision.
- **Continuous** quantitative variables can (hypothetically) take on values to any level of precision.


## Chart Junk:
Chart junk refers to all visual elements in charts and graphs that are not necessary to comprehend the information represented on the graph or that distract the viewer from this information.

**Examples of chart junk:**

- Heavy grid lines
- Unnecessary text
- Pictures surrounding the visual
- Shading or 3d components
- Ornamented chart axes

## Encoding:
We typically try to use position on the x- and y- axes to encode, or depict the value of variables. If we have more than two variables, however, we have to start considering other visual encodings for the additional variables.

In general, `color` and `shape` are best for categorical variables, while the `size` of marker can assist in adding additional quantitative data.


## Bar Charts:
A bar chart is used to depict the distribution of a categorical variable. In a bar chart, each level of the categorical variable is depicted with a bar, whose height indicates the frequency of data points that take on that level. A basic bar chart of frequencies can be created through the use of seaborn's countplot function:
```
base_color = sb.color_palette()[0]
sb.countplot(data = df, x = 'cat_var', color = base_color)
```

## Pie Charts:
A pie chart is a common univariate plot type that is used to depict relative frequencies for levels of a categorical variable. Frequencies in a pie chart are depicted as wedges drawn on a circle: the larger the angle or area, the more common the categorical value taken. You can create a pie chart with matplotlib's `pie` function. 
```
# code for the pie chart seen above
sorted_counts = df['cat_var'].value_counts()
plt.pie(sorted_counts, labels = sorted_counts.index, startangle = 90,
        counterclock = False);
plt.axis('square')
```
** donut plot:** A sister plot to the pie chart is the donut plot. It's just like a pie chart, except that there's a hole in the center of the plot.
```
sorted_counts = df['cat_var'].value_counts()
plt.pie(sorted_counts, labels = sorted_counts.index, startangle = 90,
        counterclock = False, wedgeprops = {'width' : 0.4});
plt.axis('square')
```

## Heat Maps:
A heat map is a 2-d version of the histogram that can be used as an alternative to a scatterplot. Like a scatterplot, the values of the two numeric variables to be plotted are placed on the plot axes. Similar to a histogram, the plotting area is divided into a grid and the number of points in each grid rectangle is added up. Since there won't be room for bar heights, counts are indicated instead by grid cell color. A heat map can be implemented with Matplotlib's hist2d function.

## Violin Plots:
There are a few ways of plotting the relationship between one quantitative and one qualitative variable, that demonstrate the data at different levels of abstraction. The violin plot is on the lower level of abstraction. For each level of the categorical variable, a distribution of the values on the numeric variable is plotted. The distribution is plotted as a kernel density estimate, something like a smoothed histogram.

### NOTE:
- Visuals can be bad if they:
  - Don't convey the desired message.
  - Are misleading.
  
- **DataInk Ratio:**
The data-ink ratio, credited to Edward Tufte, is directly related to the idea of chart junk. The more of the ink in your visual that is related to conveying the message in the data, the better.
Limiting chart junk increases the data-ink ratio.
`Data-Ink Ratio = (amount of ink used to describe the data) / (amount of ink used to describe everything else)`

- **Lie factor** depicts the degree to which a visualization distorts or misrepresents the data values being plotted. It is calculated in the following way:
lie factor= (Δvisual/visual _start) / (Δdata/data _start)


