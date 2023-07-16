## Introduction to Week 3
- storage and database
- rds  and amazon dynamodb

## Introduction to Week 3
- operating system, software, system file for the app
- static data like photo images
- structured data name, title and location
- two main types of storage - block and object
- block divides into chunks
- object as one
- static data mostly worm.. so object data storage works fine
- for frquent or high transaction rare--- block storage is better


Reading 3.1: Storage Types on AWS
https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/AZGDV/reading-3-1-storage-types-on-aws

## Amazon EC2 Instance Storage and Amazon Elastic Block Store
- internal and external  data storage
- internal - Amazon EC2 Instance Store  (direct  attached and fast) (lifecycle tied) -- ephemeral storage
- external  - Amazon elastic block store (ebs volumes separate from ec2 instance) (detachable from one instance to another)
- ebs multi attach
- persistent storage
- SSD and HDD backed volumes
- backing up data
- snapshots (stored  redundantly)
- EC2 has a one-to-many relationship with EBS volumes
- EBS Provisioned IOPS SSD, EBS General Purpose SSD, Throughput Optimized HDD, Cold HDD
- random vs sequential io

## Object Storage with Amazon S3
- ebs multi attach do not have multi attach for all the instance
- ebs volumes can only be attached to ec2 instances
- size limit for ebs
- amazon simple storage service (s3)
- accessed through URL
- object limit for 5 tb (flat structure)
- distributed storage
- bucket created first then object stored
- folder can be created in the bucket
- s3 private by default
- ACL - access control list
- iam and s3 bucket policy for access control of s3 object
- versioning while uploading objects in s3

## Choose the Right Storage Service
- EFS , S3, EBS, ECIS
- internal and external storage
- persistent and ephemeral storage
- file storage, object storage, block storage


## Introduction to Exercise 5
## Demo Creating an Amazon S3 Bucket

## Explore Databases on AWS
- rds and RDBMS
- MySQL
- acid property (atomicity, consistency, isolation, durability)

## Amazon Relational Database Service
- aws rds is a relational database that helps you set up, operate, and scale a business.
- amazon aurora to take advantage of the high durability
- rds dbs get places inside a subnet
- rds multi az deployment
- managed rds lowers the operational overload
- DB subnet group
- db instance should be in private subnet to ensure safety
- Automatic backups
- Manual snapshots


## Purpose-Built Databases on AWS
- specific use case for database
- employee db is just a lookup table and doesn't really required RDBMS (rdbms is expensive)\
- amazon dynamodb NoSQL database that stores key-value pair and document data
- documentdb (content management) and amazon neptune(for social web -- uses graph database (also use case fraud detection))
- amazon qldb(immutable ledger)

## Introduction to Amazon DynamoDB
- standalone tables
- data is organised into items and items has attributes
- stores data redundantly across AZS
- doesn't require well-defined schema
- best for less rigid and accessed frequently
- MongoDB is a document-based system, whereas MySQL is a table-structured system
- reading 3.8 and reading 3.9

## Introduction to Exercise 6
- exercise using dynamodb
- ref. exercise 6

## WEEK 3 DONE
~~ Soumyajeet Bal


















