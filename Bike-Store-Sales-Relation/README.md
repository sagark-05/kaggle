# Bike Store Sales Relationships

This project contains a relational bike-store dataset for exploring the connections between products, customers, orders, stores, staff, and inventory. The CSV files are the source tables; `all_combined.csv` is a concatenated view that includes a `source_file` column identifying each row's original file.

## Files

- `brands.csv`, `categories.csv`, and `products.csv`: product catalog and classifications
- `customers.csv`: customer records
- `orders.csv` and `order_items.csv`: order headers and line items
- `stores.csv` and `staffs.csv`: store and employee records
- `stocks.csv`: product inventory by store
- `all_combined.csv`: combined rows from the source CSV files
- `bike_store.db`: SQLite database used for database exploration
- `phase2.ipynb`: notebook for combining CSV files and querying data with SQLite

## Notebook

The notebook uses pandas to read and combine the CSV tables, adds each table's filename as `source_file`, and writes the result to `all_combined.csv`. It also demonstrates loading `products.csv` into the `products` table in `bike_store.db` and querying product rows.

## Run

Open `phase2.ipynb` from this directory in Jupyter Notebook or VS Code. The notebook uses Python, pandas, NumPy, Matplotlib, and SQLAlchemy; SQLite support is included with Python.

Install the external packages with:

```bash
python -m pip install pandas numpy matplotlib sqlalchemy jupyter
```
