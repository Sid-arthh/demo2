# Aspen Aerogels Infra

## Introduction
This readme is to illustrate infrastructure creation for Aspen Aerogels Project.
It will create the below listed resources and advanced network resources for a required region.

### We will categorise the infra components as AWS Resources mentioned below
    1- Network
    2- Shared
    3- EMR
    4- Data

### Network 
In network we will be creating below listed resources for different environments.

    Virtual Private Cloud (VPC)
        VPC Flow Logs
        Subnets
            -Public
            -Private
            -Database
            -AppTools
        Internet Gateway
        
        Nat Gateway
        
        Route tables for the Public, Private, Database and apptools subnets
        
        Associate all Route Tables created to the correct subnet
        
        Database Subnet group - Provides an RDS DB subnet group resources without Internet
        
        Adding routes in Route Table for VPC Peering

## Pre-Requisites
    Before using this repo, ensure you have the following in place
    Configure Git, AWS CLI & Terraform must be installed on your system.

## Usage:
For creating any infra components, execute the following commands

    $ cd ..
    $ cd <infra-component>
    $ bash launch.sh

## For launching network (if required)
Move to network folder and execute the below commands

    $ cd /network
    $ bash launch.sh

(launch.sh will perform terraform init, terraform plan, terraform apply and will create the workspace if not exits)

### Shared 
In the shared  we have created below listed resources for different environments.

EC2
   -EC2 Standalone Instances
   -Security Groups
   -SSM
IAM
   -Roles
   -Policies
LAMBDA
   -Data Lambdas
   -Devops Lambdas
RDS
  -RDS Cluster
S3
  -raw-bucket
  -staging-bucket
  -curated-bucket

Secret Manager
    -devops-secrets
    -data-secrets

SNS Topic  

## Pre-Requisites
    Before using this repo, ensure you have the following in place
    Configure Git, AWS CLI & Terraform must be installed on your system.

## Usage:
For creating any infra components, execute the following commands

    $ cd ..
    $ cd <infra-component>
    $ bash launch.sh

## For launching network (if required)
Move to network folder and execute the below commands

    $ cd /network
    $ bash launch.sh

(launch.sh will perform terraform init, terraform plan, terraform apply and will create the workspace if not exits)


## DATA

In the data we have cretad below listed resources for different environments.

Anthena
    -Anthena Workgroup
    -Coudwatch Alarm

EMR
    -EMR serverless application
    -EMR studio

Glue
    -Data connection
        -JDBC Connection
        -Network Connection
    -Crawlers
    -IAM Glue Roles

Redshift
    -Redshift IAM role
    -Redshift sg
    -Redshift Cluster

Timestream
    -Timestream Database
    -Timestream Table

## Pre-Requisites
    Before using this repo, ensure you have the following in place
    Configure Git, AWS CLI & Terraform must be installed on your system.

## Usage:
For creating any infra components, execute the following commands

    $ cd ..
    $ cd <infra-component>
    $ bash launch.sh

## For launching network (if required)
Move to network folder and execute the below commands

    $ cd /network
    $ bash launch.sh

(launch.sh will perform terraform init, terraform plan, terraform apply and will create the workspace if not exits)
