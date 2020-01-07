Q1. You have a DataFrame df with a column 'A' of integers. For example:

df = pd.DataFrame({'A': [1, 2, 2, 3, 4, 5, 5, 5, 6, 7, 7]})

How do you filter out rows which contain the same integer as the row immediately above?


Q2. A DataFrame has a column of groups 'grps' and and column of numbers 'vals'. For example:

df = pd.DataFrame({'grps': list('aaabbcaabcccbbc'), 
                   'vals': [12,345,3,1,45,14,4,52,54,23,235,21,57,3,87]})
For each group, find the sum of the three greatest values.


Q3. Given a DataFrame of numeric values, say

df = pd.DataFrame(np.random.random(size=(5, 3))) # a 5x3 frame of float values

how do you subtract the row mean from each element in the row?


Q4. A DataFrame has two integer columns 'A' and 'B'. The values in 'A' are between 1 and 100 (inclusive). 

For each group of 10 consecutive integers in 'A' (i.e. (0, 10], (10, 20], ...), 

calculate the sum of the corresponding values in column 'B'.


Q5. Consider a DataFrame df where there is an integer column 'X':

df = pd.DataFrame({'X': [7, 2, 0, 3, 4, 2, 5, 0, 3, 4]})

For each value, count the difference back to the previous zero (or the start of the Series, 

whichever is closer). These values should therefore be [1, 2, 0, 1, 2, 3, 4, 0, 1, 2]. 

Make this a new column 'Y'.