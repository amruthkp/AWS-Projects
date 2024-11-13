# 1. Login to an AWS Account

- Login to an AWS account using a user with admin privileges and ensure your region is set to `us-east-1` `N. Virginia`.
- Click [HERE](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=https://learn-cantrill-labs.s3.amazonaws.com/aws-cognito-web-identity-federation/WEBIDF.yaml&stackName=WEBIDF) to auto configure the infrastructure the app requires

![image](https://github.com/user-attachments/assets/fc7f8170-332a-4345-bb4a-0b627befc134)
  
- Check the  `The following resource(s) require capabilities: [AWS::IAM::ManagedPolicy, AWS::IAM::Role]` box  
- Click `Create Stack`

<img width="1543" alt="image" src="https://github.com/user-attachments/assets/f3986f41-bed9-4b9e-a6a6-c166b15cccb8">
  
- Wait for the STACK to move into the `CREATE_COMPLETE` state.

![image](https://github.com/user-attachments/assets/b91a0611-84f7-453c-a92d-c3da27921641)


# 2. Verify S3 bucket

- Go to S3 console https://s3.console.aws.amazon.com/s3/home?region=us-east-1    
- Open the bucket starting `webidf-appbucket`   
- Check that `index.html` and `scripts.js` are present  
- Click the `Permissions` Tab  
- Verify `Block all public access` is set to `Off`  
- Click `Bucket Policy` and verify there is a bucket policy.

<img width="1548" alt="image" src="https://github.com/user-attachments/assets/1729611f-dc28-4cda-8f37-1f1978a61e05">

# 3. Verify privatebucket

- Open the bucket starting `webidf-patchesprivatebucket-`  
- Load the objects in the bucket to check the contents  
- Verify there is no bucket policy and the bucket is entirely private.

<img width="1546" alt="image" src="https://github.com/user-attachments/assets/c7bec324-5f9b-4e5a-85e2-4b97cd58307b">

# 4. Verify CloudFormation Distribution  

- Move to the `CloudFront` console https://us-east-1.console.aws.amazon.com/cloudfront/v3/home?region=us-east-1#/distributions  
- Locate the distribution pointing at origin `webidf-appbucket-....`  and click  
- Locate the `distribution domain name` and note down as the `WebApp URL` prefixed with https `d2nmndy3vlq8c7.cloudfront.net`   

<img width="1548" alt="image" src="https://github.com/user-attachments/assets/b9db6e50-8ef7-4d04-a20e-ebe1f6dbfc51">



Below infrastructure is ready now.

- front end app bucket
- private bucket  
- CloudFront distribution with caching and HTTPS capability
