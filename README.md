# Final Project: Fraud Transaction Pipeline

## Data
You can download the dataset [here](https://drive.google.com/file/d/1LmPGE7Vgn1yYszM0s9nwfmwr36RHI3BB/view?usp=drive_link)

## Bussiness Understanding
### Problem Description
A Digital Wallet company has quite a large amount of online transaction data. The company wants to know whether the data they have is data that has good data quality or not. On the other hand, the company also wants to use online transaction data to detect online payment fraud that harms their business.

### Goals
Create a data pipeline that can be utilised for analysis and reporting to determine whether online transaction data has excellent data quality and can be used to detect fraud in online transactions. 

### Project Objectives
- Create an **automated pipeline** that facilitates the batch and stream data processing from various data sources to data warehouses and data mart.
- Create a **visualization dashboard** to obtain meaningful insights from the data, enabling informed business decisions.

## Pipeline Architecture



Image 1. Pipeline Architecture

## Tools
- Orchestration: Airflow
- Tranformation: Spark, dbt 
- Streaming: Kafka
- Compute: Virtual Machine (VM) instance
- Container: Docker
- Storage: Google Cloud Storage
- Warehouse: BigQuery
- Data Visualization: Looker

## What should you install on your desktop ?

Docker Engine & Docker Compose : https://docs.docker.com/engine/install/ 

## Batch Processing

##### Clone the repository
```bash
git clone https://github.com/graceyudhaaa/final-project-fraud-transaction-pipeline.git
```

##### Enter the directory project

```bash
cd final-project-fraud-transaction-pipeline
```

##### Run your docker Engine & docker compose

##### Create image and build environment with Docker Compose
```bash
docker-compose up
```
#### Open Airflow with username and password "airflow" to run the DAG
# add supporting images please 
<a> href:"https://drive.google.com/drive/folders/1_Khyn06a98nQ7tCEf0u3S24VEVU8ER5E?hl=id" </a>

#### Open Spark to monitor Spark master and Spark workers
# add supporting images please 

## Streaming Processing

##### Enter the directory streaming pipeline
```bash
cd kafka
```

##### Create streaming pipeline with Docker Compose
```bash
docker-compose up
```

##### Install required Python packages
```bash
pip install -r requirements.txt
```

##### Run the producer to stream the data into the Kafka topic
```bash
python producer.py
```

##### Run the consumer to consume the data from Kafka topic and load them into BigQuery
```bash
python consumer.py
```
<br>

Data will be loaded into the record table for all transactions in BigQuery, and if any data is detected as fraud, it will be recorded in the detected_fraud table, and an automatic email notification indicating fraud will be sent.

Image 2. Streaming Process <br>

Image 3. Fraud Detected Table <br>

Image 4. Email Notification from Data that Detected Fraud


## Data Warehouse

## Analytic and Visualization



