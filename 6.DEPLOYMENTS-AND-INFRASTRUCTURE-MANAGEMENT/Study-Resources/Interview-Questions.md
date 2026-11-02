# AWS Deployment Services — Interview Questions

## Basic Questions

### 1. What is AWS CloudFormation?
CloudFormation is an Infrastructure as Code service that creates, updates, and manages AWS resources using templates.

### 2. What is a CloudFormation stack?
A stack is a collection of AWS resources managed together by CloudFormation.

### 3. What is AWS CDK?
CDK lets developers define cloud infrastructure using programming languages and synthesizes CloudFormation templates.

### 4. What is Elastic Beanstalk?
Elastic Beanstalk simplifies application deployment and environment management on AWS.

### 5. What is AWS CodeDeploy?
CodeDeploy automates application deployments to supported targets.

### 6. What is AWS CodeCommit?
CodeCommit is a managed Git source-control service for private repositories.

### 7. What is AWS CodeBuild?
CodeBuild is a managed service for building and testing source code.

### 8. What is AWS CodePipeline?
CodePipeline automates software release workflows by connecting pipeline stages.

### 9. What is AWS CodeArtifact?
CodeArtifact stores and shares software packages and dependencies.

### 10. What is AWS Systems Manager?
Systems Manager helps centrally operate and manage AWS resources and supported hybrid environments.

### 11. What is Session Manager?
Session Manager provides managed access to supported instances without requiring inbound SSH ports, when configured correctly.

### 12. What is Parameter Store?
Parameter Store stores configuration data and supports encrypted `SecureString` parameters.

## Scenario-Based Questions

### 13. You need to create the same infrastructure repeatedly. Which service can help?
AWS CloudFormation, because templates can be reused to create consistent infrastructure.

### 14. You want to simplify deploying a web application. Which service can help?
Elastic Beanstalk.

### 15. You need a managed service to build and test code. Which service can help?
AWS CodeBuild.

### 16. You want to automate a software release workflow. Which service can help?
AWS CodePipeline.

### 17. You need to automate deploying an application to EC2 instances. Which service can help?
AWS CodeDeploy.

### 18. You need to access a supported EC2 instance without opening inbound SSH. Which service can help?
Systems Manager Session Manager, provided the instance, IAM permissions, and connectivity are configured.

### 19. You need to store application configuration centrally. Which service can help?
Systems Manager Parameter Store.

### 20. You want to define infrastructure in Python. Which service can help?
AWS CDK.
