# Identity and Access Manager
Amazon uses the AAA concept to provide Authentication, Authorization and Auditing to resources inside your AWS account.

- Root account should not be used to operate AWS, as it not follows the least previlege principle
- Policies (JSON) can be applied to groups or users
- Groups contains users only
- Supported MFA mechanisms
  - Virtual MFA (Google Authenticator, Authy, etc)
  - Universal 2FA Security Key (like Yubikey defices)
  - Hardware Key Fob MFA Device (like Gemalto devices)
  - Hardware Key Fob MFA Device for AWS GovCloud (US) (like SurePassID devices)

## IAM Roles
- Intended when a service needs to perform operations on your behalf
- Roles for EC2 Instances or AWS Services

## IAM Security Tools
- IAM Credential Reports (account-level): is a report that list all users and status on your account.
- IAM Access Advisor (user-level): show services permissions granted to a user, and when was the last access.
- IAM Policy Simulator: you can test and troubleshoot IAM policies
