# **AWS IAM (AWS Identity & Access Management)**

IAM is a service that helps you securely control access to AWS resources.

It allows you to manage users, roles, and permissions to define who can access what within your AWS environment.

* Free Service: IAM is offered at no additional cost.
* Global Service.
* Root account created by default; shouldn't be used or shared.

---

# **AWS IAM Create User**

* **Create Users:** You can create individual user accounts for people who need access to your AWS resources.

* **Assign Permissions:** You can assign specific permissions to users, groups, or roles to control what actions they can perform on AWS services.

* **Create Groups:** You can group users together and assign permissions to the group, making management easier for multiple users.

* **Create Roles:** You can create roles to assign temporary permissions to AWS services or users, especially useful for securely managing permissions across different AWS resources.

* **Define Policies:** You can create and attach custom policies to define fine-grained permissions for controlling access to AWS resources.

* **Manage Federated Access:** IAM allows integrating with external identity providers (like Active Directory) for centralized management of user access across AWS.

---

# **AWS IAM Ways of Accessing AWS**

* **AWS Management Console:** Provides a graphical, web-based approach.

* **AWS CLI:** Provides a command-line, scripting approach.

* **AWS SDKs and APIs:** Offer programmatic, code-based access, allowing users to integrate AWS directly into their applications.

---

# **AWS IAM Best Practices**

* Avoid using the root account except for account setup.
* Add users to a group and assign permissions to the group.
* Use a password policy or MFA.
* Use **Access Keys** for CLI/SDK.
* Never share **Access Keys** or passwords.
* Audit permissions using the IAM Credential Report.
