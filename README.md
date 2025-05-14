# AWS CloudFormation Template: S3 Bucket

This repository contains a simple AWS CloudFormation template (`s3.yaml`) to provision an Amazon S3 bucket.

## Template Overview

**Filename:** `s3.yaml`  
**Format Version:** 2010-09-09  
**Description:**  
This CloudFormation template creates a single Amazon S3 bucket. It can be used to provision an S3 bucket as part of a larger infrastructure or for standalone use cases such as data storage, hosting static websites, or backups.

## Resources

### `MyS3Bucket`
- **Type:** `AWS::S3::Bucket`
- **Description:** Creates a new S3 bucket with default settings.

## Usage

### Create the CloudFormation stack

aws cloudformation create-stack \
  --stack-name my-s3-bucket-stack \
  --template-body file://s3.yaml \
  --capabilities CAPABILITY_NAMED_IAM

### Check stack status
aws cloudformation describe-stacks --stack-name my-s3-bucket-stack

### Cleanup
aws cloudformation delete-stack --stack-name my-s3-bucket-stack
### Note: 
Ensure the bucket is empty before deletion or enable automatic deletion policies in the template.
