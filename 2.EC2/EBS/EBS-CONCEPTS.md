# EBS Concepts

## 1. EBS Volume

An EBS volume is a virtual block storage device that can be attached to an EC2 instance.

Example:

EC2 Instance → 2 GB EBS Volume

The volume can be used to store application data, files, databases, and other information.

---

## 2. Availability Zone

Every EBS volume belongs to a specific Availability Zone.

Example:

EC2 → eu-west-1a

EBS → eu-west-1a

The EBS volume can normally be attached to the EC2 instance because both are in the same Availability Zone.

---

## 3. Persistent Storage

Persistent storage means the data can remain available independently of the temporary running state of the EC2 instance.

EBS is designed for persistent storage.

---

## 4. EBS Snapshot

A snapshot is a point-in-time backup of an EBS volume.

Example:

10 GB EBS Volume
↓
Snapshot
↓
Backup

A snapshot can be used to create a new EBS volume.

---

## 5. IOPS

IOPS means Input/Output Operations Per Second.

It represents the number of input/output operations that storage can handle per second.

Higher IOPS can be important for applications that perform many read and write operations.

---

## 6. Throughput

Throughput represents the amount of data that can be transferred over a period of time.

It is commonly measured in MB/s.

IOPS focuses on the number of operations.

Throughput focuses on the amount of data transferred.

---

## 7. EBS Encryption

EBS supports encryption to protect data stored on EBS volumes.

Encryption can help protect sensitive data from unauthorized access.

---

## 8. Root Volume

The root EBS volume normally contains the operating system of an EC2 instance.

Example:

EC2
|
└── Root EBS
└── Operating System

---

## 9. Additional EBS Volume

We can attach additional EBS volumes to an EC2 instance.

Example:

EC2
|
├── Root Volume – 8 GB
|
└── Data Volume – 20 GB

The additional volume can be used for application data.

---

## 10. Detaching an EBS Volume

An EBS volume can be detached from an EC2 instance.

After detaching, the volume can remain available and can potentially be attached to another compatible EC2 instance.

Important:

Before detaching a volume that is actively being used, make sure the data is safely unmounted and the application is not actively writing to it.

---

## 11. Resizing EBS

EBS volumes can be modified to increase their storage capacity.

Example:

Original volume:

20 GB

After modification:

50 GB

The filesystem inside the operating system may also need to be extended after increasing the volume size.

---

## 12. EBS Multi-Attach

Certain EBS volume types support Multi-Attach.

It allows a supported EBS volume to be attached to multiple EC2 instances within the same Availability Zone.

This is a specialized feature and should not be confused with normal EBS usage.

---

## 13. EBS Lifecycle

Basic EBS lifecycle:

Create Volume
↓
Attach to EC2
↓
Format
↓
Mount
↓
Store Data
↓
Snapshot / Backup
↓
Detach
↓
Delete when no longer required
