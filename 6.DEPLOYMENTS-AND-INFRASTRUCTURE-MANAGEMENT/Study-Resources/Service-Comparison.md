# AWS Service Comparison

| Service | Main purpose | Easy example |
|---|---|---|
| CloudFormation | Create and manage infrastructure from templates | Create an S3 bucket and security group from a template |
| CDK | Define infrastructure using programming languages | Define an EC2 instance in Python |
| Elastic Beanstalk | Simplify application deployment | Deploy a web application |
| CodeDeploy | Automate application deployments | Release a new version to EC2 |
| CodeCommit | Host Git repositories | Store source code in a managed Git repository |
| CodeBuild | Build and test code | Run tests and produce build artifacts |
| CodePipeline | Automate release workflows | Connect source, build, and deployment stages |
| CodeArtifact | Store software packages | Share application libraries |
| Systems Manager | Operate and manage resources | Manage a fleet of instances |
| Session Manager | Access supported managed instances | Connect without opening inbound SSH |
| Parameter Store | Store configuration parameters | Store app settings and encrypted values |

## Typical CI/CD Flow
1. **Source:** A supported source provider stores the code.
2. **Build:** CodeBuild builds and tests it.
3. **Deploy:** CodeDeploy or another supported deployment provider releases it.
4. **Orchestration:** CodePipeline connects and automates the stages.

These services can be integrated, but they are not the only possible choices in a pipeline.
