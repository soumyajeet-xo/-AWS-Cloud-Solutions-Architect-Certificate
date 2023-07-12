# Welcome to the Course
## Welcome to AWS Cloud Technical Essentials
- compute, networking, database, storage, and more
- computing- elastic computing, aws container services
- serverless computing like aws lambda
- networking - vac
- how and when to use s3, ec2
- amazon dynamodb
- scaling and load balancing
-   Reading syllabus: https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/Wwi4O/welcome-to-the-course

## Meet the Instructors
- Principal cloud technologist in aws - top role in... one who also builds and teaches in the organization (Morgan Willis)
- senior cloud technologist

## Course Feedback
- repost. aws for query related to AWS

# Getting Started with AWS Cloud
## Getting Started with AWS Cloud
- theory and benefits of the cloud
- AWS global infrastructure covering regions and available zones
- security
- CRUD Employee app (create read update delete)
- amazon vpc and ec2(provides VM on aws ) in different availability zones
- amazon rds for database
- images will be stored in s3
- amazon cloudwatch to monitor the solution
- amazon elastic load balancing and amazon ec2 for scaling
- amazon Iam (identity and access management ) for security and identity

READING :
- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/K1O0b/reading-1-2-what-is-aws
- Cloud computing is the on-demand delivery of IT resources over the Internet with pay-as-you-go pricing.
The Six Benefits of Cloud Computing
- Pay as you go
- Benefit from massive economies of scale
- Stop guessing capacity
- Increase speed and agility
- Stop spending money running and maintaining data centers
- Go global in minutes

## AWS Global Infrastructure
- data stored in the cloud can be accessed throughout the globe.
- aws used redundancy for data safety
- availability zones called the region.
- aws also redundant availability zones by clustering
- to choose az, compliance(requirement), latency(closer to userbase), pricing (can vary from region to region) , and service availability.
- global edge location are used to cache locations closer to the end user. (cache frequently accessed content) from closest edge location.. amazon cloudfront


- READING: https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/sIxO9/reading-1-3-aws-global-infrastructure
- a region is a cluster of availability zones
-  An AZ comprises one or more data centers with redundant power, networking, and connectivity.
-  aws cloud > aws regions > aws az > aws resources 

## Interacting with AWS
- logical management of virtual infrastructure through aws application programming interface.
- three mains ways ( aws management console, AWS CLI interface, aws software development kits )
- management console... uses prompts..more like a GUI.
- Command line interface (download or using aws cloudshell)
- cli reduces accidental human errors as it automates... using scripts to repeat those commands too.
- SDK used to interact programmatically. (popular lang like Java, python, etc ).
- employee directory uses Python and Flask (python SDK can be used to interact with aws)

Reading ( Reading 1.4: Interacting with AWS): https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/pkNoh/reading-1-4-interacting-with-aws
docs : 
Aws complete  doc: https://docs.aws.amazon.com/index.html
- management console: https://docs.aws.amazon.com/awsconsolehelpdocs/latest/gsg/learn-whats-new.html
- CLI : https://aws.amazon.com/cli/
- tools: https://aws.amazon.com/developer/tools/

## Introduction to Exercise 1
- billing alert
- account creation
- region change
- employee directory hosting
- 

## Security and the AWS Shared Responsibility Model
- aws follows the shared responsibility model. (vary from service to service
- aws - security of the cloud
- user - security in the cloud ( patching upgrades, access control, firewall)

## Protect the AWS Root User
- email account which created the account is the root user (unrestricted access)
- single-factor authentication
- MFA (multi-factor authentication) can be used to access specific AWS service
- Reading: https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/lZN9N/reading-1-6-protect-the-aws-root-user
- 

## Introduction to AWS Identity and Access Management
- setup access control in-app level
- access management
- IAM can manage access management and API calls(action)
- IAM can give access/permissions to users
- IAM policies are JSON documents
- policy can be attached to specific user and group
- Reading 1.7: Introduction to AWS Identity and Access Management: https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/3ELvV/reading-1-7-introduction-to-aws-identity-and-access-management

## Role-Based Access in AWS
- I am roles also have credentials (temporary)
- To assign a role for employee dir app -----
- IAM > Roles > Create Roles > Common use case ec2 check > 
- roles for third-party identity providers and clients (federated users)
-  identity provider (IdP)
- aws iam identity centers
- Reading 1.8: Role-Based Access in AWS
- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/hyURm/reading-1-8-role-based-access-in-aws

## Introduction to Exercise 2
- To implement the previously discussed IAM user best practices like not using root users.

Exercise 2: Following IAM Best Practices: https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/RQIuX/exercise-2-following-iam-best-practices
Exercise 2: Working with IAM: https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/DEV-AWS-MO-GCNv2/exercise-2-iam.html

12 digits account id and IAM user: top right corner

The IAM role is used for federated logins (using an IdP with SAML tokens for example), and they don't have permanent access keys that you can download like regular IAM users have (the "an IAM role doesn't have any credentials" part)



## Demo AWS IAM
- managed policies are predefined policies (JSON FILE)
- Effect either allow or deny
- * is a wild card, all API calls are allowed against the service.
- is best practice to attach a policy to groups and not users directly
- access keys will allow users to make programmatic calls like aws cl

## Hosting the Employee Directory Application on AWS  
Load balancing is the method of distributing network traffic equally across a pool of resources that support an application.

- instance can be considered as one single virtual machine
- default vpc
- create ec2

```
#!/bin/bash -ex
wget https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/DEV-AWS-MO
GCNv2/FlaskApp.zip
unzip FlaskApp.zip
cd FlaskApp/
yum -y install python3-pip
pip install -r requirements.txt
yum -y install stress
export PHOTOS_BUCKET=${SUB_PHOTOS_BUCKET}
export AWS_DEFAULT_REGION=us-east-1
export DYNAMO_MODE=on
FLASK_APP=application.py /usr/local/bin/flask run --host=0.0.0.0 --port=80
```







# WEEK 1 DONE ~ Soumyajeet Bal





