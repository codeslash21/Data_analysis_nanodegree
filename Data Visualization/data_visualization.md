
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

### NOTE:
- Visuals can be bad if they:
  - Don't convey the desired message.
  - Are misleading.
  
- **DataInk Ratio:**
The data-ink ratio, credited to Edward Tufte, is directly related to the idea of chart junk. The more of the ink in your visual that is related to conveying the message in the data, the better.
Limiting chart junk increases the data-ink ratio.

- **Lie factor** depicts the degree to which a visualization distorts or misrepresents the data values being plotted. It is calculated in the following way:
lie factor= (Δvisual/visual _start) / (Δdata/data _start)


