# central-cloudtrail-logging

CloudFormation templates that setup CloudTrail logging to a central AWS account.

Copies are also kept in the individual accounts for troubleshooting and automation purposes. While the central logs are kept forever, the local copies are kept for 90 days in S3 and 7 days in CloudWatch Logs. The solution consists of two templates, each of which needs to be updated before deployment to whitelist your AWS accounts. See the comments at the top of each template for instructions. Note also that a bucket is create to store access logs to see who accesses the CloudTrail logs.

* **security-account.yaml**: deploy this first into the security/audit/logs account that will house the CloudTrail logs from other AWS accounts as well as itself.
* **every-account.yaml**: deploy this next into each account, including the security account.