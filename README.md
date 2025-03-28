# Car Sales Data Analysis

This repository contains the code and data focusing on web scraping, data preparation, and exploratory analysis of car sales data. The project is split into two tasks, implemented as Jupyter Notebooks: Task 1 (web scraping) and Task 2 (data preparation and analysis).

## Project Overview

The objective is to scrape car sales data from a website, preprocess it, and analyze trends in the car sales market. The dataset includes attributes like car make, model, price, mileage, and fuel type, collected from listings for Audi, BMW, Mercedes-Benz, and Volkswagen.

- **Task 1: Data Collection**  
  - Scraped data from [http://mlg.ucd.ie/modules/python/assignment1/cars/index.html](http://mlg.ucd.ie/modules/python/assignment1/cars/index.html) using Python and BeautifulSoup.
  - Covered paginated listings: Audi (20 pages), BMW (20 pages), Mercedes-Benz (30 pages), Volkswagen (17 pages).
  - Saved results to `car_sales_data.csv`.

- **Task 2: Data Preparation and Analysis**  
  - Loaded `car_sales_data.csv` into a Pandas DataFrame, cleaned inconsistencies (e.g., missing values, duplicate categories), and transformed data.
  - Conducted exploratory analysis with Matplotlib and Seaborn visualizations (histograms, scatter plots, boxplots).
  - Summarized insights on pricing, fuel type preferences, and market trends.

## Repository Structure

- `task1_web_scraping.ipynb`: Notebook for web scraping and data collection.
- `task2_data_analysis.ipynb`: Notebook for data cleaning, visualization, and analysis.
- `car_sales_data.csv`: Raw dataset from Task 1, used in Task 2.
- `README.md`: This project overview.

## Setup Instructions

To run the notebooks locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/car-sales-analysis.git
   cd car-sales-analysis
   ```

2. **Install Dependencies**:
   Requires Python 3.6+. Install packages via pip:
   ```bash
   pip install pandas numpy matplotlib seaborn beautifulsoup4 requests jupyter
   ```

3. **Run the Notebooks**:
   Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
   Open `task1_web_scraping.ipynb` and `task2_data_analysis.ipynb` in the interface and execute the cells.

## Usage

- **Task 1 (`task1_web_scraping.ipynb`)**:  
  Scrapes car sales data and generates `car_sales_data.csv`. Requires an active connection to the target website; use the provided CSV if the site is unavailable.

- **Task 2 (`task2_data_analysis.ipynb`)**:  
  Loads `car_sales_data.csv`, cleans it, and performs analysis with visualizations. Includes a discussion of findings and challenges.

## Key Insights

- **Pricing**: Most cars are priced under €50,000, with outliers up to €200,000.
- **Mileage & Age**: Older, high-mileage cars (pre-2015) correlate with lower prices.
- **Fuel Types**: Electric cars average €50,000, Diesel €15,000; Diesel and Petrol dominate SUVs.
- **Market Share**: Mercedes-Benz leads (34%), followed by Audi, BMW, and Volkswagen.

See `task2_data_analysis.ipynb` for detailed analysis.

## Challenges

- **Scraping**: Handled pagination and inconsistent table layouts.
- **Cleaning**: Addressed mixed formats (e.g., dates, numbers) and duplicates (e.g., 'SUV' vs. 'S.U.V.').

## Future Work

- Predictive modeling for car prices.
- Integration of external datasets (e.g., economic factors).
- Text analysis of car descriptions.

## Acknowledgments

Completed for COMP41680 (Data Science in Python) at University College Dublin. Thanks to the instructors for the dataset and guidance.