# AWS Systems Manager (SSM)

## 1. What is AWS Systems Manager?

**AWS Systems Manager (SSM) is an AWS service that helps you centrally manage, operate, and automate tasks on your AWS resources and hybrid servers.**

In simple words, SSM lets you manage multiple EC2 instances and supported on-premises servers from one central place instead of manually connecting to each server.

### Real-world example

Imagine your company has 20 EC2 instances. You need to:

- Check information about the servers.
- Run a command on several servers.
- Install operating-system updates.
- Connect to a server to troubleshoot an issue.
- Manage application configuration values.

Systems Manager provides tools to perform these tasks centrally.

## 2. Important features of AWS Systems Manager

| Feature | What it does | Simple example |
|---|---|---|
| **Session Manager** | Opens a secure interactive terminal session to a managed instance through the AWS console or CLI. | Open an EC2 terminal without opening inbound SSH port 22. |
| **Run Command** | Runs commands or scripts remotely on one or more managed nodes. | Run `sudo yum update -y` on selected Linux servers. |
| **Patch Manager** | Helps automate operating-system patching. | Apply approved security updates to managed EC2 instances. |
| **State Manager** | Helps keep managed nodes in a defined configuration. | Make sure a required service or configuration stays in place. |
| **Automation** | Automates common operational tasks using runbooks. | Automate a sequence of maintenance steps. |
| **Inventory** | Collects metadata about managed nodes and their installed software. | Check operating-system versions and installed applications. |
| **Fleet Manager** | Provides a central interface to view and manage server details. | Review information about a group of EC2 instances. |
| **Parameter Store** | Stores configuration data and, when configured as SecureString, encrypted values. | Store an application setting or database password. |

## 3. How AWS Systems Manager works

The diagram below is the architecture illustration supplied for these notes.

![AWS Systems Manager architecture diagram](Screenshots/SSM-Architecture-Diagram.png)

### Explanation of the diagram

1. **SSM Agent:** The SSM Agent is software that runs on a managed server. It communicates with Systems Manager.
2. **EC2 instances:** Each EC2 instance that you want to manage must be set up as a managed node. The SSM Agent is commonly included in many AWS-provided AMIs, but you should verify that it is installed and running.
3. **On-premises servers:** Servers outside AWS can also be managed after they are configured for Systems Manager hybrid environments.
4. **Systems Manager:** You use the AWS console, CLI, or APIs to request management actions.
5. **Communication:** The SSM Agent initiates communication to the Systems Manager service endpoints. You normally do not need to open inbound SSH or RDP ports just for Systems Manager management.

### What is required for an EC2 instance to become a managed node?

- SSM Agent must be installed and running.
- The instance must have an IAM instance profile with the required Systems Manager permissions (for example, `AmazonSSMManagedInstanceCore`).
- The instance must be able to reach the required Systems Manager endpoints, usually through outbound HTTPS (port 443), an internet/NAT path, or configured VPC endpoints.
- The instance must be registered and appear as a managed node in Systems Manager.

**Important:** Installing the agent alone is not enough. IAM permissions and network connectivity are also required.

## 4. SSM Session Manager

### What is Session Manager?

**Session Manager lets you connect to a managed EC2 instance using a browser-based or CLI terminal session without requiring you to open inbound SSH or RDP ports.**

### Example

Suppose your Employee Management System is running on an Amazon Linux EC2 instance. You want to check its files or restart its Node.js application.

With Session Manager:

1. Open AWS Management Console.
2. Go to **Systems Manager → Session Manager**.
3. Choose **Start session**.
4. Select your managed EC2 instance.
5. Start the session and use the terminal.

You can then run commands such as:

```bash
whoami
pwd
ls
sudo systemctl status httpd
```

### Why is Session Manager useful?

- No need to expose inbound SSH port 22 or RDP port 3389 for the session.
- No need to distribute SSH keys for Session Manager access.
- Access can be controlled using IAM permissions.
- Session activity can be logged to supported AWS logging destinations when configured.

**Remember:** Session Manager is for securely accessing a managed node's terminal. The instance still needs the SSM Agent, permissions, and network connectivity.

## 5. SSM Parameter Store

### What is Parameter Store?

**Parameter Store is a capability of AWS Systems Manager that stores configuration data and secrets as parameters in a central place.**

In simple words, it is like a secure storage cabinet for application settings.

### Real-world example

Your Employee Management System needs:

- Database host
- Application environment name
- API endpoint
- Database password

Instead of hardcoding these values in your application code, you can store them as parameters and retrieve them when the application runs.

Example parameter names:

```text
/employee-app/database/host
/employee-app/environment
/employee-app/api-url
/employee-app/database/password
```

### Parameter types

| Type | Purpose |
|---|---|
| **String** | Stores ordinary text, such as an environment name. |
| **StringList** | Stores a comma-separated list of values. |
| **SecureString** | Stores sensitive values encrypted using AWS KMS. |

### Why use Parameter Store?

- Keeps configuration values in one central location.
- Avoids hardcoding settings in application source code.
- Supports access control through IAM.
- SecureString encrypts sensitive values at rest using AWS KMS.
- Applications and automation can retrieve parameters through AWS APIs or supported SDKs.

**Important:** SecureString values should only be accessible to identities that have the necessary permissions. Do not place passwords or secret values directly in source code or GitHub.

## 6. Session Manager vs Parameter Store

| Session Manager | Parameter Store |
|---|---|
| Used to connect to a managed server terminal. | Used to store configuration values and secrets. |
| Helps with server access and troubleshooting. | Helps applications retrieve settings. |
| Example: Open an EC2 terminal. | Example: Retrieve a database password. |

## 7. Interview questions

**Q1. What is AWS Systems Manager?**

AWS Systems Manager is a service that helps centrally manage, operate, and automate tasks across AWS resources and hybrid environments.

**Q2. What is SSM Agent?**

SSM Agent is software installed on a managed node that processes Systems Manager requests and communicates with the Systems Manager service.

**Q3. What is Session Manager?**

Session Manager provides secure interactive access to managed instances without requiring inbound SSH or RDP access.

**Q4. What is Run Command?**

Run Command allows administrators to execute commands remotely on one or more managed nodes.

**Q5. What is Parameter Store?**

Parameter Store is a Systems Manager capability for centrally storing configuration data and sensitive values, including encrypted SecureString parameters.

**Q6. Does Session Manager require SSH port 22 to be open?**

No. Session Manager does not require inbound SSH port 22 to be open. The managed node still needs the SSM Agent, suitable IAM permissions, and connectivity to Systems Manager endpoints.

## 8. Quick revision

- **Systems Manager:** Centrally manage AWS and hybrid servers.
- **SSM Agent:** Software on the managed server that communicates with Systems Manager.
- **Session Manager:** Connect to a server terminal.
- **Run Command:** Run commands remotely.
- **Patch Manager:** Manage operating-system patches.
- **Parameter Store:** Store application settings and encrypted values.

### One-line interview answer

**AWS Systems Manager is a management service that helps you securely operate, monitor, and automate tasks across EC2 instances and hybrid servers from one central place.**
