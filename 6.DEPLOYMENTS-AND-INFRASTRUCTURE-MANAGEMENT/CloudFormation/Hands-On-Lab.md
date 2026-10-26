# CloudFormation Hands-On Lab: Create an S3 Bucket

## Objective
Create an Amazon S3 bucket using a CloudFormation template.

## Prerequisites
- An AWS account.
- Access to the CloudFormation console.
- Permission to create stacks and S3 buckets.

## Step 1: Create the template
Create a file named `s3-bucket.yaml` with this content:

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Create an S3 bucket using CloudFormation

Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Sub 'cf-lab-${AWS::AccountId}-${AWS::Region}'
```

The name includes the account ID and Region to reduce naming conflicts. S3 bucket names must meet S3 naming rules and be unique within the applicable partition.

## Step 2: Create the stack
1. Sign in to the AWS Management Console.
2. Open CloudFormation.
3. Choose **Create stack** and select the option to use an existing template.
4. Upload `s3-bucket.yaml`.
5. Enter the stack name `MyFirstS3Stack`.
6. Continue through the pages, review the settings, and submit the stack.

## Step 3: Verify
1. Open the stack and check its status.
2. Wait for `CREATE_COMPLETE`.
3. Open Amazon S3 and confirm that the bucket exists.

## Step 4: Understand the result
- Template: `s3-bucket.yaml`
- Stack: `MyFirstS3Stack`
- Resource: S3 bucket
- Service: CloudFormation

## Step 5: Clean up
When finished, delete the stack from CloudFormation to avoid leaving unused resources. Check the resources before deletion. Stack deletion can delete the bucket; if it contains objects, empty it first.

## Learning outcome
I learned how CloudFormation provisions an AWS resource from a reusable template.
