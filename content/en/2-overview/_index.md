---
title: "Lab Overview"
weight: 20
chapter: true
pre: "<b>2. </b>"
translationKey: "overview"
---

This lab guides you through using AWS KMS to encrypt data in Amazon S3 while monitoring activities through AWS CloudTrail.

## Objectives

After completing this lab, you will:

- ✅ Understand how to create and manage KMS keys
- ✅ Create a Customer Master Key
- ✅ Create an S3 bucket with CloudTrail logging
- ✅ Encrypt data in S3 using KMS keys
- ✅ Monitor key usage through CloudTrail
- ✅ Manage key access for users and roles

## AWS Services Used

### AWS KMS

A key management service that makes it easy to create and control encryption keys. KMS uses Hardware Security Modules (HSMs) to protect key security.

### Amazon S3

Object storage service designed to store and retrieve any amount of data. S3 provides 99.999999999% durability and seamless integration with KMS for data encryption.

### AWS CloudTrail

Logging service that enables monitoring and retention of account activity. CloudTrail provides event history for all KMS key-related activities.

## Requirements

### Required Knowledge

- Basic understanding of AWS Console
- Knowledge of IAM (Identity and Access Management)
- Familiarity with data encryption concepts

### Required Resources

- **AWS Account**: With full IAM access
- **Permissions**: For KMS, S3, and CloudTrail
- **AWS Region**: us-east-1 (default)
- **Time**: 30-45 minutes

## Implementation Process

1. **Create KMS Key** → Initialize Customer Master Key
2. **Configure S3** → Create bucket with KMS encryption
3. **Upload Data** → Test automatic encryption
4. **Check CloudTrail** → View activity logs
5. **Manage Permissions** → Configure IAM policies
