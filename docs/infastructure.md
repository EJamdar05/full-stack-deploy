## Infrastructure Needed
The following components are needed to deploy the site on AWS
* RDS Server Running Postgre 12 or 13 and that can accept all incomming traffic over IPv4
* Amazon S3 bucket to hold the FrontEnd and that is public, is configured to host a static website and has proper IAM/Cors Policy
* Elastic Beanstalk Environment to host the Backend API using Node.js 14 and SSH