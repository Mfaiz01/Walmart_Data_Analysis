# Walmart Data Analysis

## Project Overview

![Project Pipeline](https://github.com/najirh/Walmart_SQL_Python/blob/main/walmart_project-piplelines.png)

This project is an end-to-end data analysis solution that extracts valuable business insights from Walmart's sales data. I utilized Python for data processing and analysis, SQL (MySQL and PostgreSQL) for advanced querying, and structured problem-solving techniques to address key business questions.

---

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Visual Studio Code (VS Code), Python, SQL (MySQL and PostgreSQL)
   - **Goal**: I set up a well-organized development workspace in VS Code and structured project folders to ensure smooth development and data handling.

### 2. Set Up Kaggle API
   - **API Setup**: I obtained my Kaggle API token from [Kaggle](https://www.kaggle.com/) by navigating to my profile settings and downloading the JSON file.
   - **Configure Kaggle**: 
      - I placed the downloaded `kaggle.json` file in my local `.kaggle` folder.
      - Used the command `kaggle datasets download -d <dataset-path>` to directly pull the datasets into my project.

### 3. Download Walmart Sales Data
   - **Data Source**: Using the Kaggle API, I downloaded the Walmart sales datasets from Kaggle.
   - **Dataset Link**: [Walmart Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
   - **Storage**: The data was saved in the `data/` folder for easy access.

### 4. Install Required Libraries and Load Data
   - **Libraries**: I installed the necessary Python libraries using:
     ```bash
     pip install -r requirements.txt
     ```
   - **Loading Data**: The data was loaded into a Pandas DataFrame for initial analysis and data transformations.

### 5. Explore the Data
   - **Goal**: I performed an initial exploration to understand the distribution of data, check column names and types, and identify potential issues.
   - **Analysis**: I used `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 6. Data Cleaning
   - **Remove Duplicates**: I identified and removed any duplicate entries to prevent skewed results.
   - **Handle Missing Values**: I dropped rows or columns with insignificant missing values and filled essential ones.
   - **Fix Data Types**: I ensured all columns had consistent data types, such as converting dates to `datetime` and prices to `float`.
   - **Currency Formatting**: I formatted the currency values using `.replace()` for proper analysis.
   - **Validation**: I verified the cleaned data for consistency and accuracy.

### 7. Feature Engineering
   - **Create New Columns**: I calculated a new `Total Amount` for each transaction by multiplying `unit_price` by `quantity` and added it to the dataset.
   - **Enhance Dataset**: This new calculated field simplified subsequent SQL analysis and aggregation tasks.

### 8. Load Data into MySQL and PostgreSQL
   - **Set Up Connections**: I established connections to both MySQL and PostgreSQL using `sqlalchemy` and uploaded the cleaned data into both databases.
   - **Table Creation**: I automated table creation and data insertion for both MySQL and PostgreSQL using Python SQLAlchemy.
   - **Verification**: I executed initial SQL queries to confirm the successful loading of data.

### 9. SQL Analysis: Complex Queries and Business Problem Solving
   - **Business Problem-Solving**: I wrote and executed complex SQL queries to address key business questions, such as:
     - Analyzing revenue trends across branches and categories.
     - Identifying the best-selling product categories.
     - Analyzing sales performance by time, city, and payment method.
     - Investigating peak sales periods and customer buying patterns.
     - Performing profitability analysis by branch and category.
   - **Documentation**: I kept detailed notes on each query’s objectives, approach, and results.

### 10. Project Publishing and Documentation
   - **Documentation**: I maintained clear and structured documentation of the entire process in Markdown and Jupyter Notebooks.
   - **Project Publishing**: I published the completed project on GitHub, including:
     - The `README.md` file (this document).
     - Jupyter Notebooks (if applicable).
     - SQL query scripts.
     - Data files or instructions on how to access them.

---

## Requirements

- **Python 3.8+**
- **SQL Databases**: MySQL, PostgreSQL
- **Python Libraries**:
  - `pandas`, `numpy`, `sqlalchemy`, `mysql-connector-python`, `psycopg2`
- **Kaggle API Key** (for data downloading)

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repo-url>

2. Install Python libraries:
   ```bash
   pip install -r requirements.txt
   
## Project Structure

```plaintext
|-- data/                     # Raw data and transformed data
|-- sql_queries/              # SQL scripts for analysis and queries
|-- notebooks/                # Jupyter notebooks for Python analysis
|-- README.md                 # Project documentation
|-- requirements.txt          # List of required Python libraries
|-- main.py                   # Main script for loading, cleaning, and processing data
```
---

Results and Insights
This section includes the analysis findings:

Sales Insights: Key categories, branches with the highest sales, and preferred payment methods.

Profitability: Insights into the most profitable product categories and locations.

Customer Behavior: Trends in ratings, payment preferences, and peak shopping hours.

Future Enhancements
Possible future extensions to this project:

Integration with dashboard tools like Power BI or Tableau for interactive data visualizations.

Incorporating additional data sources to enhance the analysis.

Automating the data pipeline for real-time data ingestion and analysis.

License
This project is licensed under the MIT License.

Acknowledgments
Data Source: Kaggle’s Walmart Sales Dataset

Inspiration: Walmart’s business case studies on sales and supply chain optimization.
