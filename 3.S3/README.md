# Amazon S3 – Simple Storage Service

## 📌 What is Amazon S3?

Amazon S3 (Simple Storage Service) is an AWS **object storage service** used to store and retrieve data such as:

* Images
* Videos
* Documents
* PDFs
* Backups
* Application files
* Log files

### Simple Definition

> **Amazon S3 is a highly scalable object storage service used to store and retrieve files from the cloud.**

---

# 🌍 Real-Time Example

Imagine I have an online clothing website.

The website contains:

```text
Dress Images
Saree Images
Product Videos
Customer Bills
Product Documents
```

Instead of storing all these files on the application server, I can store them in an **S3 bucket**.

```text
Customer
    ↓
Online Shopping Website
    ↓
Amazon S3
    ↓
S3 Bucket
    ├── dress.jpg
    ├── saree.jpg
    ├── product-video.mp4
    └── invoice.pdf
```

When a customer opens a product page, the application can retrieve the required image from S3.

---

# 🪣 What is a Bucket?

A **bucket** is a container used to store objects in Amazon S3.

Think of a bucket like a **folder/container in the cloud**.

```text
S3
│
└── Bucket
    │
    ├── image.jpg
    ├── video.mp4
    ├── document.pdf
    └── backup.zip
```

### Example

```text
Bucket Name:
vaishnavi-boutique-products
```

The bucket can contain product images, videos and other files.

---

# 📦 What is an Object?

An **object is the actual data/file stored inside an S3 bucket.**

Examples:

```text
dress.jpg
invoice.pdf
product.mp4
backup.zip
```

So remember:

```text
Bucket = Container
Object = File
```

---

# 🧠 S3 Structure

```text
Amazon S3
   │
   └── Bucket
         │
         ├── Object
         ├── Object
         ├── Object
         └── Object
```

---

# ⭐ Important S3 Terms

| Term          | Meaning                                                |
| ------------- | ------------------------------------------------------ |
| S3            | Amazon Simple Storage Service                          |
| Bucket        | Container for storing objects                          |
| Object        | Actual file/data                                       |
| Object Key    | Name/path used to identify an object                   |
| Region        | AWS location where the bucket is created               |
| Storage Class | Different storage options based on access requirements |

---

# 📍 S3 Bucket Region

When creating an S3 bucket, we select an AWS Region.

Example:

```text
India → Mumbai
Region → ap-south-1
```

The bucket is created in the selected Region.

### Real-Time Example

If an Indian company mainly has customers in India, it may choose a Region close to its users and application infrastructure.

---

# 🗂️ S3 is Object Storage

S3 is different from EBS.

### EBS

```text
EC2
 ↓
EBS
 ↓
Block Storage
```

EBS is mainly used as storage attached to an EC2 instance.

### S3

```text
Application
     ↓
    S3
     ↓
Object Storage
```

S3 stores files as objects in buckets.

---

# 🔥 S3 vs EBS

| Feature      | S3                      | EBS             |
| ------------ | ----------------------- | --------------- |
| Storage type | Object storage          | Block storage   |
| Main purpose | Store files/data        | Storage for EC2 |
| Container    | Bucket                  | Volume          |
| Example      | Images, videos, backups | EC2 disk        |
| Access       | Through APIs/URLs/tools | Attached to EC2 |
| Scalability  | Highly scalable         | Volume-based    |

### Easy Memory Trick

> **S3 = Store files**

> **EBS = EC2 disk**

---

# 🎯 S3 Use Cases

S3 is commonly used for:

### 1. Backup and Restore

Companies can store backup files in S3.

```text
Application
    ↓
Backup
    ↓
S3
```

### 2. Website Images

An e-commerce website can store product images in S3.

```text
Product Image
      ↓
     S3
```

### 3. Video Storage

Applications can store videos in S3.

### 4. Data Storage

Companies can store large amounts of data in S3.

### 5. Log Storage

Application or server logs can be stored in S3.

---

# 🔐 S3 Security

S3 provides several security mechanisms to control access to data.

Important concepts include:

* IAM policies
* Bucket policies
* Block Public Access
* Encryption
* Access control

### Important

By default, AWS provides strong security controls for S3 resources, and public access should only be enabled when there is a specific requirement.

---

# 🔒 S3 Encryption

S3 supports encryption to protect stored data.

There are two basic concepts:

```text
Encryption at Rest
        ↓
Data stored in S3 is encrypted

Encryption in Transit
        ↓
Data transferred using HTTPS
```

---

# 🗄️ S3 Storage Classes

S3 provides different storage classes depending on how frequently the data is accessed.

| Storage Class                 | Main Use                                     |
| ----------------------------- | -------------------------------------------- |
| S3 Standard                   | Frequently accessed data                     |
| S3 Intelligent-Tiering        | Data with changing access patterns           |
| S3 Standard-IA                | Infrequently accessed data                   |
| S3 One Zone-IA                | Infrequent access where one AZ is acceptable |
| S3 Glacier Instant Retrieval  | Archive data that needs quick retrieval      |
| S3 Glacier Flexible Retrieval | Long-term archive                            |
| S3 Glacier Deep Archive       | Very long-term archive                       |

### Easy Memory Trick

```text
Frequently used
      ↓
S3 Standard

Sometimes used
      ↓
S3 Standard-IA

Archive
      ↓
S3 Glacier
```

---

# ♻️ S3 Versioning

**Versioning** allows multiple versions of an object to be kept in the same bucket.

### Example

Suppose I upload:

```text
resume.pdf
```

Then I update it and upload another version.

With versioning enabled:

```text
resume.pdf
   ↓
Version 1
Version 2
Version 3
```

If I accidentally delete or overwrite a file, previous versions can help recover the data.

---

# 🔄 S3 Lifecycle

S3 Lifecycle rules can automatically move or delete objects based on defined rules.

### Example

A company stores old application logs.

```text
Day 0
 ↓
S3 Standard

After some time
 ↓
S3 Standard-IA

After longer time
 ↓
S3 Glacier

After retention period
 ↓
Delete
```

This can help reduce storage costs.

---

# 🌐 S3 Static Website Hosting

S3 can host static websites containing files such as:

```text
HTML
CSS
JavaScript
Images
```

Example:

```text
index.html
style.css
script.js
image.jpg
```

These files can be stored in an S3 bucket and used to serve a static website.

---

# 🧑‍💻 Simple Real-Time Architecture

```text
                 Customer
                    ↓
              Web Application
                    ↓
             Amazon S3 Bucket
                    ↓
       ┌────────────┼────────────┐
       ↓            ↓            ↓
    Images       Videos       Documents
```

---

# 🎯 Interview Questions

## 1. What is Amazon S3?

> Amazon S3 is a highly scalable AWS object storage service used to store and retrieve files and data such as images, videos, documents and backups.

## 2. What is a bucket?

> A bucket is a container in Amazon S3 used to store objects.

## 3. What is an object?

> An object is the actual file or data stored inside an S3 bucket.

## 4. Is S3 block storage or object storage?

> S3 is an object storage service.

## 5. What is the difference between S3 and EBS?

> S3 is object storage used to store files and data, while EBS is block storage mainly used as storage for EC2 instances.

## 6. What are the use cases of S3?

> Common use cases include backups, storing images and videos, application data, log storage and static website hosting.

## 7. Why do we use S3?

> We use S3 because it provides highly scalable, durable and secure cloud storage for different types of data.

---

# 📝 CLF-C02 Important Points

Remember these points for the AWS Cloud Practitioner exam:

* S3 = Object Storage
* Bucket = Container
* Object = File/data
* S3 is highly scalable
* S3 supports different storage classes
* S3 supports versioning
* S3 supports lifecycle management
* S3 supports encryption
* S3 can be used for backups
* S3 can host static websites
* S3 and EBS are different types of storage

---

# 🧠 Quick Revision

```text
S3
│
├── Bucket → Container
│
├── Object → File
│
├── Storage Classes
│
├── Versioning
│
├── Lifecycle
│
├── Encryption
│
├── Backup
│
└── Static Website Hosting
```

### One-Line Memory Trick

> **S3 = A highly scalable cloud storage service where files are stored as objects inside buckets.**
