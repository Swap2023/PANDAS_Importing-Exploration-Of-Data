# PANDAS_Imporating- Exploration-Of-Data #
import pandas as pd
For Importing The Data 

1. pd.read_csv(“filename”) # From a CSV file

2. pd.read_table(“filename”) # From a delimited text file (like TSV)

3. pd.read_excel(“filename”, sheet_name= ‘Sheet2’) # From an Excel file 

4. pd.read_sql(query, connection_object) # Reads from a SQL table/database

5. pd.read_json(json_string) # Reads from a JSON formatted string, URL or file

6. pd.read_html(url) # Extract all the tables from the given url (List view).

pd.read_html(url)[0]/[1] # Extract the first/second table from the given url (Table view).

7. pd.read_clipboard() # Takes the content you copied and shows the result. 

8. pd.DataFrame(dict) # From a dict, keys for columns names, values for data as lists

9. Insert Image in Jupyter Notebook. 
Convert the Cell to MarkDown > Edit Tab > Insert Image > Run 

10. Insert Audio in Jupyter Notebook. 

from IPython.display import Audio 
file = ‘…file-path..’ 
Audio(data = file, autoplay = False)

11. Insert/Embed a YouTube Video with link
from IPython.display import YouTubeVideo 
YouTubeVideo(“..video..url id…”, height=400, width=400)

12. Insert/Embed a URL
from IPython.display import IFrame 
IFrame("…url…", width=800, height=450) 

13. Insert/Embed a PDF
from IPython.display import IFrame
IFrame("https://arxiv.org/pdf/1406.2661.pdf'", width=800, height=450) 

For Exploring The Data

1. Attributes (Series) - s.values, s.index, s.shape, s.size, s.nbytes, s.dtypes 
 # To see the attributes of a series.

2. s.head( ) / s.tail ( ) - s.head(), s.head(n) , s.tail() , s.tail(n) 
 # To show the top or last elements of the series.

3. s.nunique ( ) - s.nunique( ) # It shows the total no. of unique values in the series. 

4. s.unique ( ) - s.unique( ) # It shows the all unique values of the series.

5. s.value_counts ( ) - s.value_counts( ) # It shows all unique values with their counts in the series. 

 
 If s.value_counts( )[‘value’] – It will show counts of this value only. 
 
 If s.value_counts(normalize=True) – It will show the unique values in percentage.
 
 If s.value_counts(dropna = False) – It will show the Nan also. 
6 s.count( ) - s.count( ) # It shows the total no. of values in the series.

7. s.nlargest ( ) / s.nsmallest ( ) - s.nlargest(4) , s.nsmallest() 

# To show the n largest or n smallest values in descending or ascending order. 

8. s.mean( ), s.median( ), s.mode( ), s.std( ), s.min( ), s.max( ) - 

# It shows the mean , median , mode, std. deviation, minimum value, maximum value of the series.

9. s.skew( ) # It shows the Skewness of the series.

10. s.describe() - s.describe() # It shows the summary statistics (count, mean , median , 

std. deviation, minimum value, maximum value) of the series at once.

11. s.quantile( ) - s.quantile(0.7 ) , s.quantile([0.7, 0.8, 0.3]) 

# It shows the no. from the series where (given) percent of values falls below it.

12. s.axes # It returns the list of the labels of the series.

13. s.empty # It returns Boolean T/F whether the series is empty or not.

14. Attributes (Data Frame) - df.shape, df.size, df.index, df.columns, df.dtypes, df.values 

 # To show the attributes of a DF. 
15. df.head( ) / df.tail ( ) - df.head(), df.head(n) , df.tail() , df.tail(n) 

 # To show the top or last rows of the dataframe. 

16. df.nunique ( ) - df.nunique( ) # It shows the total no. of unique values in each column. 

17. df[‘Col_name’].value_counts ( ) - df.Col_name.value_counts( ) , sns.countplot(df.Col_name) 

 # It shows all unique values with their counts in the column. 
 
 If df.Col_name.value_counts( )[‘Delhi ’] – It will show counts of Delhi only. 
 
 If df.Col_name.value_counts(normalize=True) – It will show the unique values in percentage. 
 
 If df.Col_name.value_counts(dropna = False) – It will show the Nan also.
 
 df.Col_name.value_counts( ).plot(kind= ‘bar’) # To draw a graph of unique values of column. 
 
 df.Col_name.value_counts( ).sort_index( ) # To sort with index after value counts. 
 
 df.groupby(‘Col’)[‘Col’].count( ).sort_values(ascending=False) – Alternate method of value counts. 
18. df.count( ) - df.count( ), np.count_nonzero(df) 
 
 # It counts the no. of non-null/null values of each column.

19. df.count(axis=1) # It counts the no. of non-null/null values of each row.

20. df.axes # It returns a list of row axis & column axis.

21. df.empty # It returns Boolean T/F whether the dataframe is empty or not.

22. df.abs( ) # It shows the absolute values.

23. df.info( ) - df.info( ) # It shows indexes, columns, data-types of each column, memory at once.

df.info(memory_usage = ‘deep’) # It shows the info with actual memory size.

24. df.sum( ) - df.sum( ), df.values.sum( ) # Shows sum of each numerical columns. 

25. df.sum(axis=1) # Shows sum of each row.

26. df.prod( ) , df.prod(1) # Show the product of each numeric column & row. 

27. df.cumsum( ) , df.cumsum(1) # Shows cumulative sum of each numerical columns & rows.

28. df.cumprod( ) , df.cumprod(1) # Show the cumulative product of each numeric column & row. 

29. df.mean( ) - df.mean( ), df.values.mean( ) # Shows mean of each numerical columns.

30. df.mean(axis=1) # Shows mean of all each row.

31. df.std( ) - df.std( ) df.values.std( ) # Shows std of each numerical columns.

32. df.std(axis=1) # Shows std of each row.

33. df.var( ) - df.var( ) , df.values.var( ) # Shows variance of each numerical columns.

34. df.var(axis=1) # Shows variance of each row.

35. df.median( ) - df.median( ) , np.median(df) # Shows median of each numerical columns.

36. df.median(axis=1) # Shows median of each row.

37. df.mode( ) , df.mode(axis=1) # Shows mode of each numeric column & row.

38. df.skew( ) , df.skew(axis=1) # Shows the Skewness of each numeric column & row.

39. df.describe( ) - # It produces the summary statistics of all numeric columns. It checks extreme 
outliers and large deviations etc.

40. df.describe( ) - # For categorical dataframe, it will show a simple summary of unique values & 

most frequently occurring values.

41. df.describe(include= ‘number’) # For numeric columns.

42. df.describe(include= ‘object’) # For categorical columns.

43. df.describe(include= ‘all’) # To get summaries of all variables.

44. df.describe( ).loc[‘min’ : ‘max’ , ‘Col_1’ : ‘Col_4’ ] # To see only selected results
