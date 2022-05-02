## Summary

Launch the provided AWS CloudFormation template using the AWS Console and provide the following information:

  | Parameter            | Description
  | -------------------- | --------------------------------------------------------------------------------------------------
  | ManagementAccountId  | Numeric account ID for the management account for the security audit.

### Deployment Guide (Console)
1. <a href="https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=iam-role-security-audit&templateURL=https://s3.us-west-2.amazonaws.com/inf-security-automation/security-audit-roles.yml" target="_blank">![Launch](./img/launch-stack.png?raw=true "Launch")</a>
1. Click **Next** to proceed with the next step of the wizard.
1. Specify parameters for the stack.
1. Click **Next** to proceed with the next step of the wizard.
1. Click **Next** to skip the **Options** step of the wizard.
1. Check the **I acknowledge that this template might cause AWS CloudFormation to create IAM resources.** checkbox.
1. Click **Create** to start the creation of the stack.
1. Wait until the stack reaches the state **CREATE_COMPLETE**

### Deployment Guide (CLI)
```
aws cloudformation create-stack --stack-name "iam-role-security-audit-roles" \
                                --template-body file://security-audit-roles.yml \
                                --region us-west-2

### Clean-up Guide (CLI)
```
aws cloudformation delete-stack --stack-name "iam-role-security-audit-roles" \
                                --region us-west-2
```

