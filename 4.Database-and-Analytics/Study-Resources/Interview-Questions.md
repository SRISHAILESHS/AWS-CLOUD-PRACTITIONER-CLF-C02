# AWS Database and Analytics — Interview Questions

## 1. Basic Questions

### Q1. What is Amazon RDS?
Amazon RDS is a managed relational database service. AWS handles many routine database administration tasks.

**Example:** Storing customer and order details for an online shop.

### Q2. What is Amazon Aurora?
Aurora is an AWS relational database engine compatible with MySQL and PostgreSQL.

### Q3. What is the difference between Multi-AZ and Read Replica?
- Multi-AZ: Improves database availability and supports failover.
- Read Replica: Helps handle additional read queries.

### Q4. What is Amazon DynamoDB?
DynamoDB is a fully managed NoSQL database designed for scalable application workloads.

### Q5. What is Amazon ElastiCache?
ElastiCache is a managed in-memory caching service that helps retrieve frequently accessed data quickly.

### Q6. What is Amazon Redshift?
Redshift is a data warehouse used to analyze large amounts of business data.

### Q7. What is Amazon Athena?
Athena allows users to query data stored in Amazon S3 using SQL without managing query servers.

### Q8. What is AWS Glue?
Glue is a data integration service used to discover, prepare, and transform data for analytics.

### Q9. What is AWS DMS?
Database Migration Service helps migrate databases between supported source and target systems.

### Q10. What is Amazon QuickSight?
QuickSight is a business intelligence service used to create dashboards, visualizations, and reports.

## 2. Scenario-Based Questions

### Q11. A website needs a relational database with automatic failover support. Which feature can help?
**Answer:** Amazon RDS Multi-AZ deployment.

### Q12. A website receives many read requests for product details. What can help scale database reads?
**Answer:** RDS Read Replicas, where supported by the database configuration.

### Q13. A shopping application needs a scalable NoSQL database for cart information. Which service is suitable?
**Answer:** Amazon DynamoDB.

### Q14. A website repeatedly requests the same popular product details. Which service can reduce repeated database queries?
**Answer:** Amazon ElastiCache.

### Q15. A company wants to analyze years of sales data for business trends. Which service is suitable?
**Answer:** Amazon Redshift.

### Q16. A company stores CSV log files in S3 and wants to query them using SQL. Which service should it consider?
**Answer:** Amazon Athena.

### Q17. A manager wants visual sales dashboards. Which service is suitable?
**Answer:** Amazon QuickSight.

### Q18. A company needs to migrate an existing database to AWS. Which service can help?
**Answer:** AWS Database Migration Service (DMS).

### Q19. A company needs to clean and transform data before analysis. Which service can help?
**Answer:** AWS Glue.

### Q20. A social network needs to analyze relationships between people. Which database is suitable?
**Answer:** Amazon Neptune, a graph database.

## 3. Important Comparisons

| Services | Main difference |
|---|---|
| RDS vs DynamoDB | Relational database vs NoSQL database |
| Multi-AZ vs Read Replica | Availability vs read scaling |
| ElastiCache vs DynamoDB | In-memory cache vs persistent NoSQL database |
| Redshift vs Athena | Data warehouse vs SQL queries against data in S3 |
| Glue vs DMS | Data integration and transformation vs database migration |
| DocumentDB vs Neptune | Document data vs graph relationships |

## 4. Quick Revision

- Relational database: RDS
- Cloud-optimized relational engine: Aurora
- High availability: Multi-AZ
- Read scaling: Read Replica
- In-memory cache: ElastiCache
- NoSQL database: DynamoDB
- Data warehouse: Redshift
- SQL on S3: Athena
- Big-data processing: EMR
- Data dashboards: QuickSight
- Data integration: Glue
- Database migration: DMS
- Graph database: Neptune
- Time-series database: Timestream
- Document database: DocumentDB

## 5. Practical Evidence

Add screenshots here only after completing the corresponding AWS activity.

Suggested activities:
- Create an RDS database and record its configuration.
- Explore a DynamoDB table.
- Explore S3 data using Athena.
- Create a sample Glue Data Catalog entry.

Do not upload AWS account IDs, passwords, access keys, database credentials, or other secrets in screenshots.

