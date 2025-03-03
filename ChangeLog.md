# Changelog

## [Unreleased]
### Changes
- Renamed columns to have proper names as when i got the data there was not columns names on the dataset so that make it hard to know what was each columns for.
  ![image alt] ( https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20221351.png?raw=true)
  ### After naming the columns
  ![image alt]( https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20221633.png?raw=true)
  ![image alt](https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20124153.png?raw=true)
- i was trying to change the columns names as they were not displaying a proper name for the columns and i was having issues with this column as 'im getting on borderlands and i will murder you all , as i was tryingg to change it but and the en dof the coulmn there was a space and a coma that i was not adding to this code data = data.rename(columns={'im getting on borderlands and i will murder you all ,' : 'Comments'})

- 
- Checked for missing comments and dropped any missing values to ensure all comments are available for classification.
- Added a pie chart to the notebook to visually represent the distribution of comments categorized as negative, positive, neutral, and irrelevant.
  ### Pie Chart
    ![image alt](https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20124347.png?raw=true)
- Converted `comments` and `emotional` columns into numerical data, as multinomial Naïve Bayes only processes numerical data, requiring string-based sentiment data to be transformed.
      ![image alt](https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20124408.png?raw=true)
  

