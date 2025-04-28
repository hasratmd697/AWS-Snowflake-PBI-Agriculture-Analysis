# AWS + Snowflake + Power BI Agriculture Project

## Project Overview
This project demonstrates the complete data pipeline and analysis workflow using **Amazon S3**, **Snowflake Data Warehouse**, and **Power BI**.  
It covers data ingestion, transformation, integration, and insightful reporting on agricultural datasets, focusing on rainfall, temperature, humidity, and yield.


## Steps and Workflow

### 1. Amazon S3 Setup
- Created an **Amazon S3 bucket**.
- Loaded raw agricultural data files into the S3 bucket.

### 2. IAM Role Creation
- Created a new IAM Role named **`powerbi.role`**.
- Granted **AmazonS3FullAccess** permission to the role.
- Updated the trust relationship policy to allow integration with Snowflake.

### 3. Snowflake Data Warehouse Setup
- Created an **Integration Object** in Snowflake to connect with the S3 bucket.
- Updated the trust policy for secure connection.
- Loaded the data from S3 into **Snowflake tables**.

### 4. Data Transformation in Snowflake
- Performed **SQL-based data transformations**:
  - Cleaned and normalized the dataset.
  - Added a new derived column **`Rainfall Group`** to categorize rainfall levels.

### 5. Power BI Data Visualization
- Imported the transformed data into Power BI using the **Snowflake Connector**.
- Designed multiple insightful pages in the Power BI report:
  
  #### Rainfall Analysis Page
  - Bar charts for:
    - Average Rainfall by **Year**
    - Average Rainfall by **Season**
    - Average Rainfall by **Crops**
    - Average Rainfall by **Location**
  
  #### Temperature Analysis Page
  - Bar charts for:
    - Average Temperature by **Year**
    - Average Temperature by **Season**
    - Average Temperature by **Crops**
    - Average Temperature by **Location**

  #### Humidity Analysis Page
  - Bar charts for:
    - Average Humidity by **Year**
    - Average Humidity by **Season**
    - Average Humidity by **Crops**
    - Average Humidity by **Location**

  #### Yield Analysis Page
  - Bar charts for:
    - Average Yield by **Year**
    - Average Yield by **Season**
    - Average Yield by **Crops**
    - Average Yield by **Location**

### 6. Report Publishing
- Published the final Power BI report to the **Power BI Service** for sharing and dashboarding.

## Tech Stack

- **Cloud Storage**: Amazon S3
- **Data Warehouse**: Snowflake
- **Cloud IAM & Security**: AWS IAM
- **Data Visualization**: Microsoft Power BI

## Project Structure

```
aws-snowflake-powerbi-project/
│
├── data/                  # Amazon S3 bucket data files
├── sql/                   # Snowflake SQL scripts for transformations
├── powerbi/                # Power BI report files (.pbix)
├── documentation/          # Trust policies, IAM role screenshots
├── README.md               # Project documentation
```


## Future Enhancements
- Automate data loading using AWS Lambda and Snowflake Tasks.
- Set up incremental refresh for datasets in Power BI.
- Add predictive analysis (e.g., rainfall forecasting) using Power BI AI visuals.


## Screenshots

![Screenshot 2025-04-28 121942](https://github.com/user-attachments/assets/1a430775-e0fe-4e32-a391-67118aa06383)

![Screenshot 2025-04-28 121952](https://github.com/user-attachments/assets/8e40c390-6c2b-4987-9374-4c63aa7f04b6)

![Screenshot 2025-04-28 122002](https://github.com/user-attachments/assets/f8b120bd-ba23-4f07-b658-cb3f49e14946)

![Screenshot 2025-04-28 122012](https://github.com/user-attachments/assets/21852d2c-95a1-41ac-9834-3926abf588c9)


