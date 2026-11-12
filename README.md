## Overview
- [x] Create custom VPC
- [x] Create custom Subnet
- [x] Create Route Table and Internet Gateway
- [x] Provision EC2 Instance
- [x] Deploy nginx Docker container
- [x] Create Security Group (Firewall)
<img width="1320" height="409" alt="image" src="https://github.com/user-attachments/assets/0cd33eb0-dd8a-4971-bd9d-59e86d987079" />

## CLI commands

### aws cli setup

    aws configure

### initialize

    terraform init

### preview terraform actions

    terraform plan

### apply configuration with variables

    terraform apply -var-file terraform-dev.tfvars

### destroy a single resource

    terraform destroy -target aws_vpc.myapp-vpc

### destroy everything fromtf files

    terraform destroy

### show resources and components from current state

    terraform state list

### show current state of a specific resource/data

    terraform state show aws_vpc.myapp-vpc    

### set avail_zone as custom tf environment variable - before apply

    export TF_VAR_avail_zone="eu-west-3a"

### set aws configuration through env variables

    export AWS_ACCESS_KEY_ID="anaccesskey"
    export AWS_SECRET_ACCESS_KEY="asecretkey"
    export AWS_DEFAULT_REGION="us-west-2"

## Final outcome
### EC2 instance
```
[ec2-user@ip-10-0-10-216 ~]$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                                   NAMES
8c29b5a9e41a   nginx     "/docker-entrypoint.…"   10 minutes ago   Up 10 minutes   0.0.0.0:8080->80/tcp, :::8080->80/tcp   relaxed_hopper
```
### Nginx welcome page
<img width="1316" height="591" alt="image" src="https://github.com/user-attachments/assets/15250be8-b967-4e71-b475-0ec95b8cd51b" />

### AWS console
<img width="1402" height="813" alt="image" src="https://github.com/user-attachments/assets/a8171769-a611-4369-8d2f-cba930029db6" />

