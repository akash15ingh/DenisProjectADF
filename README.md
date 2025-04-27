This project simulates a real-world data engineering and analytics pipeline.
I worked with multiple datasets covering:

Sales data for 4 years (2022-2025)

Product Categories and Sub-categories

Product details

Sales Representatives

Geographical information

The goal was to ingest, clean, transform, and model the data into a single structured dataset for business analysis and visualization using Power BI.

📦 Datasets Used
Sales (Yearly split: 2022, 2023, 2024, 2025)

Category

Sub-category

Product

Sales Representative

Geography

🛠️ Tools & Technologies
Azure Blob Storage (for raw file storage)

Azure Data Lake Storage (ADLS Gen2) (for Bronze/Silver/Gold layer architecture)

On-Premise MySQL Database (simulated)

Azure Data Factory (ADF) (for data movement, cleansing, surrogate key generation, transformations)

Azure SQL Database (for curated gold layer storage)

Power BI (for data visualization)

🔄 Data Flow Process
Data Ingestion:

CSV, JSON, and Excel files from Blob Storage

Tables from On-Prem MySQL Database

All raw data staged into Bronze Layer of ADLS.

Data Cleansing and Transformation:

Using ADF Mapping Data Flows:

Generated Surrogate Keys (e.g., GeoID, ProductID)

Standardized formats (Dates, Text casing, etc.)

Removed duplicates

Derived new columns (e.g., Profit calculation)

Stored cleaned datasets into Silver Layer of ADLS.

Data Modeling:

Joined all datasets logically (Sales, Product, Rep, Geography) using surrogate keys.

Built a final single denormalized table ready for analysis.

Stored the final dataset into Gold Layer of ADLS and Azure SQL Database.

Data Visualization:

Connected Power BI to Azure SQL DB.

Created dashboards and analytical reports on Sales, Revenue, Profits, Regional Performance, and Sales Rep performance.

📈 Highlights
Implemented Bronze-Silver-Gold Lakehouse Architecture.

Solved real-world challenges like:

Missing keys

Surrogate key generation

Data type mismatches

Complex joins across datasets

Designed a reusable, scalable, production-like pipeline using Azure-native tools.

🚀 Future Enhancements
Automate ingestion with Event Triggers and Incremental Loads.

Add Data Quality Checks at Silver Layer.

Implement Delta Lake architecture for version control.

Optimize Power BI dashboards for real-time refresh.
