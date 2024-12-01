# 📦 Retail-Inventory-Management-Data-Engineering-Project

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![SQL Server](https://img.shields.io/badge/SQL%20Server-2019+-red.svg)](https://www.microsoft.com/sql-server)
[![Azure Machine Learning](https://img.shields.io/badge/Azure-Machine%20Learning-blueviolet)](https://azure.microsoft.com/services/machine-learning/)

## 📝 Project Overview

This project aims to improve inventory management and demand forecasting by leveraging the **AdventureWorks** dataset. The goal is to create a structured SQL database, perform ETL processes, and build forecasting models to help businesses make informed decisions on inventory levels and sales strategies.

### 🎯 Project Goals

The Retail Inventory Management and Forecasting project is designed to streamline inventory operations by focusing on three main components:

- **ERD Schema**: A visual representation of entities and their relationships, focusing on Products, Suppliers, Sales, and Inventory Levels.
- **SQL Tables and Queries**: The development of SQL tables and queries to extract insights, such as top-selling products, low-stock alerts, and monthly revenue analysis.
- **Data Warehouse Design**: The design and implementation of a data warehouse with fact and dimension tables for reporting and analysis.

The project integrates tools like SQL Server, Azure Data Factory, Python, and Azure Machine Learning to build a robust system for inventory management and forecasting.

## 🛠 Tools and Technologies

- **SQL Server**: For managing and querying the relational database.
- **Azure Data Factory**: For ETL (Extract, Transform, Load) operations.
- **Python**: For data cleaning, processing, and demand forecasting.
- **Azure Machine Learning**: For building and evaluating forecasting models.
- **AdventureWorks Dataset**: A sample retail dataset provided by Microsoft, used for database design, data analysis, and reporting.  
  Download the dataset from the official Microsoft website: [AdventureWorks Sample Databases](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure)

## 🚀 Key Features

- [x] ERD Schema Design
- [x] SQL Table Creation
- [x] Advanced Querying
- [ ] Machine Learning Model
- [ ] Predictive Analytics

## 🔧 Setup and Installation

### 📋 Prerequisites

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

## 🗄️ Database Setup

### SQL Server Database
- [ ] Restore the **AdventureWorks** database
- [ ] Import provided SQL scripts to create additional tables or views

### Setup Workflow
1. Run the Data Warehouse Design scripts in SQL Server
2. Install required Python dependencies
3. Execute Python scripts for ETL operations and demand forecasting

## 📊 Entity-Relationship Diagram (ERD)

The ERD schema represents key entities in retail inventory data:

| Entity | Description |
|--------|-------------|
| **Products** | Information about products (ID, name, category, price) |
| **Suppliers** | Supplier details (ID, name, contact information) |
| **Sales** | Sales transactions linking products, quantities, revenues |
| **Inventory Levels** | Current stock levels for each product |

### 🔗 Key Relationship Highlights
- **Products** ↔ **Suppliers**: One-to-Many
- **Products** ↔ **Sales**: Many-to-Many
- **Sales** tracks products sold
- **Inventory Levels** monitors product availability

## 💾 SQL Database Structure

### Primary Tables
- `Products`: Product information storage
- `Suppliers`: Supplier details management
- `Sales`: Transaction data recording
- `InventoryLevels`: Stock level tracking

### 🔍 Example SQL Queries

#### Top-Selling Products
```sql
SELECT TOP 5 ProductID, SUM(Quantity) AS TotalSold 
FROM Sales 
GROUP BY ProductID 
ORDER BY TotalSold DESC;
```

#### Low Stock Alerts
```sql
SELECT ProductID, StockLevel 
FROM InventoryLevels 
WHERE StockLevel < 50;
```

#### Monthly Revenue Analysis
```sql
SELECT 
    YEAR(SaleDate) AS Year, 
    MONTH(SaleDate) AS Month, 
    SUM(TotalAmount) AS Revenue 
FROM Sales 
GROUP BY YEAR(SaleDate), MONTH(SaleDate) 
ORDER BY Year, Month;
```

## 🏗️ Data Warehouse Architecture

### Warehouse Components
- **Fact Table**: `SalesFact`
  - Stores sales transactions
  - Links to dimension tables

- **Dimension Tables**:
  - `ProductDim`: Product attributes
  - `SupplierDim`: Supplier details
  - `TimeDim`: Time-related information
  - `InventoryDim`: Inventory specifics

## 🚀 Project Capabilities
- Data-driven retail inventory management
- Demand forecasting system
- Integrated technologies:
  - SQL: Data storage & processing
  - Python: Data cleaning & forecasting
  - Azure Machine Learning: Model deployment

## 🤝 Contribution Guidelines
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## ⚠️ Requirements
- SQL Server
- Python 3.8+
- Azure Machine Learning SDK

## 📜 License
Distributed under the MIT License. See `LICENSE` for more information.

**Happy Coding! 👨‍💻👩‍💻**
