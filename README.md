# Reddit Data Pipeline: Streamlining Data Flow with Airflow, Celery, Postgres, S3, AWS Glue, Athena, and Redshift

This project presents a robust solution for orchestrating the extraction, transformation, and loading (ETL) of Reddit data into a Redshift data warehouse. By utilizing a blend of cutting-edge tools and services such as Apache Airflow, Celery, PostgreSQL, Amazon S3, AWS Glue, Amazon Athena, and Amazon Redshift, this pipeline ensures efficient and scalable data processing.

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [System Setup](#system-setup)

## Overview

This data pipeline is engineered to:

1. Fetch data from Reddit via its API.
2. Store the raw data securely in an S3 bucket facilitated by Airflow.
3. Employ AWS Glue and Amazon Athena for data transformation.
4. Load the refined data into Amazon Redshift for advanced analytics and querying capabilities.

## Architecture
![RedditDataEngineering.png](assets%2FRedditDataEngineering.png)

1. **Reddit API**: Primary source of data.
2. **Apache Airflow & Celery**: Orchestrates the entire ETL process and manages task allocation.
3. **PostgreSQL**: Acts as temporary storage and oversees metadata management.
4. **Amazon S3**: Houses the raw data securely.
5. **AWS Glue**: Facilitates data cataloging and execution of ETL jobs.
6. **Amazon Athena**: Employs SQL-based transformation on the data.
7. **Amazon Redshift**: Serves as the data warehousing solution for analytics and insights.

## Prerequisites
- An AWS Account configured with appropriate permissions for S3, Glue, Athena, and Redshift.
- Valid Reddit API credentials.
- Docker Installation.
- Python version 3.9 or higher.

## System Setup
1. Clone the repository.
```bash
git clone https://github.com/DE-romane/Reddit-Data-Pipeline-AWS
```
2. Create a virtual environment.
```bash
python3 -m venv venv
```
3. Activate the virtual environment.
```bash
source venv/bin/activate
```
4. Install the required dependencies.
```bash
pip install -r requirements.txt
```
5. Rename the configuration file and input credentials.
```bash
mv config/config.conf.example config/config.conf
```
6. Start the containers.
```bash
docker-compose up -d
```
7. Access the Airflow web UI.
```bash
open http://localhost:8080
```
