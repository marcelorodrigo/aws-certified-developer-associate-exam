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

## Users, Groups and Roles
- When a user is created, he has no permissions by default (also known as *Default Deny*)
- AWS recommends attaching policies to groups and then assigning users to them.
- Roles are entities with attaches policies. Resources can assume a role to obtain permissions from a policy
- It's possible to assign a role for on AWS account to access resources in your account

## Policy Evaluation Logic
- Policies are denied by default (also in case if it is not informed on policy)
- If there is two policies, one allowing and another one denying to same condition: a deny will be granted
