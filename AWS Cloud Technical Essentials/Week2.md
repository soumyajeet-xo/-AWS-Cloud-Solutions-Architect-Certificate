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

## Networking on AWS
- default vpc provide easy way to get started.
- Reading 2.5: Networking on AWS
- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/Zq1Wb/reading-2-5-networking-on-aws

## Introduction to Amazon VPC
- acts as a wall or boundary
- region and ip range
- to create subnet with internet access
- vpc, az, ip range(cidr) requirements
- A public subnet is a subnet that is associated with a route table that has a route to an Internet gateway. This connects the VPC to the Internet and to other AWS services. A private subnet is a subnet that is associated with a route table that doesn't have a route to an internet gateway.
- vpc are isolated that means any resources we put inside the vpc, are seperated
- internet gateway connnects vpc to internet( like modem connects computer to internet)
- internet gateway attach to vpc
- traffic flow between aws and on-premise data center (no direct access to the internet) - virtual private gateway (encrypted VPN connection from )
- high availability (duplicate resources)

## Reading 2.6: Introduction to Amazon VPC
- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/svQtl/reading-2-6-introduction-to-amazon-vpc
For example, consider a VPC with the IP range 10.0.0.0/22. The VPC includes 1,024 total IP addresses. This is divided into four equal-sized subnets, each with a /24 IP range with 256 IP addresses. Out of each of those IP ranges, there are only 251 IP addresses that can be used because AWS reserves five.

Internet Gateway 

To enable internet connectivity for your VPC, you need to create an internet gateway. Think of this gateway as similar to a modem. Just as a modem connects your computer to the internet, the internet gateway connects your VPC to the internet. Unlike your modem at home, which sometimes goes down or offline, an internet gateway is highly available and scalable. After you create an internet gateway, you then need to attach it to your VPC.  

Virtual Private Gateway  

A virtual private gateway allows you to connect your AWS VPC to another private network. Once you create and attach a VGW to a VPC, the gateway acts as anchor on the AWS side of the connection. On the other side of the connection, you’ll need to connect a customer gateway to the other private network. A customer gateway device is a physical device or software application on your side of the connection. Once you have both gateways, you can then establish an encrypted VPN connection between the two sides. 

## Amazon VPC Routing
- route table contains a set of rules called routes used to determine where the network traffic is redirected
- route table > target locale (all resources can communicate locally)
- If you use 0.0. 0.0/0 , you enable all IPv4 addresses to access your instance using SSH.
-  *** 1 VPC, 4 Subnets(1 public and 1 private in both az), 2 public subnet are associated with route tables to allow internet access through the internet gateway
-  private subnets have not route table so they follow the rules of the main route table(local traffic only)


## Secure Your Network with Amazon VPC Security
- to secure vpc
- network access control list(network acl) (firewall in the subnet level)
- security groups and network acl are powerful tools to manage traffic

## Hybrid Connectivity with AWS
- hybrid deployment
- in was (use of vpc)
- on-premises (own solution)
- aws VPN (securely connect remote network to aws)
- site to site (remote network to vpc)
- was client VPN (administers to datacenter or aws)
- vpc doorway to private datacenter
- aws direct connect(never touches public internet)

Reading 2.7: Amazon VPC Routing and Security
- https://www.coursera.org/learn/aws-cloud-technical-essentials/supplement/nZ3Px/reading-2-7-amazon-vpc-routing-and-security
- Reading 2.7: Amazon VPC Routing and Security

## Introduction to Exercise 4
Exercise 4: Creating a VPC and relaunching the Corporate Directory Application on Amazon EC2
- https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/DEV-AWS-MO-GCNv2/exercise-4-networking.html





