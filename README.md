# Retail-Inventory-Management-Data-Engineering-Project

This project aims to improve inventory management and demand forecasting by leveraging the **AdventureWorks** dataset. The goal is to create a structured SQL database, perform ETL processes, and build forecasting models to help businesses make informed decisions on inventory levels and sales strategies.

## Project Overview

The Retail Inventory Management and Forecasting project is designed to streamline inventory operations by focusing on three main components:

- **ERD Schema**: A visual representation of entities and their relationships, focusing on Products, Suppliers, Sales, and Inventory Levels.
- **SQL Tables and Queries**: The development of SQL tables and queries to extract insights, such as top-selling products, low-stock alerts, and monthly revenue analysis.
- **Data Warehouse Design**: The design and implementation of a data warehouse with fact and dimension tables for reporting and analysis.

The project integrates tools like SQL Server, Azure Data Factory, Python, and Azure Machine Learning to build a robust system for inventory management and forecasting.

## Tools and Technologies

- **SQL Server**: For managing and querying the relational database.
- **Azure Data Factory**: For ETL (Extract, Transform, Load) operations.
- **Python**: For data cleaning, processing, and demand forecasting.
- **Azure Machine Learning**: For building and evaluating forecasting models.
- **AdventureWorks Dataset**: A sample retail dataset provided by Microsoft, used for database design, data analysis, and reporting.  
  Download the dataset from the official Microsoft website: [AdventureWorks Sample Databases](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure)

## Setup and Installation

### Prerequisites

- Install **SQL Server** and ensure you have access to **Azure Data Factory**.
- Install Python 3.7+ and the following libraries:
  - `pandas`
  - `sqlalchemy`
  - `statsmodels`
  - `scikit-learn`
  - `mlflow`
  
  You can install the necessary Python packages with:

  ```bash
  pip install pandas sqlalchemy statsmodels scikit-learn mlflow
