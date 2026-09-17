# E-commerce Sales Analyzer

A Python script (built in Jupyter Notebook) that reads raw e-commerce order data from a CSV file and generates key sales insights — without relying on external libraries like pandas. Built as a hands-on exercise in manual data parsing, aggregation, and file I/O using core Python.


## Features

- **Revenue & order metrics** — total revenue, total orders, and total quantity sold
- **Breakdowns** — revenue grouped by product category and by individual product
- **Top performers** — highest-selling product (by quantity) and top customer (by revenue)
- **Daily revenue report** — revenue totals grouped by order date
- **Custom date-range filter** — enter a start and end date to calculate revenue within that window
- **Category export** — filters all Electronics orders and writes them to a new CSV (`electronics_sales.csv`)


## Tech Stack

- Python 3 (standard library only — `csv` parsing done manually via string splitting, plus `datetime`)
- Jupyter Notebook


## Project Structure

```
ecommerce-sales-analyzer/
├── sales_analyzer.ipynb      # Main notebook with all analysis steps
├── sales_data.csv            # Source dataset
├── electronics_sales.csv     # Generated output (Electronics-only orders)
└── README.md
```


## How to Run

1. Clone the repo and open `sales_analyzer.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
2. Make sure `sales_data.csv` is in the same directory as the notebook.
3. Run the cells in order.
4. When prompted, enter a start and end date (format: `YYYY-MM-DD`) to see revenue for that specific range.

> **Note:** The date-range cell uses `input()`, so it needs to be run interactively — it won't execute automatically end-to-end (e.g., via "Run All" in a non-interactive environment).


## Sample Output

```
Total Revenue: $ 26662151
Total Orders: 1000
Total Quantity Sold: 3129
Highest Sold Product: Notebook
Quantity Sold: 355
Top Customer: Priya Singh | Revenue: $ 5367141
```

## Possible Future Improvements

- Refactor using `pandas` for comparison against the manual approach
- Add data visualizations (matplotlib/seaborn) for revenue trends
- Add unit tests for the aggregation functions
