# Hands-On Lab — Database & Analytics

Use the AWS Console for the following beginner-friendly practice. Follow the screenshots in the **Screenshots** folder for visual reference; individual screenshot filenames are intentionally not listed here.

## Lab 1: Explore Amazon RDS

1. Open the Amazon RDS console and choose the correct Region.
2. Explore database creation options and the supported database engines.
3. Learn the difference between Single-AZ and Multi-AZ deployments.
4. Review backup, storage, connectivity, and security settings.
5. Do not create a database unless you need it for practice and understand the cost.
6. If you create a resource, delete it after practice and confirm no billable resources remain.

**Key learning:** RDS is a managed relational database service; Multi-AZ is primarily for availability and failover, while read replicas are primarily for read scaling.

## Lab 2: Explore Amazon DynamoDB

1. Open the DynamoDB console.
2. Review how tables, partition keys, and optional sort keys work.
3. Explore the items view and the table's capacity and monitoring options.
4. If you create a test table, use a simple partition key such as `CustomerID`.
5. Add a sample item, inspect it, and delete the test table when finished.

**Key learning:** DynamoDB is a managed NoSQL database and does not require you to manage database servers.

## Lab 3: Explore analytics services

1. Open Amazon S3 and identify a test dataset or sample file.
2. Explore Amazon Athena and learn how it queries data stored in S3 using SQL.
3. Explore AWS Glue and the Data Catalog; learn how crawlers can discover schema.
4. Review Amazon Redshift as a data warehouse and Amazon QuickSight as a dashboard tool.
5. Explore Amazon EMR to understand managed big-data frameworks.

**Key learning:** Athena queries data in S3; Glue helps prepare/catalog data; Redshift is a data warehouse; QuickSight visualizes data.

## Lab 4: Explore migration and specialized databases

1. Review AWS DMS and the idea of source endpoints, target endpoints, and replication tasks.
2. Compare Amazon DocumentDB, Amazon Neptune, and Amazon Timestream by their data types and use cases.
3. Review Amazon Managed Blockchain at a high level.

**Key learning:** Pick the database based on the data model and workload, not just because all of them store data.

## Completion checklist

- [ ] I can explain RDS, Aurora, and DynamoDB.
- [ ] I can distinguish Multi-AZ from a read replica.
- [ ] I know when to use ElastiCache.
- [ ] I can distinguish Redshift from Athena.
- [ ] I can explain Glue, EMR, and QuickSight.
- [ ] I know the purpose of DMS.
- [ ] I checked for and removed any practice resources that could incur charges.
