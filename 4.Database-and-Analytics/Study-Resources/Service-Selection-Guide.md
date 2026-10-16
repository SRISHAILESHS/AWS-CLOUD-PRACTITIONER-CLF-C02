# AWS Database and Analytics — Service Selection Guide

## Which AWS service should I choose?

| Requirement | AWS Service | Reason |
|---|---|---|
| Run a relational database | Amazon RDS | Managed relational database |
| Automatically adjust Aurora database capacity | Aurora Serverless | Automatically scales database capacity |
| Store key-value or document data | DynamoDB | Managed NoSQL database |
| Speed up frequently accessed data | ElastiCache | In-memory caching |
| Analyze large datasets using SQL | Redshift | Data warehouse for analytics |
| Process huge datasets using Spark | Amazon EMR | Big-data processing |
| Query files in S3 using SQL | Amazon Athena | Serverless interactive queries |
| Clean and transform data | AWS Glue | Data integration and ETL |
| Build business dashboards | Amazon QuickSight | Business intelligence and visualization |

## Real-World Decision Examples

### Scenario 1: Online Shopping Website
Choose RDS or Aurora when the application needs relational data such as customers, orders, and payments.

### Scenario 2: Gaming Application
Choose DynamoDB when the application needs scalable access to player profiles and game scores.

### Scenario 3: Sales Reports Stored in S3
Choose Athena when you want to run SQL queries directly against supported data files in S3.

### Scenario 4: Company-Wide Business Analytics
Choose Redshift when you need a data warehouse for large-scale analytical queries.

### Scenario 5: Huge Data Processing Job
Choose EMR when you need to run big-data frameworks such as Spark or Hadoop.

### Scenario 6: Business Dashboard
Choose QuickSight to display business data in charts, reports, and dashboards.

## Important Difference

**Storing data is not the same as analyzing data.**

- RDS and DynamoDB support application data operations.
- S3 stores objects and files.
- Athena queries supported data files in S3.
- EMR processes large datasets.
- Redshift supports data warehousing and analytics.
- QuickSight visualizes data.

A solution may combine multiple services depending on its requirements.