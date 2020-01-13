# Identity and Access Manager
Amazon uses the AAA concept to provide Authentication, Authorization and Auditing to resources inside your AWS account.

## Authentication
- Provided by various methods
   - Password
   - Access Keys

*Note: Users only need a password set on their account if they are willing to use AWS Console.*

##  Authorization
- IAM Policy* is the root managing mechanism
- Every policy is consisted of
	- Effect: *Allow / Deny*
	- Action (what the user can do)
	- Resource (what recource the policy applies to)

# Users, Groups and Roles
