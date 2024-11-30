# Deployment

1. Login to AWS Account with Administrator privileges. 
1. Click [Here](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=ApplicationMigrationWorkshop&templateURL=https://ws-assets-prod-iad-r-pdx-f3b3f9f1a7d6a3d0.s3.us-west-2.amazonaws.com/c6bdf8dc-d2b2-4dbd-b673-90836e954745/migration_workshop_source_template.yml) to launch the CloudFormation stack.

1. On the Step 1 - Specify template confirm that the URL https://ws-assets-prod-iad-r-pdx-f3b3f9f1a7d6a3d0.s3.us-west-2.amazonaws.com/c6bdf8dc-d2b2-4dbd-b673-90836e954745/migration_workshop_source_template.yml  is entered in the Amazon S3 URL field and press Next.

<img width="1535" alt="image" src="https://github.com/user-attachments/assets/00f636e9-441e-46ae-8cc9-2dabd01affca">


1. On the Step 2 - Specify stack details screen make sure ApplicationMigrationWorkshop is entered in the Stack name field and press Next

   <img width="1533" alt="image" src="https://github.com/user-attachments/assets/f036b2fb-ff57-4595-bd8a-f5076726c41c">


1. On the Step 3 - Configure stack options screen don't make any changes, just press Next

1. On the Step 4 - Review screen, scroll to the bottom of the page and check all checkboxes, as on the screenshot below, then press Create stack for the template to be deployed.

<img width="1114" alt="image" src="https://github.com/user-attachments/assets/1d506f6b-d0c9-4810-87c8-b68255d7bb7a">
   

When the template is in the CREATE_COMPLETE you can find information about created source environment by going to AWS Console -> CloudFormation, selecting ApplicationMigrationWorkshop stack and going to the Outputs tab. You will see information like on the screenshot below.

<img width="1540" alt="image" src="https://github.com/user-attachments/assets/83438a0c-b471-4bc1-aca0-b03ed5207af0">


7. Copy - paste this information, as you will use it during the lab.
