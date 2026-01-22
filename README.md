# Walmart Data Analysis: End-to-End SQL + Python Project

## Project Overview

This project is an end-to-end data analysis solution designed to extract critical business insights from Walmart sales data. We utilize Python for data processing and analysis, SQL (both MySQL and PostgreSQL) for advanced querying, and structured problem-solving techniques to solve key business questions. The project demonstrates skills in data manipulation, SQL querying, database management, and data pipeline creation.

## Technologies Used

- **Python 3.x**: Core programming language for data processing
- **Pandas & NumPy**: Data manipulation and analysis
- **MySQL**: Relational database for data storage and querying
- **PostgreSQL**: Alternative relational database implementation
- **SQLAlchemy**: Database toolkit and ORM for Python
- **PyMySQL & psycopg2**: Database adapters for MySQL and PostgreSQL
- **Jupyter Notebook**: Interactive development environment
- **Kaggle API**: Dataset acquisition

## Project Files

- `project.ipynb`: Main Jupyter notebook containing the complete data analysis pipeline
- `Walmart.csv`: Original raw dataset
- `walmart_clean_data.csv`: Cleaned and processed dataset
- `MySQL Queries.sql`: MySQL-specific business queries and analysis
- `PSQL Queries.sql`: PostgreSQL-specific business queries and analysis
- `requirements.txt`: Python package dependencies
- `README.md`: Project documentation

---

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Visual Studio Code (VS Code), Python, SQL (MySQL and PostgreSQL)
   - **Goal**: Create a structured workspace within VS Code and organize project folders for smooth development and data handling.

### 2. Set Up Kaggle API
   - **API Setup**: Obtain your Kaggle API token from [Kaggle](https://www.kaggle.com/) by navigating to your profile settings and downloading the JSON file.
   - **Configure Kaggle**: 
      - Place the downloaded `kaggle.json` file in your local `.kaggle` folder.
      - Use the command `kaggle datasets download -d <dataset-path>` to pull datasets directly into your project.

### 3. Download Walmart Sales Data
   - **Data Source**: Use the Kaggle API to download the Walmart sales datasets from Kaggle.
   - **Dataset Link**: [Walmart Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
   - **Storage**: Save the data in the `data/` folder for easy reference and access.

### 4. Install Required Libraries and Load Data
   - **Libraries**: Install necessary Python libraries using:
     ```bash
     pip install pandas numpy sqlalchemy mysql-connector-python psycopg2
     ```
   - **Loading Data**: Read the data into a Pandas DataFrame for initial analysis and transformations.

### 5. Explore the Data
   - **Goal**: Conduct an initial data exploration to understand data distribution, check column names, types, and identify potential issues.
   - **Analysis**: Use functions like `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 6. Data Cleaning
   - **Remove Duplicates**: Identify and remove duplicate entries to avoid skewed results.
   - **Handle Missing Values**: Drop rows or columns with missing values if they are insignificant; fill values where essential.
   - **Fix Data Types**: Ensure all columns have consistent data types (e.g., dates as `datetime`, prices as `float`).
   - **Currency Formatting**: Use `.replace()` to handle and format currency values for analysis.
   - **Validation**: Check for any remaining inconsistencies and verify the cleaned data.

### 7. Feature Engineering
   - **Create New Columns**: Calculate the `Total Amount` for each transaction by multiplying `unit_price` by `quantity` and adding this as a new column.
   - **Enhance Dataset**: Adding this calculated field will streamline further SQL analysis and aggregation tasks.

### 8. Load Data into MySQL and PostgreSQL
   - **Set Up Connections**: Connect to MySQL and PostgreSQL using `sqlalchemy` and load the cleaned data into each database.
   - **Table Creation**: Set up tables in both MySQL and PostgreSQL using Python SQLAlchemy to automate table creation and data insertion.
   - **Verification**: Run initial SQL queries to confirm that the data has been loaded accurately.

### 9. SQL Analysis: Complex Queries and Business Problem Solving
   - **Business Problem-Solving**: Write and execute complex SQL queries to answer critical business questions, such as:
     - Revenue trends across branches and categories.
     - Identifying best-selling product categories.
     - Sales performance by time, city, and payment method.
     - Analyzing peak sales periods and customer buying patterns.
     - Profit margin analysis by branch and category.
   - **Documentation**: Keep clear notes of each query's objective, approach, and results.

---

## Key Business Questions Answered

1. **Payment Analysis**: Different payment methods, number of transactions, and quantity sold by payment method
2. **Category Performance**: Highest-rated category in each branch
3. **Traffic Analysis**: Busiest day for each branch based on transaction volume
4. **Sales Metrics**: Total quantity of items sold per payment method
5. **Rating Analysis**: Average, minimum, and maximum ratings of categories for each city
6. **Profitability**: Total profit calculation for each category
7. **Payment Preferences**: Most common payment method for each branch
8. **Time-based Analysis**: Sales categorization by shifts (Morning, Afternoon, Evening)
9. **Branch Performance**: Revenue and transaction patterns across different branches
10. **Customer Behavior**: Shopping patterns, rating trends, and payment preferences

---

## SQL Query Highlights

### MySQL & PostgreSQL Implementations
Both database systems were used to demonstrate cross-platform SQL skills:

- **Window Functions**: `RANK()`, `PARTITION BY` for advanced analytics
- **Aggregations**: `SUM()`, `AVG()`, `COUNT()`, `MIN()`, `MAX()`
- **Date Functions**: Day name extraction and date parsing
- **Common Table Expressions (CTEs)**: For complex query organization
- **GROUP BY Operations**: Multi-level grouping for detailed insights

---

## Dataset Information

- **Source**: [Walmart Sales Dataset on Kaggle](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
- **Size**: 10,000+ sales records
- **Key Features**:
  - Branch and city information
  - Product categories
  - Payment methods
  - Quantity and unit price
  - Profit margins
  - Customer ratings
  - Transaction dates and times







---

## Getting Started

### Prerequisites
```bash
# Install required Python packages
pip install pandas numpy sqlalchemy mysql-connector-python psycopg2 pymysql
```

### Database Setup

**MySQL Setup:**
```sql
CREATE DATABASE walmart_db;
USE walmart_db;
```

**PostgreSQL Setup:**
```sql
CREATE DATABASE walmart_db;
\c walmart_db;
```

### Running the Project

1. **Clone the repository**
2. **Install dependencies**: `pip install -r requirements.txt`
3. **Configure database connections** in the Jupyter notebook
4. **Run the notebook**: Open `project.ipynb` and execute cells sequentially
5. **Execute SQL queries**: Use the provided SQL files for additional analysis

---

## Results and Insights

### Sales Insights
- **Payment Methods**: Analysis reveals the distribution and preferences across Cash, Credit Card, and E-wallet transactions
- **Peak Performance**: Identified busiest days and times for each branch to optimize staffing and inventory
- **Category Leaders**: Determined highest-rated and most profitable product categories

### Profitability Analysis
- **Category Profitability**: Calculated total profit by category considering unit price, quantity, and profit margin
- **Branch Performance**: Compared revenue generation across different branches and cities
- **Margin Analysis**: Evaluated profit margins to identify high-value product lines

### Customer Behavior
- **Rating Trends**: Analyzed customer satisfaction across categories and locations
- **Payment Preferences**: Identified preferred payment methods by branch
- **Shopping Patterns**: Discovered peak shopping hours and days for better resource allocation

---

## Project Learnings

- End-to-end data pipeline development from acquisition to analysis
- Data cleaning and preprocessing techniques for real-world datasets
- Advanced SQL query writing with window functions and CTEs
- Database integration with Python using SQLAlchemy
- Cross-platform database implementation (MySQL and PostgreSQL)
- Business intelligence and actionable insight generation

---

## Future Enhancements

- **Interactive Dashboards**: Integration with Power BI or Tableau for dynamic visualizations
- **Real-time Analytics**: Implement automated data pipeline for continuous data ingestion
- **Predictive Modeling**: Add machine learning models for sales forecasting
- **Geographic Analysis**: Expand location-based analysis with mapping visualization
- **Customer Segmentation**: Implement RFM analysis for customer categorization
- **API Development**: Create REST API for query results and insights

---

## Author

Created as an end-to-end data analysis project to demonstrate proficiency in:
- Python programming
- SQL (MySQL & PostgreSQL)
- Data cleaning and preprocessing
- Database design and management
- Business analytics and problem-solving

---

## License

This project is available for educational and portfolio purposes.

---

## Acknowledgments

- Dataset provided by Kaggle
- Walmart for the sample business case scenario

