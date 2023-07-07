Set Up and Monitor a WordPress Instance for Your Organization

Problem Statement and Motivation

Problem Statement:

In this project, i was able to launch a WordPress instance using AWS CloudFormation and monitor the instance using Amazon Route 53.

Motivation:

Your organization publishes blogs and provides documentation services
for other businesses and technologies. You have been asked to:

• Set up a live WordPress instance to publish blogs
• Set up a WordPress instance that can be used for development and
testing purposes so that any work done on this instance will not impact
the live blog
• Configure the WordPress instance for development and testing
purposes, which will be available only for business hours (9 AM–6 PM)
• Monitor the health of the WordPress instance 

Industry Relevance:

Skills used in the project and their usage in the industry are given below:

• AWS console: The AWS Management Console is a web application that
includes and references several service consoles for managing AWS
services.
• AWS CloudFormation: It is a service that aids users in modeling and
configuring their AWS resources so they can focus more on their AWSbased apps and spend less time maintaining those resources.
• EC2 Instance: Amazon EC2 provides a large set of instance types that
are customized to certain use cases.

Task (Activities)

1. Create a CloudFormation stack
2. Create an AMI of the WordPress instance
3. Configure Auto Scaling to launch a new WordPress instance
4. Configure the new WordPress instance to shut down automatically
5. Monitor the instance using Availability Monitoring feature of the R53