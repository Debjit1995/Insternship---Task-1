# Internship---Task-1
Data cleaning of Netflix dataset using python

Steps in brief -

1) First, I imported the library Pandas
2) Loaded the dataset
df = pd.read_csv("netflix_titles.csv")
3)Then I cleaned the dataset by handling missing values, removing duplicate rows, standardize country names, renaming columnn headers to lowercase and removed spaces.
4)The column date_added was in text format. We convert it to a proper date
5) I made sure release_year is treated as a number :
    df['release_year'] = pd.to_numeric(df['release_year'], errors='coerce')
6) But when  checked after cleaning, the missing values were still there, so I handled it differently with the help of fillna() and dropna().
   I ran few codes so that,
   If a row has no director listed, it fills it with the word 'Unknown'.
   Filled empty cast entries with 'Not Specified'.
   Removed rows where the date_added column is missing.
   Filled missing ratings with 'Not Rated'.
   Filled missing duration values with 'Not Specified'.
7) At last, I saved the cleaned data to a new CSV file
