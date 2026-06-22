**GlobalMart Retail Data Platform using Snowflake**
**About Project**

This is my Snowflake Data Engineering project where I built a complete data pipeline using AWS S3 and Snowflake.

The main goal of this project was to understand how real-world retail data can be loaded, transformed and used for analytics. In this project I worked with different file formats like CSV, JSON and Parquet and created an automated pipeline using Snowpipe, Streams and Tasks.

**I followed the Medallion Architecture approach (Raw → Staging → Gold) to organize the data.**

**Tools and Technologies Used**
Snowflake
AWS S3
Snowpipe
Streams
Tasks
SQL
JSON
Parquet
Data Warehousing Concepts


**Project Flow**

AWS S3
   ↓
External Stage
   ↓
Snowpipe
   ↓
RAW Layer
   ↓
Streams
   ↓
Tasks
   ↓
STAGING Layer
   ↓
GOLD Layer
Data Sources
CSV Data

**Contains sales transaction data such as:**

Transaction ID
Store Details
Customer Details
Product Information
Payment Method
JSON Data

**Contains IoT sensor events such as:**

Event Information
Device Details
Sensor Readings
Battery Percentage
Parquet Data

**Contains inventory and supplier data such as:**

Orders
Suppliers
Warehouse Information
Delivery Details
What I Implemented
**1. Storage Integration**

Created a Storage Integration to connect Snowflake with AWS S3 bucket.

**2. External Stage**

Created an External Stage to access files stored in S3.

**3. File Formats**

Created separate file formats for:

CSV Files
JSON Files
Parquet Files
**4. Snowpipe**

Used Snowpipe for automatic data ingestion from S3 to Snowflake.

**Created separate pipes for**:

CSV Files
JSON Files
Parquet Files
**5. Streams**

Created streams on raw tables to capture new data changes.

**6. Tasks**

Created tasks to automatically process data from Raw Layer to Staging Layer.

**7. Transformations**

Performed data cleaning and transformations such as:

D**ata type conversions**
JSON flattening
Derived columns
Revenue calculations
Payment method standardization
Database Layers
Raw Layer

Stores source data without major transformations.

**Tables:**

iot_events_raw
pos_batch
orders_prq
Staging Layer

Stores cleaned and transformed data.

**Tables:**

stg_csv_transaction
stg_json_sensors
stg_orders_parquet
Gold Layer

Stores business-ready analytics tables.

**Tables:**

daily_sales_fact
gross_margin_fact
fact_iot_sensor
Analytics Created
Daily Sales Analysis
Total Revenue
Average Cart Size
Unique Customers
Store-wise Sales
Gross Margin Analysis
Revenue
Cost
Gross Profit
Gross Margin %
IoT Analytics
Average Footfall
Average Temperature
Sensor Monitoring
What I Learned

**Through this project I learned:**

Snowflake Architecture
Snowpipe Auto Ingestion
Streams and Tasks
Handling JSON Data
Working with Parquet Files
Building ETL Pipelines
Data Warehouse Design
Medallion Architecture
Future Improvements

**In future I want to add:**

SCD Type 2
Dynamic Tables
Data Quality Checks
Error Logging
Power BI Dashboard
CI/CD Pipeline
Final Note

This project was built for learning and practicing Snowflake Data Engineering concepts. The main focus was to create an end-to-end pipeline that automatically ingests data from AWS S3, processes it and generates business-ready analytics tables.

I learned a lot while building this project and it helped me understand how modern data engineering pipelines work in real-world scenarios.
