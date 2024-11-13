# 1. Create Google API PROJECT  

Web applications use Google API Client Libraries or Google OAuth 2.0 endpoints to implement OAuth 2.0 authorization to access Google APIs. Any application that uses OAuth 2.0 to access Google APIs must have authorization credentials that identify the application to Google's OAuth 2.0 server. 
 In this step we will create those authorization credentials.  

For this we need valid google login, GMAIL will do.  
- Go to Google Credentials page https://console.developers.google.com/apis/credentials and Login using your gmail credentials.

<img width="1549" alt="image" src="https://github.com/user-attachments/assets/c61cf338-81e5-4c56-9095-8b804611dddf">

  
- In the `Google API Console` , click the `Select a project` dropdown, and  click `NEW PROJECT` , enter project name `WebIDF`, or any other name and click `Create`.    

<img width="1548" alt="image" src="https://github.com/user-attachments/assets/771e6b6c-ca67-4470-b5b2-68ef3da33e49">


# 2. Configure Consent Screen  
- Click `Credentials`  
- Click `OAuth consent screen` because our application will be usable by any google user, we have to select external users  
- Check the box next to `External` and click `CREATE`

<img width="1548" alt="image" src="https://github.com/user-attachments/assets/f5c92dc3-c089-453b-b5ea-a0e45499f76e">


- enter `WebIDF` in the `App Name` box.   
- enter your own email in `user support email`  
- enter your own email in `Developer contact information`  
- Click `SAVE AND CONTINUE`   
- Click `SAVE AND CONTINUE`  
- Click `SAVE AND CONTINUE`  
- In the Summary page, click `BACK TO DASHBOARD`     

<img width="1554" alt="image" src="https://github.com/user-attachments/assets/794d7cdf-e705-48bf-8f7c-eda24286c9b5">

# 3. Create Google API PROJECT CREDENTIALS  

- Click `Credentials` on the menu on the left   
- Click `CREATE CREDENTIALS` and then `OAuth client ID`   
- In the `Application type download` select `Web Application`, Under Name enter `WebIDFServerlessApp`  

We need to add the `WebApp URL`, this is the distribution domain name of the cloudfront distribution (making sure it has https:// before it)  
- Click `ADD URI` under `Authorized JavaScript origins`   
- Enter the `Distribution DNS Name` of your CloudFront distribution `https://d2nmndy3vlq8c7.cloudfront.net`   
- Click `CREATE`  
- OAuth client created popup is displayed. Note down the `Client ID` you will need it later and click `OK`   

<img width="1549" alt="Screenshot 2024-11-11 at 16 53 57" src="https://github.com/user-attachments/assets/68c08dc8-2544-43b2-9a0c-d120cc8f0128">


