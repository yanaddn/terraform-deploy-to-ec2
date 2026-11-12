## Overview
- [x] Create custom VPC
- [ ] Create custom Subnet
- [ ] Create Route Table and Internet Gateway
- [ ] Provision EC2 Instance
- [ ] Deploy nginx Docker container
- [ ] Create Security Group (Firewall)
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

