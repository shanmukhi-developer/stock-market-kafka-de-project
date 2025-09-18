# Stock Market Kafka Real Time Data Engineering Project

## Introduction

This repository demonstrates a full real-time data engineering pipeline for stock market data using Kafka and AWS. The pipeline ingests streaming data, processes and transforms it, stores it in S3, and allows querying via Athena. It’s built to be scalable, modular, and maintainable.

---
## Architecture & Workflow

The system is composed of the following core components:

- **Producer / Ingestion**: Fetch raw stock market data and publish to Kafka topics.  
- **Kafka Messaging**: Acts as buffer / decoupling layer for downstream processing.  
- **Consumer / Processing**: Cleanse, transform, aggregate data (e.g. compute metrics, windows).  
- **Storage & Schema Management**: Processed data is stored in AWS S3; schema definitions and metadata managed with AWS Glue Catalog and Glue Crawler.  
- **Querying / Analytics**: Use AWS Athena to run SQL queries on stored data.  
- **Compute Environment**: Use EC2 instances for running producer or consumer scripts, deploying custom logic.
---
## Architecture 
<img src="Architecture.jpg">

## Technologies Used

| Component                  | Technology / Tool                                                         |
|----------------------------|----------------------------------------------------------------------------|
| Programming Language       | **Python**                                                                 |
| Cloud / Storage            | **AWS** – S3, Glue Crawler, Glue Catalog, Athena, EC2                     |
| Streaming / Messaging      | **Apache Kafka**                                                           |
| Data Processing / Querying | Python scripts; SQL via AWS Athena 


## Dataset Used
You can use any dataset, we are mainly interested in operation side of Data Engineering (building data pipeline) 

Here is the dataset used in the video - https://github.com/shanmukhi-developer/stock-market-kafka-de-project/blob/main/indexProcessed.csv
