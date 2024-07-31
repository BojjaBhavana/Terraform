# Terraform {
required providers {
aws = {
source = "hashicorp/aws"
version = "1.8"
}
}
required_version = ">= 1.2.0"
}

provider "aws" {
region = "India"
}
resource "aws_instance" "app_server" {
ami   = "ami-830c94e3"
instance_type = "t2.micro"
tags = {
Name = "Terraform_Demo"
}
}
