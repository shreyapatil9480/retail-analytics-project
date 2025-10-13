# Synthetic Sales Analysis Project

This project provides a complete, ready‑to‑use toolkit for analyzing synthetic retail sales data. It is designed for **business analysts**, **program managers**, and **data analysts** who want to demonstrate their analytical and machine‑learning skills on a realistic dataset. The repository includes a synthetic dataset, an exploratory data analysis and modeling notebook, and installation instructions.

## Repository Structure

| Path/Folder                 | Description                                                                        |
|-----------------------------|------------------------------------------------------------------------------------|
| `synthetic_sales_data.csv` | Synthetic dataset with retail transactions, marketing, and economic variables.    |
| `sales_analysis_notebook.ipynb` | Jupyter notebook containing exploratory data analysis, visualizations, and predictive modeling (regression and classification). |
| `requirements.txt`          | Python dependencies needed to run the notebook.                                    |
| `README.md`                 | Documentation and usage guide (this file).                                        |

## Dataset Overview

The **synthetic_sales_data.csv** file contains 1,500 records of fictional retail transactions. Each row represents a single order with the following columns:

- **`Order_ID`** – Unique identifier for the order.
- **`Date`** – Date of the transaction (between 2022‑01‑01 and 2022‑12‑31).
- **`Region`** – Region of the sale (`North`, `South`, `East`, `West`).
- **`Product_Category`** – Type of product (`Electronics`, `Clothing`, `Furniture`, `Grocery`).
- **`Price`** – Unit price of the product in dollars.
- **`Quantity`** – Number of units sold.
- **`Marketing_Spend`** – Marketing spend associated with the order (USD).
- **`Economic_Index`** – Synthetic macro‑economic indicator (scaled between 80 and 120).
- **`Competitor_Price`** – Price of a comparable competitor product.
- **`Sales`** – Total sales revenue (USD), calculated as `Price × Quantity` with noise.
- **`Profit`** – Profit on the order (USD), calculated as `Sales – Cost`.
- **`High_Performer`** – Binary flag indicating whether the order is a high performer (1) or not (0).

> **Note:** The dataset is entirely synthetic and was generated using random number generators. No real customer or company information is used.

## Notebook Contents

The **sales_analysis_notebook.ipynb** notebook guides you through:

1. **Loading and previewing the data** – Inspect data types, missing values, and sample rows.
2. **Descriptive statistics** – Summarize numeric features and basic information.
3. **Exploratory Data Analysis (EDA)** – Explore distributions of sales and profit, compare sales across regions and product categories, and visualize a correlation matrix.
4. **Regression modeling** – Predict `Sales` using numerical features with a linear regression model. Performance is evaluated using Mean Absolute Error and R² metrics.
5. **Classification modeling** – Predict the binary `High_Performer` flag using a logistic regression classifier. Performance metrics include accuracy and a confusion matrix.

The notebook includes narrative explanations alongside code to help you understand the reasoning behind each step. Visualizations are produced using Matplotlib and Seaborn.

## Getting Started

To run this project locally, follow these steps:

1. **Clone the repository.**
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```
2. **Create and activate a virtual environment (optional but recommended).**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```
3. **Install the dependencies.**
   ```bash
   pip install -r requirements.txt
   ```
4. **Launch Jupyter Notebook.**
   ```bash
   jupyter notebook
   ```
5. **Open the notebook** `sales_analysis_notebook.ipynb` and follow the code and comments. You can run the cells sequentially to replicate the analysis and models.

## Usage and Adaptation

This project is meant to serve as a template for your own analytics portfolio. You can modify the dataset generation logic, try different algorithms (e.g., Random Forests, Gradient Boosting), or add new features and charts. The modular structure makes it easy to extend the analysis or apply it to real datasets.

## License

This project is provided for educational and portfolio purposes. Feel free to fork, modify, and share it. No warranty is provided.

