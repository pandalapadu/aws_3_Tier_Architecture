AWS Three Tier Web Architecture
-----------------------------------
**Description:**

This workshop is a hands-on walk through of a three-tier web architecture in AWS. We will be manually creating the necessary network, security, app, and database components and configurations in order to run this architecture in an available and scalable manner.

**Pre-requisites:**
1. An AWS account. If you don’t have an AWS account, “Create an AWS Account”.
2. IDE or text editor of your choice.
*********************************************************************************************************
![3TierArch](https://github.com/pandalapadu/aws_3_Tier_Architecture/assets/59242614/11ba72b0-9b29-4b9d-81b6-d9d6d3ce3f9f)

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.
