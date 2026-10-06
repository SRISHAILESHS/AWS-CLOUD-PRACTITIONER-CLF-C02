# Amazon EC2

## Overview

Amazon EC2 (Elastic Compute Cloud) is an AWS service that provides resizable compute capacity in the cloud.

An EC2 instance is a virtual server that can be used to run applications, websites, and other workloads.

## What I Learned

* What Amazon EC2 is
* What an EC2 instance means
* How to launch an EC2 instance
* EC2 instance types
* Amazon Machine Images (AMI)
* Key pairs
* Security Groups
* Instance states
* Public and private IP addresses
* Elastic IP addresses
* EBS storage
* EC2 pricing options
* Connecting to an EC2 instance
* Terminating an EC2 instance

## Important EC2 Components

### AMI

An Amazon Machine Image (AMI) is a template used to create an EC2 instance. It contains the operating system and other required software.

### Instance Type

The instance type determines the computing resources available to the EC2 instance, such as CPU, memory, and networking capacity.

### Key Pair

A key pair is used to securely connect to an EC2 instance.

### Security Group

A security group acts as a virtual firewall that controls inbound and outbound traffic for an EC2 instance.

### EBS

Amazon Elastic Block Store (EBS) provides persistent block storage for EC2 instances.

## EC2 Instance Lifecycle

An EC2 instance can have different states:

* Pending
* Running
* Stopping
* Stopped
* Shutting-down
* Terminated

## Hands-On Practice

I launched and configured an EC2 instance using the AWS Management Console.

See [Hands-On Lab](Hands-On-Lab.md) for the steps and screenshots.

## CLI Commands

Common AWS CLI commands used with EC2 are documented in [CLI Commands](CLI-Commands.md).

## Key Takeaway

EC2 provides virtual servers in AWS that allow users to run applications without purchasing and maintaining physical servers.
