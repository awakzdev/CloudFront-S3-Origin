### A Terraform Infrastructure to provision a CloudFront and an S3 private bucket as its origin to allow static-page hosting
 <hr>
 
 ##### _Credentials key file is set within ~/.aws/credentials - Please create or use a different approach. [refer to documentation](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)_
*Your credentials file should look like this*
 ```
 [default]
# This key identifies your AWS account.
aws_access_key_id = foo
# Treat this secret key like a password. Never share it or store it in source
# control. If your secret key is ever disclosed, immediately use IAM to delete
# the key pair and create a new one.
aws_secret_access_key = foo
 ```
 
 ##### _SSH Key will need to be created using the following_
 `ssh-keygen -t ed25519` > You'll need to rename it to ec2 otherwise please edit the aws_key_pair resource under main.tf.
 
 
 ## *Its purpose is to serve the following configuration*
```
S3 - Will create a private bucket "ACL- Private"
IAM Policy - Set to S3:GetObject on *
CloudFront - Will set S3 as its origin allowing to host from bucket
view-request.js - will append .html to website URL (Appended within "aws_cloudfront_function").
```
