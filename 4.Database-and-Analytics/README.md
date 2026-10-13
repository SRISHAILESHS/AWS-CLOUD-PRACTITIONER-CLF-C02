# AWS Database & Analytics

This folder contains concise, interview-focused notes for the **AWS Cloud Practitioner CLF-C02** Database and Analytics section.

## Important topics to study

1. **Amazon RDS** – Managed relational databases; AWS handles routine administration such as backups and patching.
2. **Amazon Aurora** – AWS-built relational database compatible with MySQL and PostgreSQL.
3. **RDS deployment options** – Understand Single-AZ, Multi-AZ, and read replicas.
4. **Amazon DynamoDB** – Serverless, managed NoSQL key-value/document database.
5. **Amazon ElastiCache** – In-memory caching using engines such as Redis OSS and Memcached.
6. **Amazon Redshift** – Data warehouse for analytics over large datasets.
7. **Amazon Athena** – Run SQL queries on data in Amazon S3 without managing servers.
8. **AWS Glue** – Discover, prepare, transform, and integrate data for analytics.
9. **Amazon EMR** – Managed big-data processing using frameworks such as Apache Spark.
10. **AWS Database Migration Service (DMS)** – Migrate databases with minimal downtime in many supported migration scenarios.
11. **Amazon QuickSight** – Create business intelligence dashboards and visualizations.

## Quick service selection

| Requirement | AWS service |
|---|---|
| Traditional SQL database managed by AWS | Amazon RDS |
| MySQL/PostgreSQL-compatible cloud-optimized relational database | Amazon Aurora |
| Very low-latency key-value/document NoSQL database | Amazon DynamoDB |
| Speed up frequent database reads with cached data | Amazon ElastiCache |
| Analyze large datasets in a data warehouse | Amazon Redshift |
| Query files stored in S3 using SQL | Amazon Athena |
| Prepare and catalog data for analytics | AWS Glue |
| Process big data using Spark and related frameworks | Amazon EMR |
| Build dashboards and business reports | Amazon QuickSight |
| Migrate databases to AWS | AWS DMS |
| Store and query document data with MongoDB compatibility | Amazon DocumentDB |
| Work with connected data such as people, places, and relationships | Amazon Neptune |
| Store and analyze time-series data | Amazon Timestream |
| Create and manage blockchain networks | Amazon Managed Blockchain |

## Screenshot reference

For console screenshots from hands-on practice, refer to the **Screenshots** folder. Screenshot filenames are intentionally not listed in these notes.

## Exam tip

Choose the service based on the main requirement: **relational, NoSQL, cache, data warehouse, SQL query on S3, ETL, big-data processing, dashboard, or migration**. Do not confuse Amazon RDS with DynamoDB, or Redshift with Athena.
