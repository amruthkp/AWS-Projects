# Application Migration with AWS

This goal of this project is to give you an overview of the migration strategies available to move workloads from on-premises environments to AWS cloud. For that we will create a lab environment that will try to provide a close resemble to what we will see in a real migration.

## Source Environment

The most common source environment are on-premises virtualized datacenters. For this project, the source environment will be simulated by a segregated Amazon VPC named SourceVPC, deployed within the same AWS account.

![image](https://github.com/user-attachments/assets/42fea978-5a04-4d2a-9523-d155868e6858)

Within that source environment, we have our sample workload deployed:

1. **Application (Source-Webserver)** - eCommerce Web Application, written in PHP 7.x (Wordpress and WooCommerce), hosted on Linux.
1. **Database (Source-DBServer)** - Relational data persistency layer, using self-managed MySQL 5.7.x, hosted on Linux.

## Target Environment

The migrations are going to move the workload components from the source to the target environments. This project has a target environment following a standard Amazon VPC topology. This is an Amazon VPC named TargetVPC, provisioned in the same AWS account and AWS Region of the source environment, and we will use it across 2 Availability Zones for High Availability purposes.

![image](https://github.com/user-attachments/assets/04425a04-0527-49b2-bc61-e0206394defc)

The target environment is mostly empty in purpose, and the resources will be created as we progress in the migration journey.
