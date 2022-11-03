<img src="https://github.com/kura-labs-org/kuralabs_deployment_1/blob/main/Kuralogo.png">
<h1 align="center">kuralabs_deployment_4<h1> 
  
# Deployment 4
## New Purpose
This deployment was to practice the process of deploying a flask app onto a VPC and onto the public subnet using Terraform
## The Steps
1. We would need an EC2 already with Jenkins
  - If an EC2 is not set up already, you would need to set up the Jenkins service
  - The EC2 should not be in the VPC
2. Create the infrastructure as Code
  - Used Terraform within my ec2 that hosts the Jenkins Server to create infrastructure
  - Created the VPC
  - Create the Availability Zones
  - Create the Subnet Masks and CIDR blocks
  - Create the route Tables
  - Created the internet gateway
  - Created the instances with the user data to automate the application launching
3. Followed the documentation to create and configure a jenkins agent
4. Link GitHub to Jenkins
  - Fork the repo with the Flask App
  - Create access token for Jenkins by using GitHub client
    - admin:repo_hook
5. Jenkins Pipeline creation
  - Create a new item which is a multibranch and/or freestyle project pipeline
  - Add github as a source for the pipeline
  - Validate the source for the pipeline
  - Attempt to build the pipeline given the gitHub repository
  - Added destroy stage to the jenkinsfile to automate the destruction of spun up resources
## New Additions
In Jenkins, I experimented with creating a freeform project to have a webhook to build whenever there is a push to this repository to automate the process
## Tips for Future Me
I would ideally like to make modules so I would be able to just replace information on variables instead of hard coding in data to pass into the fields and to make the process not only faster, but scalable as well. This deployment was easier as it built upon the previous deployment, except with having to code in the values for our infrastructure, instead of going to aws and manually entering it in the necessary fields.
 
