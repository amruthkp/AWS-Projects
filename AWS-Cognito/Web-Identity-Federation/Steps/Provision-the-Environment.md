# 1. Login to an AWS Account

- Login to an AWS account using a user with admin privileges and ensure your region is set to `us-east-1` `N. Virginia`.
- Click [HERE](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=https://learn-cantrill-labs.s3.amazonaws.com/aws-cognito-web-identity-federation/WEBIDF.yaml&stackName=WEBIDF) to auto configure the infrastructure the app requires 
- Check the  `The following resource(s) require capabilities: [AWS::IAM::ManagedPolicy, AWS::IAM::Role]` box  
- Click `Create Stack`
- Wait for the STACK to move into the `CREATE_COMPLETE` state.
