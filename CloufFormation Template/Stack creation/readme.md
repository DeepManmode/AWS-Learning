# AWS CloudFormation – EC2 Instance Deployment

## Overview

This demonstrates how to use **AWS CloudFormation (CFT)** to create and manage an **EC2 instance** using a YAML template.

The CloudFormation template defines the AWS resources and their configuration. Instead of creating the EC2 instance manually, the resources are created automatically when the CloudFormation stack is launched.

## Practiced

* Created an EC2 instance using an AWS CloudFormation YAML template.
* Created a CloudFormation stack using an existing template.
* Uploaded the YAML template file while creating the stack.
* Monitored **Stack Events** to verify whether the resources were created successfully.
* Used **CloudFormation Drift Detection** to check whether the actual AWS resources had changed from the configuration defined in the template.


## CloudFormation Workflow

The workflow followed in this practice was:

1. Created an EC2 CloudFormation template using YAML.
2. Opened **AWS CloudFormation** in the AWS Management Console.
3. Selected **Create Stack**.
4. Selected **Choose an existing template**.
5. Selected **Upload a template file**.
6. Uploaded the CloudFormation YAML template.
7. Created the CloudFormation stack.
8. Checked the **Stack Events** to verify successful resource creation.
9. Opened the **Stack Actions** menu.
10. Selected **Detect drift** to check whether the stack resources matched the CloudFormation template.

## Structure

```text
AWS-CloudFormation-EC2/
│
├── template.yaml
└── README.md
```

## CloudFormation Template

The `template.yaml` file contains the CloudFormation configuration used to create the EC2 instance.


## Stack Events

After creating the stack, I checked the **Events** section in CloudFormation.

Stack Events help verify the status of resources during stack creation and show whether the resources were created successfully or if any errors occurred.

For example:

```text
CREATE_IN_PROGRESS
CREATE_COMPLETE
```

`CREATE_COMPLETE` indicates that the resource or stack was created successfully.

## Drift Detection

CloudFormation **Drift Detection** is used to determine whether the actual configuration of resources has changed from the configuration defined in the CloudFormation template.

For example, if an EC2 instance is created using the CloudFormation template and its configuration is later modified manually, CloudFormation can detect that difference as drift.

Common drift statuses include:

* **IN_SYNC** – The actual resource configuration matches the CloudFormation template.
* **DRIFTED** – The actual resource configuration differs from the CloudFormation template.
* **NOT_CHECKED** – Drift detection has not been performed.

## What I Learned

* How to create AWS resources using CloudFormation.
* How to upload and deploy a YAML CloudFormation template.
* How CloudFormation stacks manage AWS resources.
* How to use Stack Events for troubleshooting and monitoring.
* How CloudFormation Drift Detection identifies configuration changes.
* The importance of Infrastructure as Code (IaC) for managing AWS infrastructure.

## Reference

AWS CloudFormation Resource and Property Types:

[AWS CloudFormation Template Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/TemplateReference/aws-template-resource-type-ref.html?utm_source=chatgpt.com)
