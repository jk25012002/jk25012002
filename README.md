import pandas as pd

# Read the Excel files into DataFrames
df1 = pd.read_excel(r"F:\PROJECT\makran\data\makran-seismic\makranblock(60-63).xlsx")
df2 = pd.read_excel(r"F:\PROJECT\makran\data\makran-seismic\mw.xlsx")

# Get the first column from both files
col1 = df1.columns[0]
col2 = df2.columns[0]

# Compare the first columns
if col1 == col2:
    # Check if the columns are equal
    if df1[col1].equals(df2[col2]):
        print("yes")
    else:
        print("no")

        # Optional: Print the differences row by row
        diff = df1[col1] != df2[col2]
        diff_rows = diff[diff].index.tolist()
        print("des")
        for row in diff_rows:
            print(do)
else:
    print("The first columns in the two files have different names.")

