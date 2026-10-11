# Amazon S3 Replication

## 1. What is S3 Replication?

Amazon S3 Replication automatically copies objects from one S3 bucket to another S3 bucket based on the replication rules we configure.

**Example:** When we upload an image to the source bucket (`mainbucket`), S3 automatically copies the image to the destination bucket.

## 2. Requirements

- Create an origin/source bucket named `mainbucket`.
- Create another S3 bucket to receive the replicated objects.
- Enable **Bucket Versioning on both buckets**.
- Configure the replication rule in the source bucket.
- Provide the required IAM permissions for replication.

**Important:** Versioning must be enabled on both the source and destination buckets. Without versioning enabled on both buckets, S3 replication cannot be configured successfully.

## 3. Hands-On Lab: Configure S3 Replication

### Step 1: Create the Origin Bucket

1. Open the AWS Management Console.
2. Search for **Amazon S3**.
3. Click **Create bucket**.
4. Enter the bucket name: `mainbucket` (use a globally unique name if this name is unavailable).
5. Select your required AWS Region.
6. Under Bucket Versioning, select **Enable**.
7. Create the bucket.

### Step 2: Create the Destination Bucket

1. Click **Create bucket** again.
2. Enter a different, globally unique bucket name.
3. Select the destination AWS Region.
4. Enable **Bucket Versioning**.
5. Create the bucket.

**Note:** For CRR, choose a different Region for the destination. For SRR, use the same Region.

### Step 3: Upload an Object

1. Open the `mainbucket` source bucket.
2. Click **Upload**.
3. Add an image or file.
4. Click **Upload** to finish.

### Step 4: Create a Replication Rule

1. Open the source bucket, `mainbucket`.
2. Go to the **Management** tab.
3. Find **Replication rules**.
4. Click **Create replication rule**.
5. Enter a replication rule name.
6. Choose whether the rule applies to all objects or a specific prefix.
7. Select the destination bucket.
8. Configure the required IAM role and permissions.
9. Enable the rule and save the changes.

Refer to the screenshot named **`replication rule`** for the console configuration.

### Step 5: Verify Replication

1. Open the source bucket and upload a new image after the rule is enabled.
2. Open the destination bucket.
3. Check whether the uploaded image appears there.
4. Verify the object's details and version information if needed.

**Expected result:** The new object is automatically replicated to the destination bucket when it matches the replication rule.

Note: Objects uploaded before the rule was enabled are not automatically replicated by default. Use S3 Batch Replication if you need to replicate existing objects.

## 4. Types of S3 Replication

| Type | Full Form | Example |
|---|---|---|
| CRR | Cross-Region Replication | Mumbai → Singapore |
| SRR | Same-Region Replication | Mumbai → Mumbai |

- **CRR:** Used for disaster recovery and maintaining copies in different geographical Regions.
- **SRR:** Used for maintaining separate copies in the same Region, such as for compliance or account separation.

## 5. Important Points to Remember

- Versioning must be enabled on both source and destination buckets.
- The destination bucket must be different from the source bucket.
- Replication requires appropriate IAM permissions.
- Replication applies to eligible objects according to the configured rules.
- Replication can incur storage and data-transfer charges.
- By default, deleting an object in the source bucket does not mean its permanent deletion is automatically replicated to the destination.
- Replication is asynchronous, so objects may take some time to appear in the destination bucket.

## Conclusion

Amazon S3 Replication helps maintain copies of objects in another bucket automatically. We configure replication rules under the source bucket's **Management → Replication rules** section. Enabling versioning on both buckets is a key prerequisite.