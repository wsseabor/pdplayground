# Pandas cheatsheet

### Basic functionality

Foundational element of pandas package is the DataFrame object. The pandas documentation defines as follows:
>Two-dimensional, size-mutable, potentially heterogeneous tabular data. Data structure also contains labeled axes (rows and columns). Arithmetic operations align on both row and column labels. Can be thought of as a dict-like container for Series objects. The primary pandas data structure.

2-Dimensional data can be output to a dataframe object by variety of methods, whether manually, from 
a dictionary, series, html, etc. Can also take a variety of args to construct a dataframe according to need. See the [Pandas documentation](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html) for further explanation of all args.

### Basic dataframe methods - reading data

Reading data into dataframe via json records

`filePath = usr/example/filepath`

`records = [json.load(line) for line in open(filePath)]`

`frame = DataFrame(records)`


Reading data into df via csv

`headerNames = ['example', 'headers', 'for', 'columns']`

`df = pd.read_table('usr/example/filePath', sep = ::, engine = 'python', header = None, names = headerNames)`


These will be most common, but pandas is also able to read data via excel, sql, html, and more.

### Basic dataframe methods - maniuplating dataframes

After reading in data to a dataframe, there are many inbuilt methods used to manipulate the data

View first ten records:

`df = DataFrame(exampleRecords)`

`df.head(10)`

Similarly for the last ten

`df.tail(10)`







