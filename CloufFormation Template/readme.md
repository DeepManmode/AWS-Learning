# AWS CloudFormation

**AWS CloudFormation** is an Infrastructure as Code (IaC) service
provided by AWS that allows you to create, manage, and provision AWS
resources using a template instead of creating each resource manually
through the AWS Console. You define your infrastructure in a **YAML or
JSON template**, and CloudFormation automatically creates and configures
the required resources. It helps make infrastructure **consistent,
repeatable, scalable, and easier to manage**.

------------------------------------------------------------------------

## **1. IaC (Infrastructure as Code)**

**Infrastructure as Code (IaC)** means managing and provisioning
infrastructure using code or configuration files instead of manually
creating resources. With CloudFormation, you can define resources such
as **EC2, VPC, S3, IAM, RDS, Load Balancer, and Auto Scaling** in a
template. The same template can then be reused to create identical
environments such as **development, testing, and production**.

**Example:** Instead of manually creating a VPC, subnets, route tables,
and EC2 instances, you can define all of them in a CloudFormation
template and deploy them together.

------------------------------------------------------------------------

## **2. CloudFormation Stack**

A **Stack** is a collection of AWS resources that are created and
managed together by CloudFormation. When you upload or provide a
template to CloudFormation, it uses that template to create a stack and
provisions all the resources defined in it. You can update or delete the
stack, and CloudFormation manages the associated resources according to
the template.

**Example:** One stack can contain a **VPC + Subnets + Internet
Gateway + Route Tables + EC2 + Security Groups**.

**Key point:**

> **Template → CloudFormation → Stack → AWS Resources**

------------------------------------------------------------------------

## **3. CloudFormation Templates**

A **CloudFormation Template** is a YAML or JSON file that describes the
AWS infrastructure you want to create. It contains the configuration and
relationships between resources. Templates can define resources such as
EC2 instances, VPCs, S3 buckets, IAM roles, databases, and load
balancers.

A template commonly contains sections such as:

-   **Parameters** -- Inputs provided when creating the stack.
-   **Resources** -- AWS resources that CloudFormation should create.
-   **Mappings** -- Static values that can be referenced in the
    template.
-   **Conditions** -- Control whether certain resources or
    configurations are created.
-   **Outputs** -- Values returned after stack creation, such as
    resource IDs or DNS names.

**Example:**

``` yaml
Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
```

This tells CloudFormation to create an **S3 bucket**.

------------------------------------------------------------------------

## **4. Drift Detection**

**Drift Detection** is a CloudFormation feature used to determine
whether the actual AWS resources in a stack have been manually changed
from the configuration defined in the CloudFormation template. If
someone modifies a resource directly through the AWS Console, CLI, or
another method, CloudFormation can detect the difference between the
**expected configuration** and the **actual configuration**.

**Example:** Suppose your CloudFormation template defines an EC2
Security Group allowing port **80**. If someone manually adds port
**22** to the Security Group, the resource has **drifted** from the
template. Drift Detection can identify this change.

**Key point:**

> **Template configuration ≠ Actual AWS resource configuration → Drift
> detected**

## **AWS CloudFormation Resource Reference**

For a complete list of AWS CloudFormation resource types and their properties, refer to the official AWS documentation:

👉 [AWS CloudFormation Resource Types Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/TemplateReference/aws-template-resource-type-ref.html)