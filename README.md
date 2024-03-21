
# Analysis for a New Business City

## Table of Content
  - [Project Overview](#project-overview)
    
  - [Data Source](#data-source)
    
  - [Tools](#tools)
    
  - [Data Preparation](data-preparation)
    
  - [Exploratory Data Analysis](exploratory-data-analysis)
    
  - [Data Analysis](data-analysis)
    
  - [Results and Findings](results-and-findings)
    
  - [Recommendations](recommendations)
    
  - [Reference(s)](reference(s))

## Project Overview
In this data analysis project, insights are provided to the client on the best cities to host his new business. This project is carried out using my BigQuery Sandbox account. While carrying out this project, I ensure that I work closely with the client's criteria for a winning new site. The requirments includes:
- Average temperature,
- Average commute time,
- Happiness Ranking of the cities.

### Data Source
The data was readily available on BigQuery as city_data and added to my project 

### Tools
- Database - Data access and inspection
- SQL - Data Analysis

### Data Preparation
In the initial data preparation phase, I downloaded the dataset from bigquery and observed it carfully for errors, duplicates and missing values. However, this dataset was already precleaned and so does not require any cleaning. So following the instructions of the tutor, I delved into deriving insightes from the data using the clients criteia.

### Exploratory Data Analyis
The Exploratory Data Analysis involves asking questions to discover cities from the data that meet specific conditions, such as:

- Which city has an average temperature between 45°c and 65°c?
- What city has an average commute time of less than 60?
- what city has a happiness ranking of between 1 and 15?

### Data Analysis
Below are some queries I used for the analysis:

--- What city has an average temperature between 45°c and 65°c?

```SQL
SELECT  city_name,
        avg_temp,
        avg_commute,
        happiness_ranking

From `rugged-sunbeam-415914.city_data.cities`

WHERE avg_temp BETWEEN 45 AND 65
```

--- What city has a commute time of less than 60 minutes?

```SQL
SELECT city_name,
        avg_temp,
        avg_commute,
        happiness_ranking

From `rugged-sunbeam-415914.city_data.cities`

WHERE avg_temp BETWEEN 45 AND 65
      AND avg_commute <=60
```

--- Which country has a happiness ranking of 15 and less?

```SQL
SELECT  city_name,
        avg_temp,
        avg_commute,
        happiness_ranking

From `rugged-sunbeam-415914.city_data.cities`

WHERE avg_temp BETWEEN 45 AND 65
      AND avg_commute <=60
      AND happiness_ranking <=15
```

### Results and Findings
The results are summarized thus:
1. 11 Cities met the avearge temperature of 45 and 65.
2. 8 Cities met the average tempreture requirement and also the average commute of less than 60.
3. By including the criteria of happiness ranking of 15 and lower, only 2 cities were discovered to be suitable for the clients project.

![chart showing the 2 suitable cities and the criteria met](https://github.com/Taciann62/SQL_PROJECTS_DOCUMENTATION/assets/132772773/af31070c-116f-492c-a2b8-0dd160f7e275)
### Recommendations
Based on the analysis, I recommend that the client:
  - Decides between the two most suitable cities, which one would best generate revenue and promise good amount of  customers to sustain the business at the site.
  - Look into the customer retention rate, income revenue and business survival rate of competitor businesses in each city.
  - Utilize social media trends to boost customer interest in the city of choice
  - Ensure the city requires his services and above all, look into the rules, regulations among other legal business policies governing each city before setting his business there.

### Refrence(s)
- Google Data Analytics Certificate Course

#### Thank You 😊
