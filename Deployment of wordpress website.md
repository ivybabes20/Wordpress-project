Steps taken to deploy a wordpress website:

- i first started by creating a Key pair to be used when creating cloudformation stack.

A) Steps in creating cloudformation:

- Step 1: create stack i selected "use a sample template" then later selected a simple "wordpress blog template"(This template installs wordpress with a local mysql database for storage) i chosed this template because in the problem statement it is asked to configure the wordpress instance for a development and testing environment.

- Step 2: specify stack details. That is Stack name, Parameters-Instant type(here i selected t2 micro ), Key name (i selected the key pair we previously created), ssh location ( 0.0.0.0/0)

- Step 3: Configure stack options. Here i allowed all the parameters in the default state.

- Step 4: Review wordpress-stack and then clicked on submit.

B) After creating the cloudformation, i had to create an AMI image of the wordpress instance.(An image (also referred to as an AMI) defines the programs and settings that are applied when you launch an EC2 instance. You can create an image from the configuration of an existing instance.)

C) Configure Auto Scaling to launch a new WordPress instance:
Open the ec2 console and clicked on Auto scaling group then later click create auto scaling group:

Step 1: Choose launch template or configuration
here i named my auto scaling group , launch template using the AMI i created from wordpress intance.

Step 2:choosed instance launched options.Here i used the default VPC , availability zones and 2 subnets

Step 3: Configure Advanced options. Here i left everything as default

Step 4: Configure group size and scaling policies.Here i set the minimum capacity at 2, desired capacity at 4 and maximum capacity at 4. Below scaling policies, i selected Target tracking scaling policy,Metric type i selected Average CPU utilization, Target value:50 , instances need 120 seconds warm up before including in metric

The rest of the steps i left in the default form.

Lastly i clicked create auto scaling group.

D) Configure the new WordPress instance to shut down automatically 







