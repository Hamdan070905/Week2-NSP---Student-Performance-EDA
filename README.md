# Week2-NSP---Student-Performance-EDA

1. Import Libraries and Load Dataset

> Essential Python libraries (pandas, numpy, matplotlib.pyplot, and seaborn) are imported to handle data processing and visualization. The dataset country_wise.csv is read into a DataFrame named df.

2. Clean the Data

> The dataset is examined for missing values using .isnull().sum() and data types using .info(). All rows containing missing data are removed with .dropna(). Duplicate rows, if any, are removed using .drop_duplicates() to ensure data quality.

3. Initial Data Exploration

> The structure and summary of the dataset are explored.
               .head() shows the first few records.
               .describe() provides statistical summaries (mean, min, max, etc.).
               .unique() lists all unique country or region names under the 'Country/Region' column.

4. Identify Most Affected Countries

> The data is grouped by 'Country/Region', and the maximum number of confirmed cases per country is calculated using .groupby() and .max(). The top 10 countries are extracted using .sort_values() and .head(10) for focused analysis.

5. Line Chart – Top 10 Countries by Confirmed Cases

> The dataset is sorted by the number of confirmed cases, and the top 10 countries are selected. A line plot is generated using seaborn.lineplot() to visually compare the number of confirmed COVID-19 cases across these countries.

6. Bar Chart – Top 10 Countries by Deaths

> The dataset is sorted by the 'Deaths' column in descending order to find the top 10 countries with the highest death toll. A horizontal bar chart is plotted using seaborn.barplot() to compare these countries visually.

7. Pie Chart – Global Recovered vs Deaths

> The 'Deaths' and 'Recovered' columns are converted to numeric using pd.to_numeric() with errors='coerce' to handle any invalid entries. Rows with NaN in these columns are dropped. The global totals of deaths and recoveries are calculated using .sum(), and a pie chart is plotted to show the proportion of recoveries versus deaths globally.

