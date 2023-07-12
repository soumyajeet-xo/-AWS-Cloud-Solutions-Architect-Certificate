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
- three mains ways ( aws management console, aws CLI interface, aws software development kits )
- management console... uses prompts..more like a GUI.
- Command line interface (download or using aws cloudshell)
- cli reduces accidental human errors as it automates... using scipts to repeat those commands too.
- SDK used to interact programmatically. (popular lang like java, python, etc ).
- employee directory uses Python and flask (pyhton SDK can be used to interact with aws)

Reading ( Reading 1.4: Interacting with AWS): https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/pkNoh/reading-1-4-interacting-with-aws
docs : 
Aws complete  doc : https://docs.aws.amazon.com/index.html
- management console : https://docs.aws.amazon.com/awsconsolehelpdocs/latest/gsg/learn-whats-new.html
- cli ; https://aws.amazon.com/cli/
- tools : https://aws.amazon.com/developer/tools/

## Introduction to Exercise 1
- billing alert
- account creation
- region change
- employee directory hosting
- 









