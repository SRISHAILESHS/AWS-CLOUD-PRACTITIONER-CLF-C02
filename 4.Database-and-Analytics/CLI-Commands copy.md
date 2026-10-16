# AWS CLI Commands — Database & Analytics

> Replace the example values with your own. Commands may require AWS CLI configuration, permissions, and a resource in the correct Region. Some commands can create billable resources.

## Amazon RDS

List RDS database instances:

```bash
aws rds describe-db-instances
```

List available RDS engine versions:

```bash
aws rds describe-db-engine-versions
```

View DB snapshots:

```bash
aws rds describe-db-snapshots
```

## Amazon DynamoDB

List DynamoDB tables:

```bash
aws dynamodb list-tables
```

Describe a table:

```bash
aws dynamodb describe-table --table-name YOUR_TABLE_NAME
```

Scan a table (can consume read capacity and return a large amount of data):

```bash
aws dynamodb scan --table-name YOUR_TABLE_NAME
```

## Amazon ElastiCache

List ElastiCache replication groups:

```bash
aws elasticache describe-replication-groups
```

List ElastiCache clusters:

```bash
aws elasticache describe-cache-clusters
```

## Amazon Redshift

List Redshift clusters:

```bash
aws redshift describe-clusters
```

## AWS Glue

List Glue databases in the Data Catalog:

```bash
aws glue get-databases
```

List Glue crawlers:

```bash
aws glue list-crawlers
```

## AWS Database Migration Service (DMS)

List replication instances:

```bash
aws dms describe-replication-instances
```

List replication tasks:

```bash
aws dms describe-replication-tasks
```

## Region and help

Check the configured default Region:

```bash
aws configure get region
```

Get help for a command:

```bash
aws rds help
```

## Notes

- The AWS CLI does not provide a single simple command that covers every console workflow for every analytics service.
- `describe`, `list`, and `get` commands are generally for viewing configuration or metadata; create, modify, and delete commands can change resources or incur charges.
- Avoid putting database passwords or access keys directly into scripts or GitHub.
