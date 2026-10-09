# Amazon S3 – Hands-On Lab

## 🎯 Objective

In this hands-on lab, I created an Amazon S3 bucket and performed basic operations such as:

* Creating an S3 bucket
* Uploading an object
* Viewing an object
* Downloading an object
* Deleting an object
* Deleting the bucket

---

# 1. Open Amazon S3

1. Log in to the AWS Management Console.
2. Search for **S3**.
3. Open **Amazon S3**.

---

# 2. Create an S3 Bucket

1. Click **Create bucket**.
2. Enter a unique bucket name.

Example:

```text
shylu-s3-demo-bucket
```

### Important

S3 bucket names must be **globally unique**.

3. Select the required AWS Region.
4. Keep the default settings unless there is a specific requirement.
5. Review the settings.
6. Click **Create bucket**.

---

# 3. Open the Bucket

After creating the bucket:

1. Open the newly created bucket.
2. The bucket will initially be empty.

Example:

```text
Bucket
└── No objects
```

---

# 4. Upload an Object

1. Click **Upload**.
2. Click **Add files**.
3. Select a file from your computer.

Example:

```text
sample.jpg
```

4. Click **Upload**.

The file is now stored as an object inside the S3 bucket.

```text
S3 Bucket
└── sample.jpg
```

---

# 5. View the Object

After uploading:

1. Open the uploaded object.
2. Check the object's details.

You can see information such as:

* Object name
* Object size
* Last modified date
* Storage class
* Object URL

---

# 6. Create a Folder

S3 is object storage, but the console allows us to organize objects using prefixes that appear like folders.

1. Go back to the bucket.
2. Click **Create folder**.
3. Enter:

```text
images
```

4. Click **Create folder**.

The bucket now appears like:

```text
S3 Bucket
│
├── images/
│
└── sample.jpg
```

---

# 7. Upload an Object into the Folder

1. Open the `images` folder.
2. Click **Upload**.
3. Select another image.
4. Click **Upload**.

Example:

```text
S3 Bucket
│
├── images/
│   └── dress.jpg
│
└── sample.jpg
```

---

# 8. Download an Object

1. Select an object.
2. Click **Download**.

The file will be downloaded to your computer.

Example:

```text
S3
 ↓
sample.jpg
 ↓
Local Computer
```

---

# 9. Delete an Object

1. Select the object.
2. Click **Delete**.
3. Confirm the deletion.

Example:

```text
Before:

S3 Bucket
├── sample.jpg
└── images/
    └── dress.jpg


After deleting sample.jpg:

S3 Bucket
└── images/
    └── dress.jpg
```

---

# 10. Enable Versioning

Versioning allows S3 to keep multiple versions of an object.

### Steps

1. Open the S3 bucket.
2. Go to the **Properties** tab.
3. Find **Bucket Versioning**.
4. Click **Edit**.
5. Enable versioning.
6. Save the changes.

### Example

```text
document.pdf
     │
     ├── Version 1
     ├── Version 2
     └── Version 3
```

Versioning can help recover objects after accidental overwrites or deletions.

---

# 11. Check Storage Class

When uploading an object, S3 assigns a storage class.

The default storage class is:

```text
S3 Standard
```

S3 also provides other storage classes for different access and cost requirements.

Examples:

```text
S3 Standard
S3 Intelligent-Tiering
S3 Standard-IA
S3 One Zone-IA
S3 Glacier
```

---

# 12. Delete the Bucket

Before deleting the bucket:

1. Remove all objects from the bucket.
2. Open the bucket.
3. Select **Delete**.
4. Confirm the bucket name.
5. Delete the bucket.

### Important

A bucket generally needs to be empty before it can be deleted.

---

# 📸 Screenshots to Add to GitHub

Create a `Screenshots` folder and capture the important steps.

```text
Screenshots/
│
├── 01-S3-Create-Bucket.png
├── 02-S3-Bucket-Created.png
├── 03-S3-Upload-Object.png
├── 04-S3-Object-Uploaded.png
├── 05-S3-Object-Details.png
├── 06-S3-Create-Folder.png
├── 07-S3-Versioning.png
└── 08-S3-Bucket-Deleted.png
```

---

# 🧠 What I Learned

Through this hands-on lab, I learned:

* How to create an S3 bucket
* How to upload objects
* How to download objects
* How to organize objects using prefixes/folders
* How to enable versioning
* How to view object details
* How to delete objects
* How to delete an S3 bucket

---

# 🎯 Interview Summary

> **I created an Amazon S3 bucket, uploaded and managed objects, explored bucket properties and versioning, and practiced basic S3 operations through the AWS Management Console.**
