# EBS vs EFS

## What is EBS?

Amazon EBS is block storage that is commonly attached to an EC2 instance.

Think of EBS as a virtual hard disk.

## What is EFS?

Amazon EFS is a managed file storage service that can be shared by multiple EC2 instances.

Think of EFS as a shared network folder.

---

## EBS vs EFS

| Feature      | EBS                               | EFS                             |
| ------------ | --------------------------------- | ------------------------------- |
| Full form    | Elastic Block Store               | Elastic File System             |
| Storage type | Block storage                     | File storage                    |
| Main use     | Virtual hard disk for EC2         | Shared file system              |
| Access       | Commonly used by one EC2 instance | Multiple EC2 instances          |
| Sharing      | Limited/specialized               | Designed for sharing            |
| Availability | Specific Availability Zone        | Regional service                |
| Example      | Database disk                     | Shared application files        |
| Scaling      | Modify volume size                | Automatically scales            |
| Backup       | EBS Snapshots                     | EFS backups/replication options |

---

## Real-Time Example

### EBS

Imagine you have one laptop.

You connect a 500 GB external hard disk to it.

That is similar to:

EC2 → EBS

EBS is useful when one EC2 instance needs its own block storage.

---

### EFS

Imagine an office has a shared network folder.

Multiple employees can access the same folder.

Similarly:

EC2-1 ──┐
│
EC2-2 ──┼── EFS
│
EC2-3 ──┘

Multiple EC2 instances can access the same EFS file system.

---

## Interview Answer

### When would you use EBS?

"I would use EBS when an EC2 instance needs persistent block storage, such as for an operating system, database, or application data."

### When would you use EFS?

"I would use EFS when multiple EC2 instances need to access the same files through a shared file system."

### One-Line Difference

**EBS = virtual hard disk for EC2**

**EFS = shared file system for multiple EC2 instances**
