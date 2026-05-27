# Instacart Market Basket Analysis

## Overview

This project analyzes shopping data from the Instacart app to uncover insights into customer purchasing behavior. The analysis cleans raw data and explores patterns in order timing, product popularity, and customer shopping habits.

## Project Goals

- **Clean and Prepare Data**: Process raw Instacart datasets, handle missing values, and remove duplicates
- **Understand Customer Behavior**: Identify shopping patterns and preferences
- **Temporal Analysis**: Determine when customers order (day of week, time of day)
- **Product Analysis**: Identify the most frequently ordered products
- **Visualize Insights**: Present findings through charts and data visualizations

## Dataset Description

The project uses five main CSV datasets:

- **orders.csv**: Contains order information including order IDs, customer IDs, order dates, and days since prior order
- **products.csv**: Lists all products with product IDs, names, aisle, and department information
- **departments.csv**: Maps department IDs to department names
- **aisles.csv**: Maps aisle IDs to aisle names
- **order_products.csv**: Links orders to products with quantity and cart order information

### Data Cleaning Steps

1. **Missing Values Handling**:
   - Products with missing names are marked as "Unknown"
   - First orders naturally have no `days_since_prior_order` value (NaN retained)
   - Missing `add_to_cart_order` values (for cart positions 65+) are replaced with 999

2. **Duplicate Removal**: Duplicate rows are identified and removed from all datasets

## Analysis Performed

- Order frequency patterns by day of week
- Order timing analysis (preferred ordering times)
- Popular products and categories
- Customer ordering habits over time

## Key Technologies

- **Python 3**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Jupyter Notebook**: Interactive analysis environment

## Project Structure

```
instacart_market_basket_analysis/
├── README.md
└── instacart_market_basket_analysis.ipynb
```

## Usage

1. Ensure required datasets are available in the `/datasets/` directory:
   - instacart_orders.csv
   - products.csv
   - departments.csv
   - aisles.csv
   - order_products.csv

2. Open and run the Jupyter notebook:
   ```bash
   jupyter notebook instacart_market_basket_analysis.ipynb
   ```

3. Execute cells sequentially to:
   - Load and explore the datasets
   - Clean the data
   - Perform exploratory data analysis
   - Generate visualizations

## Key Insights Generated

The analysis provides answers to questions such as:
- What days of the week do customers order most frequently?
- What times are orders typically placed?
- Which products and categories are most popular?
- How do customer ordering patterns vary?

## Notes

- Dataset files use semicolon (`;`) as the delimiter instead of comma
- For cart orders beyond position 64, `add_to_cart_order` values are coded as 999
- First-time orders naturally have NaN values for `days_since_prior_order`

## Requirements

- Python 3.x
- pandas
- matplotlib
- jupyter

Install dependencies with:
```bash
pip install pandas matplotlib jupyter
```

## Author

This analysis is part of a market basket analysis project for Instacart customer insights.

## License

Project details and licensing information can be added here.
