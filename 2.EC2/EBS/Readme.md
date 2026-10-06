# Amazon EBS – Elastic Block Store

## What is Amazon EBS?

Amazon Elastic Block Store (EBS) is a block-level storage service provided by AWS for EC2 instances.

It works like a hard disk or SSD attached to an EC2 instance.

We can use EBS to store:

* Operating system files
* Application files
* Databases
* Documents
* Images and videos
* Other important data

---

## Real-Time Example

Think of an EC2 instance as a computer.

The EC2 instance has storage for running the operating system and applications.

If we need additional storage, we can attach an EBS volume to the EC2 instance.

### Simple Example

EC2 = Computer

EBS = Additional hard disk

Attach EBS = Connect the hard disk to the computer

Mount EBS = Make the storage available for use

---

## Why Do We Use EBS?

EBS is mainly used when an EC2 instance needs persistent storage.

For example:

An EC2 instance is running a website.

The website stores:

* Images
* User data
* Application files

Instead of keeping all the data only on temporary instance storage, we can store it on an EBS volume.

---

## Important EBS Features

### 1. Persistent Storage

EBS data remains available even if the EC2 instance is stopped.

For example:

EC2 Instance
↓
EBS Volume
↓
Application Data

If the EC2 instance is stopped, the EBS volume can retain the data.

---

### 2. Attached to EC2

An EBS volume can be attached to an EC2 instance.

Example:

EC2 Instance
|
|
EBS
10 GB

---

### 3. Availability Zone

An EBS volume is created in a specific Availability Zone.

For example:

Region: Europe (Ireland)

Availability Zone:

eu-west-1a

The EBS volume must normally be in the same Availability Zone as the EC2 instance to attach it.

Example:

EC2 → eu-west-1a

EBS → eu-west-1a

This can be attached.

---

## EBS Volume

An EBS volume is a virtual hard disk that can be attached to an EC2 instance.

Example:

Volume Type: gp3

Size: 2 GiB

Availability Zone: eu-west-1a

---

## Common EBS Volume Types

### General Purpose SSD – gp3

Used for most general workloads.

Examples:

* Web applications
* Development environments
* Small databases

### Provisioned IOPS SSD

Used when applications require high and consistent I/O performance.

Examples:

* Large databases
* Critical applications

### Throughput Optimized HDD

Used for workloads that require high throughput.

### Cold HDD

Used for less frequently accessed workloads.

---

## EBS Snapshot

An EBS snapshot is a point-in-time backup of an EBS volume.

Example:

EBS Volume
10 GB
↓
Create Snapshot
↓
Backup

If the original EBS volume is lost or damaged, the snapshot can be used to create a new EBS volume.

### Real-Time Example

Imagine you have a hard disk containing important company files.

Before making major changes, you create a backup.

That backup is similar to an EBS snapshot.

---

## EBS Encryption

EBS volumes can be encrypted to protect stored data.

Encryption helps protect sensitive information stored on the volume.

Example:

EC2
↓
Encrypted EBS
↓
Protected Data

---

## IOPS

IOPS means:

Input/Output Operations Per Second.

It represents how many input/output operations a storage system can perform per second.

Example:

If a storage system supports higher IOPS, it can handle more storage operations per second.

IOPS is especially important for applications such as databases.

---

## EBS and EC2

EBS is commonly used with EC2.

Example:

EC2 Instance
|
├── Root EBS Volume
|
└── Additional EBS Volume

The root volume normally contains the operating system.

An additional EBS volume can be used to store application data.

---

## Basic EBS Practical Steps

1. Open AWS Console.
2. Open EC2.
3. Go to Elastic Block Store → Volumes.
4. Click Create volume.
5. Select the volume type.
6. Select the size.
7. Select the Availability Zone.
8. Create the volume.
9. Select the volume.
10. Choose Actions → Attach volume.
11. Select the EC2 instance.
12. Attach the volume.
13. Connect to the EC2 instance.
14. Check the disk using `lsblk`.
15. Format the volume if required.
16. Create a mount directory.
17. Mount the EBS volume.
18. Verify the storage using `df -h`.

---

## Important Commands

Check available disks:

```bash
lsblk
```

Format the EBS volume:

```bash
sudo mkfs -t ext4 /dev/xvdf
```

Create a directory:

```bash
sudo mkdir /data
```

Mount the volume:

```bash
sudo mount /dev/xvdf /data
```

Check mounted storage:

```bash
df -h
```

---

## EBS vs Instance Store

| Feature                  | EBS                       | Instance Store                |
| ------------------------ | ------------------------- | ----------------------------- |
| Storage type             | Persistent block storage  | Temporary local storage       |
| Data after instance stop | Retained                  | Depends on instance lifecycle |
| Can be detached          | Yes                       | No                            |
| Backup                   | Snapshots                 | No EBS snapshots              |
| Use case                 | Important persistent data | Temporary data/cache          |
| Connected to             | EC2                       | EC2 host                      |

---

## Important Interview Point

### What is EBS?

EBS is a persistent block storage service used with EC2 instances to store operating system files, application data, databases, and other information.

### Simple Interview Answer

"Amazon EBS is a persistent block storage service for EC2. It works like a virtual hard disk that can be attached to an EC2 instance and used to store data. EBS volumes can also be backed up using snapshots."

---

## EBS Learning Progress

* [ ] Understand EBS
* [ ] Create an EBS volume
* [ ] Understand Availability Zones
* [ ] Attach EBS to EC2
* [ ] Check the volume using `lsblk`
* [ ] Format the volume
* [ ] Mount the volume
* [ ] Store data
* [ ] Understand EBS snapshots
* [ ] Understand EBS encryption
* [ ] Understand IOPS
* [ ] Understand EBS volume types
* [ ] Understand EBS vs Instance Store
* [ ] Understand EBS vs EFS
