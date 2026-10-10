# AWS S3 Security and Bucket Policies

## 1. What Is S3 Security?

S3 security protects files stored in Amazon S3 from unauthorized access, modification, and deletion.

**Real-time example:** A boutique stores customer bills and product images in S3. Security ensures that only authorized people can access private bills.

## 2. S3 Bucket Policy

A bucket policy is a JSON-based resource policy that controls access to an S3 bucket and its objects.

**Real-time example:** Allow customers to view product images while preventing unauthorized users from uploading or deleting files.

### Important Elements

| Element | Meaning |
|---|---|
| Version | Policy language version |
| Statement | Permission rule |
| Effect | Allow or Deny |
| Principal | Who receives the permission |
| Action | What operation is permitted |
| Resource | Which bucket or objects are affected |

### Example Bucket Policy

This example allows a specific IAM role to read objects from a bucket.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "AWS": "arn:aws:iam::123456789012:role/PhotoViewer"
      },
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::boutique-photos-example/*"
    }
  ]
}
```

Note: Replace the example account ID, role name, and bucket name with your actual values.

- `Allow`: Grants the specified permission.
- `Principal`: Identifies the IAM role.
- `s3:GetObject`: Allows reading objects.
- `Resource`: Identifies objects inside the bucket.

## 3. IAM Policy

An IAM policy defines permissions for IAM users, groups, and roles.

**Real-time example:** Give an employee permission to upload invoices to S3 without allowing them to delete invoices.

## 4. Bucket Policy vs IAM Policy vs ACL

| Feature | Bucket Policy | IAM Policy | ACL |
|---|---|---|---|
| Attached to | S3 bucket | IAM identity | Bucket or object |
| Purpose | Controls bucket access | Controls identity permissions | Grants basic access |
| Example | Allow a role to read files | Allow an employee to upload files | Grant basic object access |
| Format | JSON | JSON | S3-specific permissions |

ACLs are generally disabled in modern S3 configurations when using Bucket owner enforced Object Ownership.

## 5. Block Public Access

S3 Block Public Access helps prevent buckets and objects from becoming publicly accessible.

**Real-time example:** Prevent strangers from accessing confidential customer invoices.

**Best practice:** Keep Block Public Access enabled unless public access is specifically required.

## 6. Allow and Deny

- **Allow:** Grants a specified permission.
- **Deny:** Explicitly blocks a specified permission.

**Important:** An applicable explicit Deny overrides an Allow. Permissions not granted are generally denied by default.

## 7. S3 Encryption

Encryption protects stored data from being read without the necessary decryption capability.

### Encryption at Rest

Protects data while it is stored in S3.

- **SSE-S3:** Amazon S3 manages the encryption keys.
- **SSE-KMS:** Uses AWS Key Management Service (KMS) for key management and additional access controls.

### Encryption in Transit

Protects data while it travels between applications and S3.

**Example:** HTTPS/TLS protects data during upload and download.

## 8. S3 Versioning

Versioning stores multiple versions of an object.

**Real-time example:** If an employee accidentally overwrites an inventory report, an earlier version may be recoverable.

## 9. Pre-signed URLs

Pre-signed URLs provide temporary access to a specific S3 object.

**Real-time example:** Send a customer a temporary link to download their invoice without making the entire bucket public.

## 10. IAM Access Analyzer for S3

Access Analyzer helps identify buckets that may be accessible to external users or accounts.

**Real-time example:** Detect a bucket that accidentally exposes confidential business documents.

## 11. AWS CloudTrail

CloudTrail records AWS API activity. S3 object-level activity can be recorded by configuring the appropriate data events.

**Real-time example:** Investigate which identity deleted an object and when the event occurred.

## 12. Amazon GuardDuty

GuardDuty detects suspicious activity and potential threats. Its S3 Protection feature helps identify potentially malicious S3 data-access activity.

**Real-time example:** Investigate unusual access patterns involving customer records.

## 13. S3 Object Lock

Object Lock helps prevent objects from being deleted or overwritten during a retention period or under a legal hold.

**Real-time example:** Protect financial records that must be retained for compliance.

## 14. S3 Access Points

Access Points provide separate access endpoints and policies for different applications or teams using the same bucket.

**Real-time example:** Give the finance application access to invoices and the marketing application access to product images.

## 15. VPC Endpoint Policy

A VPC endpoint policy controls which requests are permitted through a particular VPC endpoint.

**Real-time example:** Allow an application in a private network to access only approved S3 resources through its endpoint.

## 16. S3 Object Ownership

Object Ownership determines object ownership and whether ACLs are enabled.

**Real-time example:** Ensure your organization owns and manages uploaded objects rather than relying on individual uploaders' ACLs.

## 17. Important S3 Security Best Practices

1. Keep Block Public Access enabled for private buckets.
2. Follow the principle of least privilege.
3. Use bucket policies and IAM policies appropriately.
4. Enable encryption for stored data and use HTTPS/TLS for data in transit.
5. Enable versioning when recovery from accidental changes is important.
6. Use CloudTrail to audit relevant AWS activity.
7. Use Access Analyzer to identify unintended external access.
8. Never expose AWS access keys or secret keys in public repositories.
9. Use pre-signed URLs for temporary file access when appropriate.
10. Consider Object Lock for records that require protection against deletion.

## 18. Interview Revision

| Question | Short Answer |
|---|---|
| What is a bucket policy? | A JSON policy that controls access to an S3 bucket and its objects. |
| What is an IAM policy? | A policy that defines permissions for an IAM identity. |
| What is Block Public Access? | A feature that helps prevent public exposure of S3 data. |
| What is SSE-S3? | Server-side encryption with keys managed by Amazon S3. |
| What is SSE-KMS? | Server-side encryption using AWS KMS for key management. |
| What is versioning? | A feature that maintains multiple object versions. |
| What is a pre-signed URL? | A URL that grants temporary access to a specified object. |
| What is CloudTrail? | A service that records AWS API activity. |
| What is GuardDuty? | A service that detects suspicious activity and potential threats. |
| What is Object Lock? | A feature that helps prevent object deletion or overwriting during retention. |

## Conclusion

Amazon S3 security uses policies, access controls, encryption, versioning, and monitoring to protect stored data.

For the AWS Cloud Practitioner exam, focus first on Bucket Policies, IAM Policies, Block Public Access, Encryption, Versioning, and CloudTrail.