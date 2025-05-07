# Business Value 

Using Docker, Terraform and Ansible we are able to deploy services quickly and efficiently on many servers around the world. The application we have deployed in this project in North Virginia was performing poorly in that region due to a lack of accessibility, by provisions servers on cloud infrastructure we have been able to deploy 2 microservices to help combat this issue and give the audience in North Virginia the same accessibility that the audience in Europe has.

## Docker

Using docker I was able to create 2 different images, one of the Database and one of the MVC. This allows me to push and containerise these images giving me access to all the resources needed to run these containers on AWS servers. This will also allow the app to scale as these containers can be run on any servers around the world, increasing the scope for the application.

## Terraform 

Terraform allowed me to provision the infrastructure of my servers remotely in North Virginia using AWS as my chosen cloud service provider, saving costs as I did not need to go to North Virgina, rent an office space in North Virginia or buy and hardware to act as servers. All of this was done remotely saving money and time. We can also deploy updates on this application remotely, which increases the scope for the project as new releases of the application can be released regularly. 

## Ansible 

Using Ansible we are able to install docker and run a docker-compose file on our server to run docker images.



