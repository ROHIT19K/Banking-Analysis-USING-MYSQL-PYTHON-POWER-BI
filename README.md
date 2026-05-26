# 📊 Banking Data Analysis Dashboard
🔗 Power BI Dashboard Link : 
   
   (https://app.powerbi.com/groups/edd2cd91-ae5b-4698-8d63-7ca7575e2e08/reports/4dd06152-732a-497f-b4fb-b44edf0f484c/4a7dd4809a6d0d1da291?experience=power-bi)

## 📌 Project Overview

The Banking Analytics Dashboard is an interactive business intelligence solution developed to analyze and monitor banking operations, customer financial activities, loans, deposits, and account performance. The project was designed to help banking institutions gain meaningful insights from customer banking data and improve strategic decision-making.

## 🎯 Business Problem

Banks generate massive volumes of customer financial data daily, making it difficult for financial institutions to: 

The challenge was to:

* Track overall banking performance in one centralized dashboard.

* Analyze loan and deposit distribution across customer segments.

* Identify high-value customers and profitable banking relationships.

* Monitor business lending, deposits, savings, and checking accounts efficiently.

* Improve decision-making using interactive and real-time analytics.

* Reduce manual reporting efforts by automating insights through Power BI.

## 🛠 Tools & Technologies

🗄 MySQL Database – Used for storing and managing banking customer data.

🐍 Python – Used for Data Cleaning, Exploratory Data Analysis (EDA), and transformation.

🔌 MySQL Connector – Used to connect Python with MySQL Database.

📊 Power BI Desktop – Main data visualization platform used for dashboard development.

📂 Power Query – Used for additional data transformation and preprocessing.

🧠 DAX (Data Analysis Expressions) – Used for calculated measures, KPIs, and dynamic visuals.

## 📂 Dataset Information

### 📌 Dataset Source

MYSQL WorkBench - Banking Database (Table Name is : Customers)

### 📌 Dataset Columns

The dataset includes the following important fields:

Client ID

Name

Age

Location ID

Joined Bank

Banking Contact

Nationality

Occupation

Fee Structure

Loyalty Classification

Estimated Income

Superannuation Savings

Amount of Credit Cards

Credit Card Balance

Bank Loans

Bank Deposits

Checking Accounts

Saving Accounts

Foreign Currency Account

Business Lending

Properties Owned

Risk 

BRId

IAId

## 📈 Dashboard Highlights

1️⃣ Data Collection

Stored banking data in MySQL Database

Connected Python with MySQL using MySQL Connector

Imported banking data into Power BI

Verified dataset consistency and relationships

2️⃣ Data Cleaning & Transformation

Performed data cleaning and preprocessing using Python:

Removed null and inconsistent values

Standardized customer categories

Performed Exploratory Data Analysis (EDA)

Transformed banking and financial columns

Optimized data for reporting and visualization

Additional transformations were performed using Power Query.

### Calculated Measures :

    Banking Loans = SUM('banking_case customer'[Bank Loans]) + SUM('banking_case customer'[Business Lending]) + SUM('banking_case customer'[Credit Card Balance])


    Engagement Account =  SUM('banking_case customer'[Checking Accounts])
                        + SUM('banking_case customer'[Saving Accounts])
                        + SUM('banking_case customer'[Foreign Currency Account])
                        + SUM('banking_case customer'[Business Lending])
                        + SUMX(
                            'banking_case customer',
                            IF('banking_case customer'[Credit Card Balance] > 0, 1, 0)
                        )
                        + SUMX(
                            'banking_case customer',
                            IF('banking_case customer'[Bank Loans] > 0, 1, 0)
                        )
                        + SUMX(
                            'banking_case customer',
                            IF('banking_case customer'[Bank Deposits] > 0, 1, 0)
                        )

    Total Deposit = SUM('banking_case customer'[Bank Deposits]) +SUM('banking_case customer'[Saving Accounts]) + SUM('banking_case customer'[Checking Accounts]) +SUM('banking_case customer'[Foreign Currency Account])

    Total Fees = SUM('banking_case customer'[Business Lending]) + SUM('banking_case customer'[Foreign Currency Account]) + SUM('banking_case customer'[Bank Loans]) + SUM('banking_case customer'[Credit Card Balance])

3️⃣ KPI Development

Developed dynamic KPIs including:

Total Loan

Bank Loan

Business Lending

Credit Card (CC) Amount

Total Deposit

Bank Deposit

Savings Account Amount

Checking Account Amount

Foreign Currency Amount

Bank Loan by Income Band

Bank Deposit by Income 

Bank Loan by Nationality

Bank Deposit by Nationality

Bank Loan by 

Bank Deposit by Occupation

## 📊 Dashboard Preview

🔹 MySQL Database Integration

![Image1](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/MYSQL%20Connector%20.png)

🔹 Python EDA & Data Cleaning

![Image1](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Data%20Cleaning%20and%20Tranformation%20In%20Python%201.png%20.png)
![Image2](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Data%20Cleaning%20and%20Tranformation%20In%20Python%202.png%20.png)
![Image3](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Data%20Cleaning%20and%20Tranformation%20In%20Python%203.png%20.png)
![Image4](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Data%20Cleaning%20and%20Tranformation%20In%20Python%204.png%20.png%20.png)
![Image5](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Data%20Cleaning%20and%20Tranformation%20In%20Python%205.png%20.png)
![Image6](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Data%20Clearning%20And%20TransFormation.png)
![Image7](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/EDA%201.png)
![Image8](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/EDA%202.png)
![Image9](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/EDA%203.png)
![Image10](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/EDA%204.png)
![Image11](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/EDA%205.png)
![Image12](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/EDA%206.png)

🔹 Banking Dashboard Overview

![Image1](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Banking%201.png)
![Image2](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Banking%202.png)
![Image3](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Banking%203.png)
![Image4](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Banking%204.png)

🔹 Power BI Service Published Report

![Image1](https://github.com/ROHIT19K/Banking-Analysis-USING-MYSQL-PYTHON-POWER-BI/blob/main/Banking%20Power%20BI%20Service%20%201.png%20.png)


## 🔍 Key Insights

### 1. Home Page Insights

* Key Insights

        Total Clients: 3000

        Total Loan Amount: 4.38bn

        Total Deposit Amount: 3.77bn

        Business Lending contributes 2.60bn

        Checking Account balance reached 963.28M

        Savings Accounts contribute 698.73M

### . Loan Analysis Page Insights

* Key Insights

        Total Loan Amount: 4.38bn

        Business Lending contributes majority share at 2.60bn

        Private Banking segment has highest loan distribution (0.81bn)

        Medium income group customers take the highest loans (942.49M)

        European customers contribute highest bank loans (0.78bn)

        Occupations like Accountants and Database professionals show higher loan amounts.


### 3. Deposit Analysis Page 

* Key Insights

        Total Deposit Amount: 3.77bn

        Bank Deposits contribute 2.01bn

        Private Banking segment has highest deposits (0.93bn)

        Medium income customers contribute maximum deposits (1091.33M)

        European customers contribute highest deposits (0.87bn)

        Structural Engineers and Database professionals have higher deposit balances.

### 4. Summary Page Insights

* Key Insights

        Total Fees generated: 4.47bn

        Engagement Account amount reached 4.35bn

        Foreign Currency transactions contribute 89.65M

        Bank Loan vs Deposit comparison provides financial balance visibility.

        Strong contribution from both lending and deposit products.

## 🚀 Future Enhancements

Add real-time banking transaction monitoring

Integrate fraud detection analytics

Implement customer churn prediction using Machine Learning

Add predictive financial modeling

Create mobile-optimized dashboard version

Implement automated ETL pipelines

Add customer segmentation analytics

Deploy enterprise-level reporting architecture

## ▶️ How to Run the Project

* Step 1: 

Setup MySQL Database

Import banking dataset into MySQL Database

Configure database connection settings

* Step 2:

 Run Python Scripts

Connect Python with MySQL using MySQL Connector

Perform data cleaning and EDA

Validate transformed data

* Step 3:

 Open Power BI Dashboard

Open the .pbix file using Power BI Desktop

Connect Power BI with MySQL Database

Refresh dataset connections

* Step 4: 

Explore Dashboard

Use slicers and filters

Analyze banking customer insights

Monitor financial KPIs and risk 

## 📊 Project Workflow

Data Storage in MySQL Database

Python-MySQL Connection Setup

Data Cleaning & EDA Using Python

Data Transformation & 

Data Modeling

KPI 

Dashboard Design in Power BI

Interactive Reporting

Banking Insights Generation

## ✅ Results & Outcomes

Successfully built an interactive Banking Analysis Dashboard.

Implemented MySQL and Python-based analytics workflow.

Improved visibility into customer financial behavior.

Enabled detailed banking product analysis.

Created dynamic KPI monitoring system.

Delivered actionable banking insights for decision-making.

Demonstrated expertise in Python EDA, MySQL integration, and Power BI reporting.

# 📬 Contact
## 👤 Author

Your Name

LinkedIn: https://linkedin.com/in/yourprofile

GitHub: https://github.com/yourusername

Email: yourmail@gmail.com
