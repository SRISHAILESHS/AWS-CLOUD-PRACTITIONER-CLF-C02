# AWS Deployment Services — Real-World Use Cases

## CloudFormation
A company needs similar development, test, and production infrastructure. It can reuse templates to create consistent resources.

## CDK
A developer prefers defining cloud infrastructure with a programming language such as Python or TypeScript. CDK synthesizes a CloudFormation template from that code.

## Elastic Beanstalk
A developer wants to deploy a web application while AWS handles much of the environment provisioning and management.

## CodeDeploy
A team wants to automate releasing a new application version to supported deployment targets.

## CodeCommit
A team wants a managed Git repository for private source-code collaboration.

## CodeBuild
A team wants to automatically install dependencies, run tests, build code, and generate artifacts.

## CodePipeline
A team wants to connect source, build, testing, and deployment into an automated release workflow.

## CodeArtifact
Several projects share internal libraries and dependencies. CodeArtifact provides a managed repository for supported package formats.

## Systems Manager
An operations team needs centralized tools for managing supported AWS and hybrid resources.

## Session Manager
An administrator needs controlled access to an instance without opening inbound SSH ports, with the required instance configuration and IAM permissions.

## Parameter Store
An application needs configuration values in a central location. Sensitive values can be stored as encrypted `SecureString` parameters with suitable access controls.
