---
title: Data Analytics (Python)
categories:
  - big-data
tags:
  - null
toc: true
date: 2016-09-21 23:05:16
---

[Home - PyData](https://pydata.org/)

[An Overview of Python’s Datatable package – Towards Data Science](https://towardsdatascience.com/an-overview-of-pythons-datatable-package-5d3a97394ee9)
[Pyodide: Bringing the scientific Python stack to the browser - Mozilla Hacks - the Web developer blog](https://hacks.mozilla.org/2019/04/pyodide-bringing-the-scientific-python-stack-to-the-browser/)

[Python Data Analysis Library](https://pandas.pydata.org/)(`pandas`) massage data into a tabular state so it can be modeled
[Spyder - Documentation](https://pythonhosted.org/spyder/#) Scientific PYthon Development EnviRonment

[5 essential Python programming tools for data science—now updated](https://www.infoworld.com/article/3233250/python/5-essential-python-tools-for-data-sciencenow-improved.html)
[Weekend Reading: Python | Linux Journal](https://www.linuxjournal.com/content/weekend-reading-using-python-science-and-machine-learning) science and ML

[Python Data Science Handbook | Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/index.html)
[pydata/pydata-cookbook: PyData Cookbook Project](https://github.com/pydata/pydata-cookbook)

I do not recommend Anaconda, it installs a separate Python and messes up with your distro's Python and Pip.
Try Docker image for [Intel® Distribution for Python* | Intel® Software](https://software.intel.com/en-us/distribution-for-python)

## NumPy

[NumPy — NumPy](http://www.numpy.org/)
[NumPy - Wikiwand](https://www.wikiwand.com/en/NumPy)
[NumPy User Guide — NumPy Manual](https://docs.scipy.org/doc/numpy/user/index.html)

[A Visual Intro to NumPy and Data Representation – Jay Alammar – Visualizing machine learning one concept at a time](https://jalammar.github.io/visual-numpy/)
[Numpy Guide for People In a Hurry – Towards Data Science](https://towardsdatascience.com/numpy-guide-for-people-in-a-hurry-22232699259f)
[Look Ma, No For-Loops: Array Programming With NumPy – Real Python](https://realpython.com/numpy-array-programming/)
[Python Numpy Array Tutorial (article) - DataCamp](https://www.datacamp.com/community/tutorials/python-numpy-tutorial)

[Boosting numpy: Why BLAS Matters - Weblog](https://markus-beuckelmann.de/blog/boosting-numpy-blas.html)

## SciPy

[SciPy.org — SciPy.org](https://www.scipy.org/)
[SciPy - Wikiwand](https://www.wikiwand.com/en/SciPy)

[Numpy and Scipy Documentation — Numpy and Scipy documentation](https://docs.scipy.org/doc/)

## Pandas

[Python Data Analysis Library — pandas: Python Data Analysis Library](http://pandas.pydata.org/)
[API Reference — pandas documentation](https://pandas.pydata.org/pandas-docs/stable/api.html)

[Idiomatic Pandas: Tricks & Features You May Not Know – Real Python](https://realpython.com/courses/idiomatic-pandas-tricks-features-you-may-not-know/?__s=9yjm1swp7s426a4xisnd)
[pandas-datareader — pandas-datareader documentation](https://pydata.github.io/pandas-datareader/stable/index.html)

### Tutorials

[Intro to Data Structures — pandas documentation](https://pandas.pydata.org/pandas-docs/stable/dsintro.html)
Series:
1-D array with `index` as axis label
equivalent to a `dict` with key as index
mostly compatible to NumPy's `ndarray`

DataFrame:
2-D labeled data, like table or `dict` of series with key as columns
`index` is row labels , `columns` is column (field) labels
not intended to work as 2-D `ndarray`

[Python Pandas Tutorial](https://www.tutorialspoint.com/python_pandas/index.htm)
[Examining Data Using Pandas | Linux Journal](https://www.linuxjournal.com/content/examining-data-using-pandas)
[Introduction to Pandas | Machine Learning, Deep Learning, and Computer Vision](https://www.ritchieng.com/pandas-introduction/)
[Fast, Flexible, Easy and Intuitive: How to Speed Up Your Pandas Projects – Real Python](https://realpython.com/fast-flexible-pandas/)

[Quick and Dirty Data Analysis with Pandas](https://machinelearningmastery.com/quick-and-dirty-data-analysis-with-pandas/)
[Python Pandas DataFrame: load, edit, view data | Shane Lynn](https://www.shanelynn.ie/using-pandas-dataframe-creating-editing-viewing-data-in-python/)

[Pandas: The Swiss Army Knife for Your Data, Part 1](https://code.tutsplus.com/tutorials/pandas-the-swiss-army-knife-for-your-data-part-1--cms-29523)
[Pandas: The Swiss Army Knife for Your Data, Part 2](https://code.tutsplus.com/tutorials/pandas-the-swiss-army-knife-for-your-data-part-2--cms-29524)

[Video series: Easier data analysis in Python using the pandas library](https://www.dataschool.io/easier-data-analysis-with-pandas/)

[Intro to pandas data structures](http://gregreda.com/2013/10/26/intro-to-pandas-data-structures/)
[Working with DataFrames](http://www.gregreda.com/2013/10/26/working-with-pandas-dataframes/)
[Using pandas on the MovieLens dataset](http://www.gregreda.com/2013/10/26/using-pandas-on-the-movielens-dataset/)

[datas-frame – Modern Pandas (Part 1)](https://tomaugspurger.github.io/modern-1-intro.html)
[datas-frame – Modern Pandas (Part 2): Method Chaining](https://tomaugspurger.github.io/method-chaining)
[datas-frame – Modern Panadas (Part 3): Indexes](https://tomaugspurger.github.io/modern-3-indexes)
[datas-frame – Modern Pandas (Part 4): Performance](https://tomaugspurger.github.io/modern-4-performance)
[datas-frame – Modern Pandas (Part 8): Scaling](https://tomaugspurger.github.io/modern-8-scaling)
[datas-frame – Modern Pandas (Part 6): Visualization](https://tomaugspurger.github.io/modern-6-visualization)
[datas-frame – Modern Pandas (Part 7): Timeseries](https://tomaugspurger.github.io/modern-7-timeseries)
[datas-frame – Modern Pandas (Part 8): Scaling](https://tomaugspurger.github.io/modern-8-scaling)

[Pandas Tutorial 1: Pandas Basics (read_csv, DataFrame, Data Selection)](https://data36.com/pandas-tutorial-1-basics-reading-data-files-dataframes-data-selection/)
[Pandas Tutorial 2: Aggregation and Grouping](https://data36.com/pandas-tutorial-2-aggregation-and-grouping/)
[Pandas Tutorial 3: Important Data Formatting Methods (merge, sort, reset_index, fillna)](https://data36.com/pandas-tutorial-3-important-data-formatting-methods-merge-sort-reset_index-fillna/)

[Seven Clean Steps To Reshape Your Data With Pandas Or How I Use Python Where Excel Fails](https://towardsdatascience.com/seven-clean-steps-to-reshape-your-data-with-pandas-or-how-i-use-python-where-excel-fails-62061f86ef9c)

### Tips and Tricks

[Python Pandas: Tricks & Features You May Not Know – Real Python](https://realpython.com/python-pandas-tricks/)
[Pandas tips and tricks – Towards Data Science](https://towardsdatascience.com/pandas-tips-and-tricks-33bcc8a40bb9)

[Efficiently Store Pandas DataFrames](http://matthewrocklin.com/blog/work/2015/03/16/Fast-Serialization)

```python
with pd.option_context('display.max_rows', None, 'display.max_columns', None):
    print(df)
```

[python - Pretty-print an entire Pandas Series / DataFrame - Stack Overflow](https://stackoverflow.com/questions/19124601/pretty-print-an-entire-pandas-series-dataframe)

### groupby

[groupby — pandas documentation](https://pandas.pydata.org/pandas-docs/stable/api.html#groupby)
[pandas.core.groupby.DataFrameGroupBy.agg — pandas documentation](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.core.groupby.DataFrameGroupBy.agg.html)

[Apply Operations To Groups In Pandas](https://chrisalbon.com/python/data_wrangling/pandas_apply_operations_to_groups/)
[Summarising, Aggregating, and Grouping data in Python Pandas | Shane Lynn](https://www.shanelynn.ie/summarising-aggregation-and-grouping-data-in-python-pandas/amp/)

[ZaxR/pandas_multiindex_tutorial: An in-depth introduction to Pandas' MultiIndexes and practical code snippets](https://github.com/ZaxR/pandas_multiindex_tutorial)

```python
# Group the dataframe by regiment, and for each regiment,
for name, group in df.groupby('regiment'):
    # print the name of the regiment
    print(name)
    # print the data of that regiment
    print(group)
```

### filter

[python - pandas: filter rows of DataFrame with operator chaining - Stack Overflow](https://stackoverflow.com/questions/11869910/pandas-filter-rows-of-dataframe-with-operator-chaining)
[How To Filter Pandas Dataframe By Values of Column? — Python, R, and Linux Tips](https://cmdlinetips.com/2018/02/how-to-subset-pandas-dataframe-based-on-values-of-a-column/)

`df.field == value` creates a list of matching indices
so `df[df.field == value]` is a filtered list of data with those indices

Or use:
[pandas.DataFrame.query — pandas documentation](http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.query.html)

### Pivot Tables

[Pivot Tables | Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/03.09-pivot-tables.html)

### Input/Output

[IO Tools (Text, CSV, HDF5, …) — pandas documentation](http://pandas.pydata.org/pandas-docs/stable/io.html)

For reading: `xlrd` (XLS)
For writing: `openpyxl`/`xlsxwriter` (XLS), `PyTables` (HDF5)

[Working with Python Pandas and XlsxWriter — XlsxWriter Documentation](https://xlsxwriter.readthedocs.io/working_with_pandas.html)
[Example: Pandas Excel output with a line chart — XlsxWriter Documentation](https://xlsxwriter.readthedocs.io/example_pandas_chart_line.html)

[Python Excel](http://www.python-excel.org/)
[openpyxl - A Python library to read/write Excel 2010 xlsx/xlsm files — openpyxl documentation](https://openpyxl.readthedocs.io/en/stable/)
[Chapter 12 - Automate the Boring Stuff with Python](https://automatetheboringstuff.com/chapter12/)

[Three Ways of Storing and Accessing Lots of Images in Python – Real Python](https://realpython.com/storing-images-in-python/)

### #perfmatters

[Enhancing Performance — pandas documentation](https://pandas.pydata.org/pandas-docs/stable/enhancingperf.html)

[Parallel Pandas – KRSTN](https://krstn.eu/paralell_Pandas/) `concurrent.futures.ProcessPoolExecutor` faster than `multiprocessing.Pool`
[Parallelize Pandas map() and apply() while accounting for future records – Adeel's Corner](http://blog.adeel.io/2017/02/11/parallelize-pandas-map-and-apply-while-accounting-for-future-records/)
