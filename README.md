# JSON_exercises

Springboard's Data Science Curriculum: Chapter 5.2

The IPython notebook, sliderule_dsi_json_exercise.ipynb, contains solutions to the JSON exercises provided at the end of Chapter 5.2. These exercises are a test for the student's ability at cleaning JSON data in Python via Pandas dataframes.

The first exercise was to find the 10 countries with most projects. To accomplish this, I use Pandas "groupby" method to group the dataframe by country code and counted the number of projects for each country code. I then use the "nlargest()" method to provide a list of countries with largest number of projects.  

The second exercise was to find the top 10 major project themes (using column 'mjtheme_namecode'). I defined a function 'get_code_count' to search all rows in the 'mjtheme_namecode' column. Each row in the 'mjtheme_namecode' column contained a list of dictionaries which contained the theme codes and names associated with each project. I use nested for-loops to search through the dictionaries in each row. I kept count of the number of codes found in each row with a defaultdict. I sorted the defaultdict by its values to find the top 10 major project themes. 

For the last exercise, some theme codes were missing code names, and the goal was to fill in those missing code names. I created another function "replace_name" to find code name given a code using the "theme_code_name" dictionary. The "replace_name" function was applied to the entire "mjtheme_namecode" column.
