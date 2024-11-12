# 1. CREATE A COGNITO IDENTITY POOL  

- Go to the Cognito Console https://console.aws.amazon.com/cognito/home?region=us-east-1#
- Select `Grant access to AWS Services` from the dropdown and click on `Create identity pool`        

<img width="1680" alt="image" src="https://github.com/user-attachments/assets/ef633135-5954-4fd0-b6a5-32a0284efd44">


- In `Configure identity pool trust` page, Select `Authenticated Access` for User access
- Select `Google` for Authenticated identity sources

<img width="1680" alt="image" src="https://github.com/user-attachments/assets/07c6f0d1-3537-431e-b324-0956674c7656">

## Configure Permissions  

Under Authenticated role 
- Select `create a new IAM role`  
- Enter name `WebIDFpool` for IAM role name and click `Next`

<img width="1676" alt="image" src="https://github.com/user-attachments/assets/86db45ab-f782-4a9a-be1a-6f6d5a06e8e9">


## Connect Identity providers

- Enter `client ID` under Set up Google federation.(Client ID is the ID generated from previous step)  

<img width="1549" alt="image" src="https://github.com/user-attachments/assets/d949df3a-5b65-4ac7-a425-fbad88dfd7e5">


## Configure properties

- Enter `WebIDFpool` as Identity pool name and click `Next`
- Review the content and click `Create identity pool`. Make note of the `Identity pool ID`

<img width="1551" alt="image" src="https://github.com/user-attachments/assets/d5032368-87d2-4f06-be9b-f4be32422d33">


# 2. Adjust Permissions 

The serverless application is going to read images out of a private bucket created by the initial cloudformation template. The bucket is called `patchesprivatebucket`.

- Go to the IAM Console https://console.aws.amazon.com/iam/home?region=us-east-1#/home    
- Click `Roles`   
- Locate and click on `WebIDF-role`  
- Click on `Trust Relationships`  

![image](https://github.com/user-attachments/assets/acea221e-1784-49e4-8618-cf21139bfe5a)

See how this is assumable by `cognito-identity.amazonaws.com`  
With two conditions  

- `StringEquals` `cognito-identity.amazonaws.com:aud` `your congnito ID pool`  
- `ForAnyValue:StringLike` `cognito-identity.amazonaws.com:amr` `authenticated`
  
This means to assume this role - you have to be authenticated by one of the ID providers defined in the cognito ID pool.  
When you use WEDIDF with cognito, this role is assumed on your behalf by cognito, and its what generates temporary AWS credentials which are used to access AWS resources.
