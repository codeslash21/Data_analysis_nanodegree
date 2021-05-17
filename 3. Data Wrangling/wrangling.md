
# Data Wrangling:
Data wrangling is a core skill that everyone who works with data should be familiar with since so much of the world's data isn't clean.
Data wrangling process is consist of three steps 

- Gather Data
- Assess Data 
- Clean Data

## Gather Data:

  - Scalability: Imagine you had a thousand files to download on a thousand different web pages, instead of just one. It'd take an eternity to point and click a thousand times. You can do the same with a few lines of code.

  - Reproducibility: Someone, whether it's you or another person, is likely going to want to run your analysis later, so make downloading the dataset or datasets as easy on that person as possible. Reproducibility is also one of the main principles of the scientific method. You want to be able to prove to people that your analysis, visualization, etc. is legitimate. People need to know that given your data, your computational environment, your code, etc., that they can reproduce your results!
  
## Assess Data:
We consider two condition in Assess Data process -

- Quality
- Tidiness

### Quality of Data:
Data quality is a perception or an assessment of data's fitness to serve its purpose in a given context. Low quality data is often termed as dirty data. Common data quality issues include -
  
  - Missing Data
  - Invalid Data
  - Inaccurate data, like Jane actually being 58 inches tall, not 55 inches tall.
  - Inconsistent data, like using different units for height (inches and centimetres).
  
  
### Tidiness:
Untidy data is commonly referred to as "messy" data. Messy data has issues with its structure. A dataset is messy or tidy depending on how rows, columns, and tables are matched up with observations, variables, and types. In tidy data:

- Each variable forms a column.
- Each observation forms a row.
- Each type of observational unit forms a table.

</br>


![](../Images/oblstsm-imgur.gif)

### Types of Assessment:
There are two types of assessment -

- **Visual assessment** is simple. Open your data in your favorite software application (Google Sheets, Excel, a text editor, etc.) and scroll through it, looking for quality and tidiness issues.

- **Programmatic assessment** tends to be more efficient than visual assessment. One simple example of a programmatic assessment is pandas' info method, which gives us the basic info of your DataFrame—like number of entries, number of columns, the types of each column, whether there are missing values, and more.


## Data Cleaning:
The programmatic data cleaning process:

- **Defining** means defining a data cleaning plan in writing, where we turn our assessments into defined cleaning tasks. This plan will also serve as an instruction list so others (or us in the future) can look at our work and reproduce it.

- **Coding** means translating these definitions to code and executing that code.

- **Testing** means testing our dataset, often using code, to make sure our cleaning operations worked.


## Wrangle VS EDA:

`EDA`: an analysis approach that focuses on identifying general patterns in the data, and identifying outliers and features of the data that might not have been anticipated.

- **Data wrangling** is about gathering the right pieces of data, assessing your data's quality and structure, then modifying your data to make it clean. But the assessments you make and convert to cleaning operations won't make your analysis, viz, or model better, though. The goal is to just make them possible, i.e., functional.

- **EDA** is about exploring your data to later augment it to maximize the potential of our analyses, visualizations, and models. When exploring, simple visualizations are often used to summarize your data's main characteristics. From there you can do things like remove outliers and create new and more descriptive features from existing data, also known as feature engineering. Or detect and remove outliers so your model's fit is better.

## Wrangle VS ETL:

[Documentation](https://tdwi.org/articles/2017/02/10/data-wrangling-and-etl-differences.aspx)

ETL(Extract Transform Load) differs from data wrangling in three main ways:

- The users are different
- The data is different
- The use cases are different


## Flat File:

Flat files contain tabular data in plain text format with one data record per line and each record or line having one or more fields. These fields are separated by delimiters, like commas, tabs, or colons.

**Advantages:**
Advantages of flat files include:

  - They're text files and therefore human readable.
  - Lightweight.
  - Simple to understand.
  - Software that can read/write text files is ubiquitous, like text editors.
  - Great for small datasets.

**Disadvantages:**
Disadvantages of flat files, in comparison to relational databases, for example, include:

  - Lack of standards.
  - Data redundancy.
  - Sharing data can be cumbersome.
  - Not great for large datasets (see "When does small become large?" in the Cornell link in More Information).

