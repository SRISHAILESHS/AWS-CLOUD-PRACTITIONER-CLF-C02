# Docker – Complete Beginner Notes

## 1. What is Docker?

Docker is a platform used to package an application and everything it needs to run into a unit called a **container**.

A container includes the application code, libraries, dependencies, and configuration needed to run the application.

**Simple meaning:** Docker helps an application run consistently on different computers and servers.

## 2. Real-Time Example

Imagine you developed an Employee Management System on your laptop.

It works perfectly on your computer, but when you move it to an EC2 server, some dependencies or configurations may be missing.

Docker helps solve this problem by packaging the application and its required dependencies into a container.

## 3. Important Docker Terms

### Docker Image
An image is a template used to create containers.

Example: An image containing Node.js and the application setup.

### Docker Container
A container is a running instance of a Docker image.

Example: Your Employee Management System running inside a container.

### Dockerfile
A Dockerfile contains instructions to build a Docker image.

Example: Instructions to install dependencies and start your Node.js application.

### Docker Hub
Docker Hub is an online registry where Docker images can be stored and shared.

Example: Downloading an official Node.js image.

### Docker Engine
Docker Engine is the software that builds and runs containers.

## 4. Docker Image vs Container

| Docker Image | Docker Container |
|---|---|
| A template | A running instance of an image |
| Used to create containers | Runs the application |
| Similar to a recipe | Similar to the prepared dish |

## 5. What is a Dockerfile?

A Dockerfile contains instructions for building a Docker image.

Example:

```dockerfile
FROM node:22
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "server.js"]
```

Explanation:

- `FROM` – Specifies the base image.
- `WORKDIR` – Sets the working directory.
- `COPY` – Copies files into the image.
- `RUN` – Executes a command while building the image.
- `EXPOSE` – Documents the port the application uses.
- `CMD` – Specifies the default command to start the application.

This example assumes the project has a `package.json` file and a `server.js` file.

## 6. What is a Docker Registry?

A Docker registry stores Docker images.

Examples:
- Docker Hub
- Amazon Elastic Container Registry (Amazon ECR)

Amazon ECR is an AWS service used to store and manage container images.

## 7. Docker in AWS

Docker can be used with several AWS services.

| AWS Service | Purpose |
|---|---|
| Amazon EC2 | Run Docker containers on a virtual server where Docker is installed |
| Amazon ECS | Manage and run containers |
| Amazon EKS | Run containerized applications using Kubernetes |
| AWS Fargate | Run containers without managing the underlying servers |
| Amazon ECR | Store Docker images |

## 8. Docker vs Virtual Machine

| Docker Container | Virtual Machine |
|---|---|
| Shares the host operating system kernel | Runs its own guest operating system |
| Generally lightweight | Generally uses more resources |
| Usually starts quickly | Usually takes longer to start |
| Packages an application and its dependencies | Provides a complete virtualized machine |

## 9. Benefits of Docker

1. Consistent application environments.
2. Easier application deployment.
3. Portable application packaging.
4. Efficient resource usage compared with many full virtual machines.
5. Easier scaling when used with container orchestration services.
6. Helps teams develop and deploy applications consistently.

## 10. Docker vs Amazon ECS

Docker packages and runs applications in containers.

Amazon ECS is an AWS container orchestration service that helps manage and run containers across infrastructure such as EC2 or AWS Fargate.

**Remember:** Docker creates and runs containers; ECS helps manage containerized applications.

## 11. Docker Workflow

1. Write the application code.
2. Create a Dockerfile.
3. Build a Docker image.
4. Run a container from the image.
5. Test the application.
6. Push the image to a registry such as Amazon ECR.
7. Deploy the container using EC2, ECS, or another suitable platform.

## 12. Important Points to Remember

- Docker image = template.
- Docker container = running instance of an image.
- Dockerfile = instructions to build an image.
- Docker Hub = online image registry.
- Amazon ECR = AWS container image registry.
- Amazon ECS = container orchestration service.
- AWS Fargate = serverless compute for containers.
- Containers are not automatically serverless; they still need a runtime environment.

## Conclusion

Docker simplifies application packaging and deployment. In AWS, Docker can be combined with Amazon ECR, ECS, EC2, and Fargate to deploy and manage containerized applications.¬