This project aims to learn how to set up a complete CI/CD pipeline using Terraform and GitHub Actions. 

A sample application, nodeapp, is provided. Terraform is used to deploy infrastructure, including an AWS EC2 instance and S3 bucket. The EC2 instance hosts the application, while S3 stores the Terraform state file. GitHub Actions automate the deployment of infrastructure and the sample application within it. The workflow is triggered by every commit pushed to the main branch of the repository. The first workflow deploys cloud infrastructure by executing Terraform commands. The second workflow deploys the application within this infrastructure. It begins by pushing a Docker image to the AWS private repo and then pulling the repo inside the EC2 instance. Once the image is pulled, it runs the application on port 8080. 
