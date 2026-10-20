# AWS Compute Services — Important Notes

## 1. Amazon ECS

- Full form: Amazon Elastic Container Service.
- Used to run and manage containers.
- Supports AWS Fargate and Amazon EC2 as compute options.
- A container packages an application and its dependencies.
- ECS can run applications without requiring you to manage the underlying servers when using Fargate.

**Remember:** ECS = Container management.

## 2. AWS Lambda

- Runs code without requiring you to manage servers.
- Executes code when triggered by an event or request.
- Uses a pay-for-use pricing model, subject to AWS pricing rules.
- Common triggers include S3 events, API Gateway requests, and EventBridge rules.
- Lambda functions have execution limits, so it is not suitable for every long-running workload.

**Remember:** Lambda = Event-driven serverless computing.

## 3. AWS Batch

- Runs batch computing jobs at scale.
- Can schedule and queue jobs.
- Automatically provisions and scales computing resources as needed.
- Supports job dependencies and job queues.
- Useful for scientific simulations, financial calculations, and large-scale data processing.

**Remember:** Batch = Run many computing jobs.

## 4. Amazon Lightsail

- Simplifies launching virtual private servers.
- Provides predictable monthly pricing plans for many common configurations.
- Useful for websites, blogs, and small applications.
- Offers simplified access to features such as storage, networking, and databases.
- Suitable for beginners who want simpler cloud hosting.

**Remember:** Lightsail = Easy cloud hosting.

## Important Differences

- ECS is designed for containerized applications.
- Lambda is designed for short-lived, event-driven code executions.
- Batch is designed for batch jobs that can be queued and processed.
- Lightsail is designed for simplified virtual server and application hosting.