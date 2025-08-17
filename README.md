# Analysis of the AI & Data Science Job Market

### Project Objective

The goal of this notebook is to perform a comprehensive analysis of a dataset containing job listings related to the fields of Artificial Intelligence and Data Science. By cleaning, exploring, and visualizing the data, we aim to uncover key insights into the current job market landscape.

Specifically, this analysis seeks to answer the following questions:
*   What are the most common job roles, and how are they distributed?
*   What is the typical distribution of company ratings for these roles?
*   Which companies are the most active recruiters in this space?
*   What are the most in-demand technical skills mentioned in job descriptions?

### The Dataset

The data for this project is sourced from a CSV file (`jobs_dataset.csv`) containing scraped job listings. The key features we will be leveraging include:
*   `positionName`: The raw job title.
*   `company`: The name of the hiring company.
*   `rating`: The company's rating.
*   `job_description`: The full text of the job posting.
*   `job_type`: The employment type (e.g., Full-time, Internship).

### Analysis Workflow

Our approach will follow a structured data analysis process:

1.  **Data Loading and Preprocessing:**
    *   Import all necessary libraries for data manipulation, visualization, and text analysis.
    *   Load the dataset from the CSV file.
    *   Perform initial data cleaning by dropping irrelevant columns and renaming others for clarity and consistency.

2.  **Feature Engineering:**
    *   Create a new `role_category` column by defining a function that maps diverse job titles into standardized categories (e.g., 'Data Scientist', 'Machine Learning', 'Data Engineer'). This is crucial for meaningful aggregation and analysis.

3.  **Exploratory Data Analysis (EDA):**
    *   Analyze and visualize the distribution of the newly created `role_category`.
    *   Investigate the statistical summary and distribution of company `rating` using histograms and boxplots.
    *   Examine relationships between different features, such as the average company rating per `job_type`.
    *   Identify the top 10 companies with the most job listings for AI/Data roles.

4.  **Text Mining & Skill Extraction:**
    *   Define a comprehensive, categorized list of key technical skills (languages, libraries, platforms, etc.).
    *   Develop a function to parse the `job_description` text and extract any matching skills from our predefined list.
    *   Count the frequency of each skill across all job listings to determine which are most in-demand.

5.  **Visualization:**
    *   Use a variety of plots (bar charts, histograms) to communicate findings from the EDA.
    *   Generate a **Word Cloud** from the extracted skills data to provide a compelling and intuitive visual summary of the most sought-after technical proficiencies in the job market.
