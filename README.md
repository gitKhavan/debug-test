# Debug Assignment CDO

## Project Overview

The purpose of this application is to deploy two microservices relating to the tour de france in North Virginia, due to its success in Europe, using Docker, Terraform, Ansible and AWS as the chosen cloud service provider.

## Docker

Docker is user to create images and container of the two microservices.
`docker build -t khavan123/tour-de-france-db:0.0.0.Release` - This command builds the image for the database, replace with your own username.

`docker build -t khavan123/tour-de-france-mvc:0.0.0.Release` - This command builds the image for the mvc, replace with your own username.

## Terraform 

Terraform is used to host the application in North Virginia by provisioning an EC2 instance using AWS.
When trying to launch this application, direct yourself to inside the terraform folder and perfom the folowing:

`terraform init` - to initialise terraform
`terraform apply` - to update the known state into the desired state

Once you have provisioned your server, you must transfer the docker-compose.yml using the following scp command:
`scp -i <path-to-identity-file> <path-to-file-to-copy> <remote-user>@<remote-dns-or-ip>:<location-to-send-file>`

## Ansible 

Ansible allows us to configure the instrastructre that we have just created. Direct yourself to the ansible folder and perform the following: 

`ansible-playbook playbooks/docker-install.yml` - to install docker using the docker-compose folder we sent over using the scp command
`ansible-playbook playbooks/docker-run.yml` to run the containers inside the server

The application should now be successfully deployed on the IP address of your server on port 3000

When done with this application, perform a `terraform destroy` command from inside the terraform folder to delete the servers we have provisioned on AWS.

