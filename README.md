# Project_ETL_Netflix-Data

===================================
ETL Process in Python (Kaggle to Data Lake)
===================================

This project involves an ETL (Extract, Transform, Load) process that extracts a dataset from Kaggle, processes the data using Python libraries (NumPy, Pandas), and then loads the processed data into a Data Lake (Google Cloud Storage).

Project Overview
================

This project demonstrates the following steps:

1. **Extract Kaggle Dataset:**
   - Download a dataset from Kaggle using the Kaggle API.
   - Use Python libraries such as Pandas and NumPy to extract the data from the downloaded file.

2. **ETL Process:**
   - **Extract:** Load the dataset into a Pandas DataFrame.
   - **Transform:**
     - **Data Cleaning:** Handle missing values and remove duplicates.
     - **Data Type Conversion:** Convert data types for compatibility.
     - **Filtering:** Filter data based on specific conditions.
     - **Aggregation:** Apply any necessary aggregations to the data.
     - **Transformations:** Apply transformations to shape the data as per requirements.

3. **Load Data to Data Lake (Cloud Storage):**
   - Store the transformed dataset as a CSV file in Google Cloud Storage.
   - Create a Cloud Storage bucket and load the transformed CSV file into it.

Diagram Overview
================

The following diagram illustrates the ETL process:

1. **Kaggle → Python:**
   - Extract dataset from Kaggle via API.
   
2. **Python (ETL Process):**
   - Load data into a Pandas DataFrame.
   - Data Cleaning: Handle missing data, remove duplicates.
   - Data Transformation: Data type conversion, filtering, and aggregation.

3. **Python → Google Cloud Storage (Data Lake):**
   - Store the transformed data into Google Cloud Storage as a CSV file.
   - Use the Google Cloud Storage bucket to store the CSV file.

Project Structure
=================

The main components of the project are:

- **`data/`:** Directory for raw and processed data.
- **`scripts/`:** Python scripts used for ETL.
- **`config/`:** Configuration files, such as Kaggle API key and GCP credentials.
- **`README.rst`:** Project documentation.

Setup and Prerequisites
=======================

**Prerequisites:**
- Python 3.x
- Kaggle API access
- Google Cloud SDK and GCP access
- Cloud Storage bucket
- Internet connection to download Kaggle datasets

**Python Libraries Required:**
- `numpy`
- `pandas`
- `google-cloud-storage`
- `kaggle`

**Environment Setup:**
1. Install the Kaggle API and authenticate:
   ::
   
       pip install kaggle
       mkdir ~/.kaggle
       cp /path/to/kaggle.json ~/.kaggle/kaggle.json
       chmod 600 ~/.kaggle/kaggle.json

2. Install the necessary Python libraries:
   ::
   
       pip install numpy pandas google-cloud-storage

3. Set up Google Cloud credentials:
   ::
   
       export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your-service-account-key.json"


