# Command Line Interface
- You can use `--dry-ryn` parameter to test if you have permissions for an action, without running the action
- When you got an error from an API call, you can use `aws sts decode-authorization-message` to 

## Profiles
- `aws configure --profile my-profile-name`
- Profiles and credentials are stored in `~/.aws/credentials`
- By default, commands run using the default profile
- You can specify a profile in any command appending `--profile my-profile-name`

## MFA with CLI
You must create a temporary session:
- `aws sts get-session-token --serial-number arn-of-mfa-device --token-code token --duration--seconds 7200`
- You're going to receive temporary credentials as response

## Credentials Order
Credentials are loaded by the following order:
1. Command Line Options `--region`, `--output` and `--profile`
2. Environment variables `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY` and `AWS_SESSION_TOKEN`
3. CLI credentials file (`~/.aws/credentials`)
4. CLI configuration file (`~/.aws/config`)
5. Container Credentials (ECS Tasks)
6. Instance Profile Credentials (EC2 Instance Profiles)
