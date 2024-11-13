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

# 4. Test application  

- Open the `WebApp URL` you noted down earlier, the `distribution domain name` of the cloudfront distribution  
This is the web app, with no access to any AWS resources right now  
- Open your browser `web developer tools` (firefox tool->browser tools-> web developer tools)  
it might be called browser console in other browsers, it will log any output from javascript running in your web browser.  
- With the browser console open, Click `Sign In`    
- Sign in with your google account  

<img width="1550" alt="image" src="https://github.com/user-attachments/assets/63d41806-9cc7-4ddd-a6e5-9e63d8954f72">


When you click the Sign In button a few things happen:-  (watch the console)  

- You authenticate with the Google IDP  
- a Google Access token is returned  
- This token is provided as part of the API Call to Cognito  
- If successful this exchanges this for Temporary AWS credentials  
- These are used to list objects in the private bucket  
- for all objects, presignedURLs are generated and used to load the images in the browser.

<img width="1551" alt="image" src="https://github.com/user-attachments/assets/e04bdffa-cd05-4b57-99c5-23cca4141b31">


## Caching Issue

If you're having issues signing in, the CloudFront distribution is caching the old `index.html` and `scripts.js` files. 

<img width="1545" alt="image" src="https://github.com/user-attachments/assets/1accb9a4-1843-44cc-b08d-48fe98d70ea8">

To fix this, you can invalidate the cache by following these steps:
  - Go to the CloudFront console
  - Select the CloudFront distribution that you created
  - Click on the `Invalidations` tab
  - Click on `Create invalidation`
  - Enter `/index.html` and `/scripts.js` in the `Object Paths` field
  - Click on `Create invalidation`

<img width="1545" alt="image" src="https://github.com/user-attachments/assets/cfba557d-6655-4921-bec7-6d4b0f6e5d90">
