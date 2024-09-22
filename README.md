#terraform project to create s3 and ec2
provider "aws" {
    region = "us-east-2"  # Set your desired AWS region
}

resource "aws_instance" "example" {
    ami           = "ami-0c55b159cbfafe1f0"  # Specify an appropriate AMI ID
    instance_type = "t2.micro"
}


resource "aws_s3_bucket" "s3_bucket" {
  bucket = "ty-s3-demo" # change this
}
