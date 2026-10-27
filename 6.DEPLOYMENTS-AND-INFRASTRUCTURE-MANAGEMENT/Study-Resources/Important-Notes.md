# AWS Deployments and Infrastructure Management — Important Notes

## 1. AWS CloudFormation
CloudFormation creates, updates, and manages AWS resources using templates.
- **Template:** YAML or JSON blueprint defining resources.
- **Stack:** Collection of resources managed together.
- **Benefit:** Automates infrastructure creation and supports template reuse.

## 2. AWS CDK
AWS Cloud Development Kit (CDK) lets developers define cloud infrastructure using programming languages such as TypeScript, Python, and Java. CDK synthesizes CloudFormation templates.

## 3. AWS Elastic Beanstalk
Elastic Beanstalk simplifies application deployment and environment management. AWS provisions and manages much of the underlying environment for you.

## 4. AWS CodeDeploy
CodeDeploy automates application deployments to supported targets, including EC2 instances, on-premises servers, and supported serverless compute resources.

## 5. AWS CodeCommit
CodeCommit is AWS's managed Git source-control service for hosting private Git repositories.

## 6. AWS CodeBuild
CodeBuild is a managed build service that can compile source code, run tests, and produce build artifacts.

## 7. AWS CodePipeline
CodePipeline automates software release workflows by connecting source, build, test, and deployment stages.

## 8. AWS CodeArtifact
CodeArtifact is a managed repository service for storing, publishing, and sharing software packages and dependencies.

## 9. AWS Systems Manager (SSM)
Systems Manager helps centrally operate and manage AWS resources and supported hybrid environments.

## 10. SSM Session Manager
Session Manager provides managed access to supported instances through the AWS console or CLI without requiring inbound SSH ports. Correct instance setup, IAM permissions, and connectivity are required.

## 11. SSM Parameter Store
Parameter Store stores configuration data as parameters.
- Use it for application settings and configuration values.
- `SecureString` parameters use AWS KMS encryption for sensitive values.
- Configure IAM access carefully; do not expose secrets in source code.

## Quick Differences
- **CloudFormation:** Creates and manages infrastructure.
- **CDK:** Defines infrastructure using programming languages and generates CloudFormation templates.
- **Elastic Beanstalk:** Simplifies application deployment and environment management.
- **CodeDeploy:** Automates application deployments.
- **CodeBuild:** Builds and tests code.
- **CodePipeline:** Orchestrates release workflows.
- **CodeArtifact:** Stores software packages and dependencies.
- **Systems Manager:** Helps operate and manage resources.
- **Session Manager:** Provides managed instance access.
- **Parameter Store:** Stores configuration parameters and encrypted values.
