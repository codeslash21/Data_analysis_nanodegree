### Data Analysis:
We organized the data analysis process into five steps:
* **1. Ask questions:** Either you're given data and ask questions based on it, or you ask questions first and gather data based on that later.
* **2. Wrangle data:** You get the data you need in a form you can work with in three steps: gather, assess, clean. You gather the data you need to answer your questions, assess your data to identify any problems in your data’s quality or structure, and clean your data by modifying, replacing, or removing data to ensure that your dataset is of the highest quality and as well-structured as possible.
* **3. Perform EDA (Exploratory Data Analysis):** You explore and then augment your data to maximize the potential of your analyses, visualizations, and models. Exploring involves finding patterns in your data, visualizing relationships in your data, and building intuition about what you’re working with. After exploring, you can do things like remove outliers and create better features from your data, also known as feature engineering.
* **4. Draw conclusions (or even make predictions):** This step is typically approached with machine learning or inferential statistics.
* **5. Communicate your results:** You often need to justify and convey meaning in the insights you’ve found. Or, if your end goal is to build a system, you usually need to share what you’ve built, explain how you reached design decisions, and report how well it performs.

### Package:
A package is a collection of modules or python files that we can import into our code. Using a short alias can help to keep your code concise and clean. Example `import numpy as np`.

### CSV:
csv stands for Comma Seperated Values. Its a text file. One can read `csv` file using `pandas` as following - 
```
import pandas as pd
df = pd.read_csv('student_scores.csv')
```
There are various optins for `read_csv()` like `sep=":"` or `header=none` or `header=2` etc.
`read_csv()` loads the data into the dataframe.

### Plotting:
`seaborn` is a library to make the plot little nicer. The code as follows -
```
%pylab inline # To plot in the notebook
import seaborn as sns
```
`sns.set_style()` To set style for the background.
