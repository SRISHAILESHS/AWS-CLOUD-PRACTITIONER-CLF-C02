# AWS CloudFormation

## What is CloudFormation?
AWS CloudFormation is an Infrastructure as Code (IaC) service that creates, updates, and manages AWS resources using templates.

## Important Terms
- **Template:** A YAML or JSON file defining the resources you want.
- **Stack:** A group of resources managed together.
- **Resource:** An AWS component, such as an S3 bucket or EC2 instance.
- **Change set:** A preview of proposed stack changes before they are applied.

## Benefits
1. **Productivity:** Automate infrastructure creation.
2. **Reuse:** Reuse templates instead of starting from scratch.
3. **Consistency:** Create environments using the same defined configuration.
4. **Fewer manual errors:** Reduce repetitive manual setup.
5. **Change visibility:** Review proposed changes with change sets.

## How it works
1. Write a CloudFormation template.
2. Create a stack from the template.
3. CloudFormation provisions the specified resources.
4. Update the template when changes are needed.

## Example
A template defines an S3 bucket. When you create a stack from that template, CloudFormation creates the bucket, subject to valid configuration and permissions.

## Hands-on
Follow `Hands-On-Lab.md` for a beginner S3 bucket exercise.
