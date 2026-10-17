# AWS Compute Services — CLI Commands

These commands require the AWS CLI to be installed and configured with appropriate permissions.

## 1. Amazon ECS

List ECS clusters:

```bash
aws ecs list-clusters
```

List services in a cluster:

```bash
aws ecs list-services --cluster my-cluster
```

List running tasks:

```bash
aws ecs list-tasks --cluster my-cluster
```

## 2. AWS Lambda

List Lambda functions:

```bash
aws lambda list-functions
```

Get function details:

```bash
aws lambda get-function --function-name my-function
```

Invoke a function:

```bash
aws lambda invoke --function-name my-function response.json
```

## 3. AWS Batch

List job queues:

```bash
aws batch describe-job-queues
```

List compute environments:

```bash
aws batch describe-compute-environments
```

List jobs in a queue:

```bash
aws batch list-jobs --job-queue my-job-queue --job-status RUNNING
```

## 4. Amazon Lightsail

List Lightsail instances:

```bash
aws lightsail get-instances
```

List Lightsail blueprints:

```bash
aws lightsail get-blueprints
```

## Important
- Replace example names with actual AWS resource names.
- Configure the AWS CLI before running commands.
- Some commands require additional IAM permissions.
- Listing resources may incur no direct charge, but creating or running resources can incur charges.
- Check the AWS Region and your account before running commands.