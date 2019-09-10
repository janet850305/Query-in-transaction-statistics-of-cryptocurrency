# Query-in-transaction-statistics-of-cryptocurrency

Problem definition

Cryptocurrency is getting hot these year. So John Ceena, an oil tycoon wants to dive into the cryptocurrency market. However, the currencies (幣別), exchanges (交易所), and so many things make John really confused. As a result, he wants to hire you helping him to sort out the large data, and find out the best currency, exchange to put his enormous asset in.

Your job:

Put the data into a format easy for search (for instance, sort the data with multiple keys)

Perform several kinds of search, as explained below.

The database (stored in a data file) to be searched has the following fields:


date: date in the format "yyyymmdd"
currency: Name of the cryptocurrency (with string length less than 100).
exchange: Name of the store where transactions occur (with string length less than 100)
low: Lowest price (with data type of float)
high: Highest price (with data type of float)
cap: value of transactions (with data type of long long int)
Note that in the data file, columns (fields) are separated by tabs '\t', and each entry (of a given date) is terminated by newline '\n'.

You program should support 4 types of commands for querying the database. Again, items in the query input are separated by tab '\t' (in order to avoid a item with a space in it), while items in the output are separated by a single space. These 4 types of commands are listed as follows.

Simple query: Find the data corresponding to the inputs of [date], [currency], and [exchange].
input: query	[date]	[currency]	[exchange]
output: [low] [high] [cap]
[low] & [high] should be float, accurate to the 4th decimal places. Note that you need to use "float" in order to conform to our standard program, which might lose some precision though.
Daily min/max: Find the minimum or maximum on a given date of a given currency.
input:  price	[min/max]	[date]	[currency]
output: [min/max of the currency on that date]
The output should be float, accurate to the 4th decimal places. Note that you need to use "float" in order to conform to our standard program, which might lose some precision though.
Total cap of all currencies, for a given date and a given exchange
input: cap	[date]	[exchange]
output: [total_cap]
The output should be long long int.
End of query
input: end
action: exit the program


Input: query	20130114	Diamond	Tidex
Output: 2.9440 4.6044 24

Input: price	max	20130114	Diamond
Output: 4.6257

Input: cap	20130114	Tidex
Output: 210671

Input: query	20120114	Roger	Jang
Output: none

