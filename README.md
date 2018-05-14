# central-cloudtrail-logging

CloudFormation templates that setup CloudTrail logging to a central AWS account.

This solution consists of two templates, each of which needs to be updated before deployment to whitelist your AWS accounts. See the comments at the top of each template for instructions.

* **security-account.yaml**: deploy this first into the security/audit/logs account that will house the CloudTrail logs from other AWS accounts as well as itself.
* **every-account.yaml**: deploy this next into each account, including the security account.