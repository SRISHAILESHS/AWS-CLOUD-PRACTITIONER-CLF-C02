# IAM Hands-on Labs

This document contains the hands-on activities I completed while learning AWS Identity and Access Management (IAM).

---

## Lab 1: Create an IAM User

### Objective
Create a new IAM user with console access.

### Steps Performed
1. Opened the AWS Management Console.
2. Navigated to IAM.
3. Selected **Users**.
4. Clicked **Create User**.
5. Assigned a username.
6. Enabled console access.
7. Created the user successfully.

### Result
Successfully created an IAM user.

---

## Lab 2: Create an IAM Group

### Objective
Create an IAM group to manage user permissions.

### Steps Performed
1. Opened IAM.
2. Selected **User Groups**.
3. Clicked **Create Group**.
4. Entered the group name.
5. Created the group.

### Result
Successfully created an IAM group.

---

## Lab 3: Add User to Group

### Objective
Assign a user to an IAM group.

### Steps Performed
1. Opened the IAM user.
2. Selected **Add User to Group**.
3. Chose the Developers group.
4. Saved the changes.

### Result
The user was successfully added to the group.

---

## Lab 4: Attach an IAM Policy

### Objective
Grant S3 read-only access to the IAM user.

### Steps Performed
1. Opened the IAM user.
2. Clicked **Add Permissions**.
3. Selected **AmazonS3ReadOnlyAccess**.
4. Attached the policy.

### Result
The user could access Amazon S3 in read-only mode.

---

## Lab 5: Test Permissions

### Objective
Verify IAM permissions.

### Steps Performed
1. Logged in using the IAM user.
2. Opened Amazon S3.
3. Successfully viewed S3 buckets.
4. Attempted to open Amazon EC2.

### Result
S3 access was allowed, but EC2 access was denied because the user did not have EC2 permissions.

---

## Lab 6: Enable MFA

### Objective
Enable Multi-Factor Authentication for an IAM user.

### Steps Performed
1. Opened IAM.
2. Selected the IAM user.
3. Chose **Enable MFA**.
4. Configured the authenticator application.

## Lab 7: Create a Custom IAM Policy

## Lab 8: Generate IAM Credentials Report

## Lab 9: View IAM Access Advisor

## Lab 10: Create an IAM Role for EC2

### Result
Successfully enabled MFA for the IAM user.

---

## Skills Practiced

- Creating IAM Users
- Creating IAM Groups
- Managing IAM Permissions
- Attaching IAM Policies
- Testing Access Permissions
- Configuring MFA
- Understanding Access Denied errors