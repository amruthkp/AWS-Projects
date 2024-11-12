# 1. Download index.html and scripts.js from the S3   

- Go to the S3 Console https://s3.console.aws.amazon.com/s3/home?region=us-east-1    
- Open the `webidf-appbucket-` bucket   
- select `index.html` and `scripts.js`, click `Download` & save the file locally  

# 2. Update files with your specific connection information  

- Open the local copy of `index.html` in a code editor.    
- Locate the `REPLACE_ME_GOOGLE_APP_CLIENT_ID` placeholder in Line 15.  
- Replace this with YOUR CLIENT ID and Save `index.html`  

<img width="1031" alt="image" src="https://github.com/user-attachments/assets/94c03df0-14d8-4a67-92d3-7fb9105b0f30">

- Open the local copy of `scripts.js` in a code editor.   
- Locate the IdentityPoolId: `REPLACE_ME_COGNITO_IDENTITY_POOL_ID` placeholder    
- Replace the `REPLACE_ME_COGNITO_IDENTITY_POOL_ID` part with your IDENTITY POOL ID you noted down in the previous step  
- Locate the `Bucket: "REPLACE_ME_NAME_OF_PATCHES_PRIVATE_BUCKET" ` placeholder.  
- Replace `REPLACE_ME_NAME_OF_PATCHES_PRIVATE_BUCKET` with with bucket name of the `webidf-patchesprivatebucket-` bucket
- Save `scripts.js`  

# 3. Upload files

- Back on the S3 console, inside the `webidf-appbucket-` bucket.   
- Click `Upload`    
- Add the `index.html` and `scripts.js` files and click `Upload`

