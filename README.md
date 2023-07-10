# pandas-challenge
This is Module 4 Challenge - pandas challenge

In this challenge we were tasked with manipulating Pandas DataFrames to analyze school and standardized test data.

CODE SOURCES WITHIN REPO:
https://stackoverflow.com/questions/43096522/remove-dollar-sign-from-entire-python-pandas-dataframe
    Use `pd.cut` to categorize spending based on the bins.
    school_spending_df["Spending Ranges (Per Student)"] = pd.cut(school_spending_df['Per Student Budget'].replace({'\$':''}, regex = True).astype(float), 
                                                             spending_bins, labels=labels)
school_spending_df.head()

I was having difficulty usuing pd.cut() because the 'Person budget' column held a string. Comparing the string to int resulted in Type Error repetedly. I needed to convert it to a float first, so I had to remove the leading dollar sign. This code helped me find out how.



