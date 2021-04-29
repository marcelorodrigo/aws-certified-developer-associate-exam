# Identity and Access Manager
Amazon uses the AAA concept to provide Authentication, Authorization and Auditing to resources inside your AWS account.

- Root account should not be used to operate AWS, as it not follows the least previlege principle
- Policies (JSON) can be applied to groups or users
- Roles for EC2 Instances or AWS Services
- IAM Credential Reports and IAM Access Advisor can help you audit IAM usage
- IAM Policy Simulator: you can test and troubleshoot IAM policies
- Supported MFA mechanisms
  - Virtual MFA (Google Authenticator, Authy, etc)
  - Universal 2FA Security Key (like Yubikey defices)
  - Hardware Key Fob MFA Device (like Gemalto devices)
  - Hardware Key Fob MFA Device for AWS GovCloud (US) (like SurePassID devices)
