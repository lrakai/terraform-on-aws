# terraform-on-aws

Demonstrate how to manage AWS resources with Terraform. Piece-by-piece you will build up a two-tier architecture with web servers in private subnets in different availability zones and an Elastic Load Balancer in public subnets.

## Environment Diagrams

### Initial environment

![Initial environment](https://user-images.githubusercontent.com/3911650/36611765-bbba4128-1891-11e8-94c2-0fd1977f33b1.png)

### After Part 1

![After Part 1](https://user-images.githubusercontent.com/3911650/36611780-c7e86efc-1891-11e8-8a33-1bafadb3420e.png)

### After Part 2

![After Part 2](https://user-images.githubusercontent.com/3911650/36611782-cc7b798c-1891-11e8-90c7-b9ae97687fe6.png)

### Final Environment

![Final Environment](https://user-images.githubusercontent.com/3911650/36611759-b6b4b15e-1891-11e8-8408-1c28bef6e67d.png)

## Getting Started

Deploy the CloudFormation `infrastructure/cloudformation-1.json` template. The template creates a user with the following credentials and minimal required permisisons to complete the Lab:

- Username: _student_
- Password: _password_

You can also deploy a CloudFormation stack to jump ahead to part 2 or part 3 using `infrastructure/cloudformation-2.json` or `infrastructure/cloudformation-3.json`, repsectively.

## Instructions

- SSH into the Development instance
- Install Terraform 0.11.3:
    - wget https://releases.hashicorp.com/terraform/0.11.3/terraform_0.11.3_linux_amd64.zip
    - sudo unzip terraform_0.11.3_linux_amd64.zip -d /usr/local/bin/
- Copy the files in `src/part1` to a project directory
- Initialize the directory with `terraform init`
- Create the resources with `terraform apply`
- Copy the files in `src/part2` to the project directory
- Initialize the directory with `terraform init`
- Create the resources with `terraform apply`
- Copy the files in `src/part3` to the project directory
- Initialize the directory with `terraform init`
- Create the resources with `terraform apply`

## Cleaning Up

Destroy the resources managed by Terraform with `terraform destroy`. Delete the CloudFormation stack to remove all the remaining template resources.