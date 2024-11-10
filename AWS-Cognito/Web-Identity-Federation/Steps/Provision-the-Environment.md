# 1. Login to an AWS Account

- Login to an AWS account using a user with admin privileges and ensure your region is set to `us-east-1` `N. Virginia`.
- Click [HERE](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=https://learn-cantrill-labs.s3.amazonaws.com/aws-cognito-web-identity-federation/WEBIDF.yaml&stackName=WEBIDF) to auto configure the infrastructure the app requires

![image](https://github.com/user-attachments/assets/fc7f8170-332a-4345-bb4a-0b627befc134)
  
- Check the  `The following resource(s) require capabilities: [AWS::IAM::ManagedPolicy, AWS::IAM::Role]` box  
- Click `Create Stack`

<img width="1543" alt="image" src="https://github.com/user-attachments/assets/f3986f41-bed9-4b9e-a6a6-c166b15cccb8">

  
- Wait for the STACK to move into the `CREATE_COMPLETE` state.


![image](https://github.com/user-attachments/assets/b91a0611-84f7-453c-a92d-c3da27921641)


