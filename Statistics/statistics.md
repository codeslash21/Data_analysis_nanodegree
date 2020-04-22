# Statistics
There are two types of statistics. These are - 
* `Descriptive statistics` is about describing our collected data.
* `Inferential Statistics` is about using our collected data to draw conclusions to a larger population.
**Some terms:**
> `Population` - our entire group of interest.
> `Parameter` - numeric summary about a population
> `Sample` - subset of the population
> `Statistic` numeric summary about a sample

## Datatypes:
There are two types of data, Quantitative and Categorical.
* **Quantitative** data takes on numeric values that allow us to perform mathematical operations (like the number of dogs).We can think of quantitative data as being either continuous or discrete.

   * **Continuous data** can be split into smaller and smaller units, and still a smaller unit exists. An example of this is the age of the dog - we can measure the units of the age in years, months, days, hours, seconds, but there are still smaller units that could be associated with the age.

   * **Discrete data** only takes on countable values. The number of dogs we interact with is an example of a discrete data type.

* **Categorical** are used to label a group or set of items (like dog breeds - Collies, Labs, Poodles, etc.).We can divide categorical data further into two types: Ordinal and Nominal.

    * **Categorical Ordinal** data take on a ranked ordering (like a ranked interaction on a scale from Very Poor to Very Good with the dogs).

    * **Categorical Nominal** data do not have an order or ranking (like the breeds of the dog).

### Analyzing Quantitative Data
*  **Four Aspects for Quantitative Data**:
   There are four main aspects to analyzing Quantitative data.

   - Measures of `Center`
   - Measures of `Spread`
   - The `Shape` of the data.
   - `Outliers`
   
 * **Measures of Center**
There are three measures of center:

   - Mean
   - Median
   - Mode
   
   <br></br>
   > `MEAN` is the average of the values in the dataset.
   `MEDIAN` is the middle most value of the sorted dataset.
   `MODE` is the value with higher frequency in the dataset. If all the values in the dataset share the same frequency then there is no mode. On the other hand if two or more values have the highest frequency then there are many modes.
   
   
 * **Measures of Spread** are used to provide us an idea of how spread out our data are from one another. Common measures of spread include:

    - Range
    - Interquartile Range (IQR)
    - Standard Deviation
    - Variance 
    > `Range` is the value of (max-min) of the dataset.
    > `IQR` or Inter Quartile Range is (Q3 -Q1). Q2 is the median of the dataset.
    
 * **The Shape of the data**:
 Plotting `Histogram` one can visualize the shape of the quantitative data.
 
### Analyzing Categorical Data:
Analyzing categorical data has fewer parts to consider. Categorical data is analyzed usually be looking at the counts or proportion of individuals that fall into each group. For example if we were looking at the breeds of the dogs, we would care about how many dogs are of each breed, or what proportion of dogs are of each breed type.

### Histogram:
Histogram is the most popular visual for quantitative data. From a histogram we can quickly identify the shape of our data. The distribution of our data is frequently associated with one of the three shapes:
> 1. Right-skewed - In which histogram shorter bin in the right side and longer bin in the left side.
> 2. Left-skewed - In which histogram shorter bin in the left side and longer bin in right side.
> 3. Symmetric (frequently normally distributed) - In which histogram right side mirrors the left side.

**NOTE:**
* For `Right-skewed` distribution `Mean>Mode`.
* For `Left-skewed` distribution `Mean<Mode`.
* For symmetric distribution `Mean=Median=Mode`. Example - bell curve.
* Histogram is used for depicting quantative data not the categorical data.
* If `Mean=Median` then that always not be Normal distribution that can be symmetric distribution.

### Box Plot:
In descriptive statistics, a box plot or boxplot is a method for graphically depicting groups of numerical data through their quartiles. Box plots may also have lines extending from the boxes indicating variability outside the upper and lower quartiles, hence the terms box-and-whisker plot and box-and-whisker diagram.
*  The measures of center and spread we can determine from a Box Plot.
### Outliers:
Below are my guidelines for working with any column (random variable) in your dataset.
>1. Plot your data to identify if you have outliers.
>2. Handle outliers accordingly via the methods above.
>3. If no outliers and your data follow a normal distribution - use the mean and standard deviation to describe your dataset, and report that the data are normally distributed.
>4. If you have skewed data or outliers, use the five number summary to summarize your data and report the outliers. Five numbers are min, max, Q1, Q2, Q3.
Outliers have a larger influence on measures like the mean than on measures like the median. We have to work on outliers on a situation on a situation basis.

### Simpson's Paradox:
Simpson's paradox, which goes by several names, is a phenomenon in probability and statistics, in which a trend appears in several different groups of data but disappears or reverses when these groups are combined.

### NOTE:
* Notation is a common language used to communicate mathematical ideas. Think of notation as a universal language used by academic and industry professionals to convey mathematical ideas.
* Capital Letter is used for random varibles and small letter is used for referencing random variables' values.
* The variance is the average squared difference of each observation from the mean.
* `sd` or `var` is used for comparing which dataset spread out more. We cant measure center by these. If `sd1` > `sd2` - this does not imply that `d1` has more range than `d2`.
* Standard deviation of two datasets may be same despite having different maximums.
