# AWS CloudFormation CLI Commands

These commands use the AWS CLI. Configure credentials and a default Region first, and ensure your IAM identity has the required permissions.

## 1. Validate a template

```bash
aws cloudformation validate-template --template-body file://s3-bucket.yaml
```

Checks the template's format and returns template information.

## 2. Create a stack

```bash
aws cloudformation create-stack --stack-name MyFirstS3Stack --template-body file://s3-bucket.yaml
```

Starts creating the stack from the local template.

## 3. Check stack status

```bash
aws cloudformation describe-stacks --stack-name MyFirstS3Stack
```

Displays information about the stack.

## 4. List stack resources

```bash
aws cloudformation list-stack-resources --stack-name MyFirstS3Stack
```

Lists resources associated with the stack.

## 5. Delete a stack

```bash
aws cloudformation delete-stack --stack-name MyFirstS3Stack
```

Starts deleting the stack and resources that CloudFormation is allowed to delete. Review the stack contents before running this command.

## Notes
- Run commands from the folder containing `s3-bucket.yaml`, or provide its full path.
- Stack operations take time; check status before continuing.
- S3 bucket names must be valid and unique.
