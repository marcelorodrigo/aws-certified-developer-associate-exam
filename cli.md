# Command Line Interface
- You can use `--dry-ryn` parameter to test if you have permissions for an action, without running the action
- When you got an error from an API call, you can use `aws sts decode-authorization-message` to 

## Profiles
- `aws configure --profile my-profile-name`
- Profiles and credentials are stored in `~/.aws/credentials`
- By default, commands run using the default profile
- You can specify a profile in any command appending `--profile my-profile-name`

