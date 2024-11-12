# CREATE A COGNITO IDENTITY POOL  

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
- Review the content and click `Create identity pool`

<img width="1551" alt="image" src="https://github.com/user-attachments/assets/d5032368-87d2-4f06-be9b-f4be32422d33">

