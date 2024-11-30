## **This Terraform Template:**
- Build 2 ASGs:
- One for Port 80
- One for Port 443
- IS routed through a single Load Balancer
- Uses a purchased domain
- Adds WAF

User must add SNS messaging


## **COMMANDS - PRIMARY**
## Basic commands used

`terraform init`

`terraform validate`

`terraform plan`

`terraform apply`

`terraform destroy`

`terraform plan` - see a preview → a list of actions that terraform will preform. see the difference between the current and desired state: 

`terraform apply -auto-approve`  → apply changes automatically without approving

`terraform destroy`  → will remove all of the resources  





## **COMMANDS - DESCRIPTION**
### initialize

`terraform init`


### preview terraform actions

`terraform plan`


### apply configuration with variables

`terraform apply -var-file terraform-dev.tfvars`


### destroy a single resource

`terraform destroy -target aws_vpc.myapp-vpc`


### destroy everything from tf files

`terraform destroy`


**State**:
### show resources and components from current state

`terraform state` - see the list of sub commands for terraform state

`terraform state list` - a list of the all the resources that are in the state

`terraform state show -<resource>` - show a specific resource . Get to know the attributes AWS generates


### show current state of a specific resource/data

`terraform state show aws_vpc.myapp-vpc`


### set avail_zone as custom tf environment variable - before apply
## Example:
`export TF_VAR_avail_zone="us-west-2a"`
