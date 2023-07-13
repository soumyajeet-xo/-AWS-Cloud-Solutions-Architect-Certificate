# AWS Compute
## AWS Compute
- amazon elastic container service (ecs)
- amazon elastic kubernetes service (eks)
- serverless option (ews lambda)
- network (vpc)

## Compute as a Service on AWS
- container, serverless compute

Reading 2.1: Compute as a Service on AWS --- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/gheft/reading-2-1-compute-as-a-service-on-aws

Compare different compute service : https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html

## Introduction to Amazon Elastic Compute Cloud
- AMI amazon machine image - contains information about how you want os to be configured, permssion.
- list of instace type
- G instance for graphic oriented

## Amazon EC2 Instance Lifecycle
- elastic, flexible, start and stop anytime
- hibernate phase of instance
- termination protection


Reading 2.25: Amazon EC2 Instance Lifecycle
- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/AD2iI/reading-2-25-amazon-ec2-instance-lifecycle

Exercise 3: Launching an EC2 Instance
- https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/DEV-AWS-MO-GCNv2/exercise-3-compute.html
- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/s81nc/exercise-3-launch-and-corporate-directory-application-on-amazon-ec2

## Demonstration: Launching the Employee Directory Application
- using defualt vpc
- The AMI is the Amazon machine image, and this is a template that contains the software configuration for your instance on boot like the operating system
- no keypair selected... as we are going to connect through aws console
- Auto assign public ip allows publicly reachable ip address
- iam instance profile - to EmployeeWebApp (API calls to s3 and dynamodb)
```
#!/bin/bash -ex
wget https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/DEV-AWS-MO-GCNv2/FlaskApp.zip
unzip FlaskApp.zip
cd FlaskApp/
yum -y install python3-pip
pip install -r requirements.txt
yum -y install stress
export PHOTOS_BUCKET=${SUB_PHOTOS_BUCKET}
export AWS_DEFAULT_REGION=<INSERT REGION HERE>
export DYNAMO_MODE=on
FLASK_APP=application.py /usr/local/bin/flask run --host=0.0.0.0 --port=80
```

## Container Services on AWS
- container are portable and scalable (includes all code and dependencies.... behaves the same throughout different environments like development, QA, production)
- aws elastic container service, amazon aws kubernetes service.
- aws fargate

Reading 2.3: Container Services on AWS : https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/AAEwe/reading-2-3-container-services-on-aws

## Introduction to Serverless
- fleet of instances
- serverless means you cannot see or access the underlying infrastructure but can use it. (maintenance and underlying management are abstracted)
- ec2 - more control , lambda - more convenience (serverless)

## Serverless with AWS Fargate
- ecs and eks are container orchestrators (lifecycle)
- compute platform (where container run)
- aws fargate (managed serverless platform)

## Introduction to AWS Lambda
- one of the serverless option
- lambda function (runs only when triggered... like an HTTP request) 
- 1 or 1000 request, aws lambda can scale the function to meet demand
-  the HTTP PUT method is used to update an existing resource, while the POST method is used to create a new resource.
-  image resize  lambda function

## Choose the Right Compute Service
- 
