
#                                                   Implementing Web Identity Federation

In this project, we will implement a simple serverless application utilizing Web Identity Federation. The main focus is to showcase how to integrate Google as an identity provider with AWS services to create a seamless authentication and authorization process. Here's an overview of the key components and technologies involved:




- **Amazon S3**: Hosting the front-end application.

- **Google API Project**: Act as an Identity Provider (IDP).

- **Amazon Cognito**: User management and authentication.

- **AWS IAM Roles**: Manage permissions and access to AWS resources.

The application runs from a browser, gets the user to login using a Google ID and then loads all images from a private S3 bucket into a browser using presignedURLs.




![ARCHITECTURE-ENDSTATE](https://github.com/user-attachments/assets/9eadb523-2c97-4ed7-8644-fa5399e83b08)



## Environment Setup

Cloudformation File

[WEBIDF](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?templateURL=https://learn-cantrill-labs.s3.amazonaws.com/aws-cognito-web-identity-federation/WEBIDF.yaml&stackName=WEBIDF)

## Steps

 - [Provision the environment and review](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)

 - [Create Google API Project & Client ID](https://github.com/matiassingers/awesome-readme)
 
 - [Create Cognito Identity Pool](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)

 - [Update App Bucket & Test Application]()

 - [Cleanup]() 

