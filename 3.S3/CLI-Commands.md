# Amazon S3 – AWS CLI Commands

This file contains commonly used AWS CLI commands for Amazon S3.

---

## 1. Check AWS CLI Configuration

```bash
aws configure
```

Used to configure:

* AWS Access Key ID
* AWS Secret Access Key
* AWS Region
* Output format

---

## 2. Check AWS Identity

```bash
aws sts get-caller-identity
```

Shows information about the currently configured AWS account/user.

---

# Bucket Commands

## 3. List All S3 Buckets

```bash
aws s3 ls
```

Lists all S3 buckets available in the AWS account.

---

## 4. Create an S3 Bucket

For example:

```bash
aws s3 mb s3://my-shylu-demo-bucket
```

Creates a new S3 bucket.

### Note

S3 bucket names must be globally unique.

---

## 5. List Contents of a Bucket

```bash
aws s3 ls s3://my-shylu-demo-bucket
```

Lists objects stored inside the bucket.

---

# Upload Commands

## 6. Upload a File

```bash
aws s3 cp image.jpg s3://my-shylu-demo-bucket/
```

Uploads `image.jpg` to the S3 bucket.

---

## 7. Upload a File to a Folder

```bash
aws s3 cp image.jpg s3://my-shylu-demo-bucket/images/
```

Uploads the file into the `images` prefix.

---

## 8. Upload Multiple Files

```bash
aws s3 cp ./files s3://my-shylu-demo-bucket/files/ --recursive
```

Uploads all files from the local `files` directory.

---

# Download Commands

## 9. Download a File

```bash
aws s3 cp s3://my-shylu-demo-bucket/image.jpg .
```

Downloads `image.jpg` from S3 to the current directory.

---

## 10. Download Multiple Files

```bash
aws s3 cp s3://my-shylu-demo-bucket/files/ ./files/ --recursive
```

Downloads multiple objects from S3.

---

# Copy Commands

## 11. Copy an Object Inside S3

```bash
aws s3 cp s3://my-shylu-demo-bucket/image.jpg s3://my-shylu-demo-bucket/backup/image.jpg
```

Copies an object from one S3 location to another.

---

# Sync Commands

## 12. Synchronize Local Folder with S3

```bash
aws s3 sync ./website s3://my-shylu-demo-bucket/website/
```

Synchronizes files from a local folder to an S3 bucket.

---

## 13. Synchronize S3 with Local Folder

```bash
aws s3 sync s3://my-shylu-demo-bucket/website/ ./website/
```

Downloads and synchronizes S3 objects with a local folder.

---

# Delete Commands

## 14. Delete an Object

```bash
aws s3 rm s3://my-shylu-demo-bucket/image.jpg
```

Deletes an object from the bucket.

---

## 15. Delete Multiple Objects

```bash
aws s3 rm s3://my-shylu-demo-bucket/images/ --recursive
```

Deletes multiple objects under the specified prefix.

---

## 16. Delete an Empty Bucket

```bash
aws s3 rb s3://my-shylu-demo-bucket
```

Deletes an empty S3 bucket.

---

## 17. Force Delete a Bucket

```bash
aws s3 rb s3://my-shylu-demo-bucket --force
```

Deletes the bucket and its objects.

### ⚠️ Warning

Use this command carefully because it can permanently remove data.

---

# S3 API Commands

## 18. List Buckets Using s3api

```bash
aws s3api list-buckets
```

Returns detailed information about S3 buckets.

---

## 19. Get Bucket Location

```bash
aws s3api get-bucket-location --bucket my-shylu-demo-bucket
```

Shows the Region associated with the bucket.

---

## 20. List Objects Using s3api

```bash
aws s3api list-objects-v2 --bucket my-shylu-demo-bucket
```

Lists objects inside the bucket.

---

# Quick Revision

| Command                         | Purpose                      |
| ------------------------------- | ---------------------------- |
| `aws s3 ls`                     | List buckets                 |
| `aws s3 mb`                     | Create bucket                |
| `aws s3 cp`                     | Copy/upload/download objects |
| `aws s3 sync`                   | Synchronize folders          |
| `aws s3 rm`                     | Delete objects               |
| `aws s3 rb`                     | Delete bucket                |
| `aws s3api list-buckets`        | List buckets using API       |
| `aws s3api get-bucket-location` | Get bucket Region            |
| `aws s3api list-objects-v2`     | List bucket objects          |
| `aws sts get-caller-identity`   | Check AWS identity           |

---

# Important Interview Commands

The most important commands to remember for beginners are:

```bash
aws s3 ls
aws s3 mb s3://bucket-name
aws s3 cp file.txt s3://bucket-name/
aws s3 cp s3://bucket-name/file.txt .
aws s3 sync ./folder s3://bucket-name/folder/
aws s3 rm s3://bucket-name/file.txt
aws s3 rb s3://bucket-name
```
