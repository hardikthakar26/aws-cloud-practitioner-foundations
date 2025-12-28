# AWS S3 Static Website – CLI Commands

This file contains AWS CLI commands used for S3 static website hosting.

## Step 1: Configure AWS CLI
aws configure

**Purpose**
Configure AWS credentials locally for CLI access

## Step 2: Create S3 Bucket
aws s3 mb s3://my-static-site-demo-bucket

## Step 2: Create S3 Bucket
aws s3 mb s3://my-static-site-demo-bucket

**Purpose**
Create an S3 bucket to host static website files

*Note:*
Bucket name must be globally unique

## Step 3: Upload Website Files
aws s3 cp index.html s3://my-static-site-demo-bucket/


**Purpose**
Upload website content to S3 bucket

## Step 4: Enable Static Website Hosting
aws s3 website s3://my-static-site-demo-bucket \
  --index-document index.html


**Purpose**
Enable static website hosting on S3

## Step 5: Verify Bucket Content
aws s3 ls s3://my-static-site-demo-bucket


**Purpose**
Verify uploaded files

## Step 6: Cleanup (Cost Awareness)
aws s3 rb s3://my-static-site-demo-bucket --force

**Purpose**
Delete resources to avoid unwanted charges

## Key Learnings
1.Used AWS CLI instead of only AWS Console

2.Understood serverless static website hosting

3.Learned importance of cleanup and cost control