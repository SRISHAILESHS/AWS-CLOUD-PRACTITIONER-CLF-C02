# EBS Snapshot

## What is an EBS Snapshot?

An EBS Snapshot is a point-in-time backup of an EBS volume.

It can be used to protect data and create a new EBS volume later.

### Simple Example

Imagine an EBS volume is like a hard disk.

```text
EBS Volume
   |
   | Create Snapshot
   ↓
EBS Snapshot
   |
   | Restore / Create Volume
   ↓
New EBS Volume
```

The snapshot acts as a backup of the EBS volume.

---

## Why Do We Use EBS Snapshots?

Snapshots are mainly used for:

* Backup
* Data protection
* Disaster recovery
* Creating new EBS volumes
* Migrating data
* Creating AMIs

---

## Real-Time Example

Suppose an EC2 instance has a 20 GB EBS volume containing important application data.

Before making a major change, we can create a snapshot.

```text
EC2
 |
20 GB EBS
 |
Create Snapshot
 |
Backup
```

If something goes wrong later, we can use the snapshot to create a new EBS volume.

---

## Snapshot vs EBS Volume

| Feature                   | EBS Volume        | EBS Snapshot       |
| ------------------------- | ----------------- | ------------------ |
| Purpose                   | Store active data | Backup data        |
| Used directly by EC2      | Yes               | No                 |
| Storage                   | Block storage     | Backup of EBS data |
| Can attach to EC2         | Yes               | No                 |
| Can create another volume | Yes               | Yes, from snapshot |
| Main use                  | Active storage    | Backup/recovery    |

---

## Snapshot Workflow

```text
EBS Volume
     ↓
Create Snapshot
     ↓
Snapshot stored by AWS
     ↓
Create new EBS Volume
     ↓
Attach new volume to EC2
```

---

## Important Point

A snapshot is **not the same as an EBS volume**.

An EBS volume is used as active storage.

A snapshot is used as a backup from which a new EBS volume can be created.

---

## Incremental Snapshots

EBS snapshots are incremental.

After the first snapshot, later snapshots store only the blocks that have changed since the previous snapshot.

Example:

```text
First Snapshot
100 GB

Second Snapshot
Only changed blocks are backed up

Third Snapshot
Only newly changed blocks are backed up
```

This makes repeated snapshots more efficient than creating a completely new full copy each time.

---

## Snapshot and Availability Zone

An EBS volume exists in a specific Availability Zone.

A snapshot is different: it can be used to create a new EBS volume in an Availability Zone of your choice within the supported Region.

Example:

```text
Snapshot
   |
   ├── Create Volume → eu-west-1a
   |
   └── Create Volume → eu-west-1b
```

---

## Snapshot Best Practice

Before creating a snapshot of important application data, make sure the data is in a consistent state.

For databases and applications with active writes, application-aware backup procedures may be needed for a reliable recovery point.

---

## Interview Answer

### What is an EBS Snapshot?

"An EBS Snapshot is a point-in-time backup of an EBS volume. It is mainly used for backup, recovery, and creating new EBS volumes."

### What is the difference between EBS and Snapshot?

"EBS is active block storage attached to an EC2 instance, whereas a snapshot is a backup of an EBS volume that can be used to create a new volume."

### What is an incremental snapshot?

"After the first snapshot, subsequent snapshots store only the blocks that have changed since the previous snapshot."
