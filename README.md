# Zeus
AWS Auditing &amp; Hardening Tool

Zeus is a powerful tool for AWS EC2 / S3 / CloudTrail / CloudWatch / KMS best hardening practices. It checks security settings according to the profiles the user creates and changes them to recommended settings based on the CIS AWS Benchmark source at request of the user.

~~Currently, it only includes the Logging mechanism.~~

## Identity and Access Management
- Avoid the use of the "root" account
- Ensure multi-factor authentication (MFA) is enabled for all IAM users that have a console password
- Ensure credentials unused for 90 days or greater are disabled
- Ensure access keys are rotated every 90 days or less
- Ensure IAM password policy requires at least one uppercase letter

## Logging
- Ensure CloudTrail is enabled in all regions
- Ensure CloudTrail log file validation is enabled
- Ensure the S3 bucket CloudTrail logs to is not publicly accessible
- Ensure CloudTrail trails are integrated with CloudWatch Logs
- Ensure AWS Config is enabled in all regions
- Ensure S3 bucket access logging is enabled on the CloudTrail S3 bucket
- Ensure CloudTrail logs are encrypted at rest using KMS CMKs
- Ensure rotation for customer created CMKs is enabled

# Requirements

Zeus has been written in bash script using AWS-CLI and it works in Linux/UNIX and OSX.

~~Make sure that the AWS-CLI tool is installed on the system and profile is configured (aws configure).~~

### Update:

pip & aws-cli checking functions are added that based on operating system.

# Usage

git clone https://github.com/DenizParlak/Zeus.git && cd Zeus && chmod +x zeus.sh && ./zeus.sh

# Screenshots

![alt text](https://i.hizliresim.com/DdBYbm.jpg)

![alt text](https://i.hizliresim.com/r2EPn1.jpg)
