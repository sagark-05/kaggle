# BMW Global Sales Prediction

This project explores BMW sales data from 2018–2025. The dataset records monthly sales by region and vehicle model, alongside pricing and market indicators.

## Files

- `bmw_global_sales_2018_2025.csv`: sales and market dataset
- `phase1.ipynb`: notebook for loading the data and performing exploratory analysis

## Dataset

The CSV includes `Year`, `Month`, `Region`, `Model`, `Units_Sold`, `Avg_Price_EUR`, `Revenue_EUR`, `BEV_Share`, `Premium_Share`, `GDP_Growth`, and `Fuel_Price_Index`.

## Notebook

The notebook uses pandas to inspect the dataset and calculate descriptive statistics. It also plots distributions and compares sales across years, regions, and models. The current notebook is exploratory; it does not yet train or evaluate a sales prediction model.

## Run

Open `phase1.ipynb` from this directory in Jupyter Notebook or VS Code. The notebook uses Python, pandas, NumPy, and Matplotlib.

Install the required packages with:

```bash
python -m pip install pandas numpy matplotlib jupyter
```
