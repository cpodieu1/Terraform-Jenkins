# Terraform-Jenkins
Overview
This repository will demonstrate an example GitOps workflow with Terraform and Jenkins.

The configuration in this repository was updated and now supports Terraform v0.12.19.

Video can be found here:

https://youtu.be/qFjGqPw1NUY

Requirements
Terraform installed on Jenkins
Correct plugins installed on Jenkins
GitHub access token
AWS credentials
S3 bucket
Setup Bucket
You will need to create a bucket and reference the bucket name in the following section of main.tf:

terraform {
  backend "s3" {
    bucket = "maliano"
    key    = "terraform.tfstate"
    region = "us-east-1"
  }
}
