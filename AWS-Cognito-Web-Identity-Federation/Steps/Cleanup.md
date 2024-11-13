# 1. Delete the Google API Project & Credentials


- Go to https://console.developers.google.com/cloud-resource-manager 
- Select `WebIDF` and click `DELETE`  
Type in the ID of the project, which might have a slightly different name (shown above the text box) click `Shut Down`  

<img width="1552" alt="image" src="https://github.com/user-attachments/assets/a6619e65-197f-4b33-ba70-48109a4a67c6">

# 2. Delete the Cognito ID Pool
- Go to the cognito console https://console.aws.amazon.com/cognito/home?region=us-east-1  
- Select `WebIDFIDpool`  
- Click `Delete Pool`

# 3. Delete the CloudFormation Stack
- Go to the cloud formation console https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks?filteringText=&filteringStatus=active&viewNested=true&hideStacks=false  
- Select `WEBIDF`, click `Delete` then `Delete Stack`
