### A Terraform Infrastructure to provision a cloudfront and an S3 private bucket as its origin to allow static-page hosting
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
