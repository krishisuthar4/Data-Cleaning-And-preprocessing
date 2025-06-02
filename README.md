# Data-Cleaning-And-preprocessing
# Movie and TV Titles Dataset Cleaning

This project focuses on cleaning a dataset of movie and TV titles using Python and pandas.

## Dataset Overview
- 5,850 entries
- 15 columns including title, type, release year, genres, and ratings

## Tasks Performed
- Loaded CSV using pandas
- Checked dataset dimensions and structure
- Identified and handled missing values
- Removed duplicates
- Converted text columns to lowercase and removed unwanted characters
- Renamed columns for consistency
- Converted data types where needed

## Sample Operations
```python
df['genres'] = df['genres'].str.lower().str.replace("[\[\]']", '', regex=True).str.strip()
df['imdb_score'].fillna(df['imdb_score'].mean(), inplace=True)
