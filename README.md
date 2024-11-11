# Personal Expense Tracker

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.4.2-green.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-0.11.2-purple.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.5.1-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## 📊 Project Overview

The **Personal Expense Tracker** is a Python-based application designed to help individuals monitor and analyze their financial transactions. By simulating realistic expense and income data, the project demonstrates data collection, cleaning, analysis, and visualization techniques essential for effective personal finance management.

*Click [here](https://app.powerbi.com/view?r=eyJrIjoiOTY2NWEzYzEtOWIyZC00NDQxLThiODYtYzRiZjQ5ZWFiMTQ0IiwidCI6ImE4ZWVjMjgxLWFhYTMtNGRhZS1hYzliLTlhMzk4YjkyMTVlNyIsImMiOjN9&pageName=3339e70762d6dd490c1b) to view the Power BI report.*


## 🛠️ Features

- **Data Simulation:** Generates synthetic financial transaction data, including income and expenses.
- **Data Cleaning:** Identifies and handles duplicates, missing values, and outliers to ensure data integrity.
- **Descriptive Analytics:** Provides summary statistics and insights into spending and income patterns.
- **Visualization:** Creates informative charts and dashboards to visualize financial trends.
- **Database Management:** Structures data for efficient storage and retrieval using CSV and relational databases.

## 🚀 Technologies Used

- **Programming Language:** Python 3.10
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Faker
- **Database:** CSV for data storage (optional: MySQL)
- **Visualization/BI tools:** Power BI, AWS QuickSight, MS Excel

## 💾 Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/yourusername/personal-expense-tracker.git
    cd personal-expense-tracker
    ```

2. **Create a Virtual Environment (Optional but Recommended):**

    ```bash
    python3 -m venv env
    source env/bin/activate  # On Windows: env\Scripts\activate
    ```

3. **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

    *If `requirements.txt` is not available, install the necessary libraries manually:*

    ```bash
    pip install pandas numpy matplotlib seaborn faker
    ```

## 📁 Usage

1. **Generate Synthetic Data:**

    Run the `data_collection.py` script to generate and save the expense data.

    ```bash
    python data_collection.py
    ```

    This will create an `expense_data.csv` file containing simulated financial transactions.

2. **Data Cleaning and Analysis:**

    Run the `data_management.py` script to clean, validate, and perform initial analysis on the data.

    ```bash
    python data_management.py
    ```

3. **Visualization:**

    Use the `data_visualization.py` script to generate various charts and dashboards that visualize your financial data.

    ```bash
    python data_visualization.py
    ```

## 📈 Data Collection & Cleaning

### Data Collection

- **Simulation:** Utilizes the `Faker` library to generate realistic synthetic data for personal financial transactions over the past year.
- **Fields Included:** Transaction ID, Date, Amount, Category, Payment Method, Merchant, User ID, Notes, and Type (Income/Expense).

### Data Cleaning and Transformation

- **Duplicate Removal:** Identifies and removes duplicate transactions based on `Transaction_ID`.
- **Missing Values Handling:** 
    - Replaces missing `Category` and `Payment_Method` with the mode.
    - Assigns 'Unknown Merchant' to missing `Merchant` entries.
    - Fills missing `Notes` with "No notes available."
- **Outlier Detection:** Uses the Interquartile Range (IQR) method to identify and handle outliers in transaction amounts.
- **Data Standardization:** Ensures consistent data types and formats for all fields.

## 📊 Data Analysis & Visualization

- **Descriptive Statistics:** Provides summary statistics such as mean, median, and distribution of transaction amounts.
- **Category Analysis:** Identifies top spending and income categories.
- **Trend Analysis:** Visualizes monthly and daily trends in income and expenses.
- **Payment Method Analysis:** Examines the distribution of payment methods used in transactions.
- **Predictive Modeling:** Implements forecasting techniques to predict future expenses and income.

## 🗄️ Database Management

- **Storage:** Data is primarily stored in CSV format for simplicity and ease of access.
- **Advanced Management:** For enhanced data handling, the dataset can be imported into relational databases like MySQL.
- **Schema Example:**

    | Column Name      | Data Type        | Description                                     |
    |------------------|-------------------|-------------------------------------------------|
    | Transaction_ID   | VARCHAR(36)       | Unique identifier for each transaction          |
    | Date             | DATETIME          | Date and time of the transaction                |
    | Amount           | FLOAT             | Monetary value of the transaction               |
    | Category         | VARCHAR(50)       | Category of the transaction (e.g., Food)        |
    | Payment_Method   | VARCHAR(50)       | Method used for the transaction (e.g., Cash)    |
    | Merchant         | VARCHAR(100)      | Merchant or source associated with the transaction |
    | User_ID          | VARCHAR(36)       | Unique identifier for the user                   |
    | Notes            | VARCHAR(255)      | Additional notes or descriptions                |
    | Type             | VARCHAR(10)       | Type of transaction (Income or Expense)         |

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## 📫 Contact

For any questions or suggestions, feel free to reach out:

- **Email:** geethikameka997@gmail.com
- **LinkedIn:** www.linkedin.com/in/gmeka

## 📝 License

This project is licensed under the [MIT License](LICENSE).

