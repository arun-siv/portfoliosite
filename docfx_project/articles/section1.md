# Managing and Monitoring access on aws
We require the following tools
- postman
- awscli
- terminal/putty

## Use case for managing aws environment
Role of IT people is paramount in protecting the resources when moving the workloads to cloud
Everything starts when HCL receives root credentials.

## AWS IAM
* Identify and access management - Securely control to Aws resources
* Who is authenticated ( Signed in) 
* Who is authorized ( to use the resources)

## Following are IAM identities
1. Users - an entity that you create in aws
2. Groups - group of users
3. Roles - an identity that is assumable
Management of access by creating policies and attaching them to IAM identities.
### Securing root access
- Secure root account with mfa
- root access key delete
- Multiple platform available even Yubikey

## How to add mfa device to iam user
```
aws iam create-virtual-mfa-device \
--virtual-mfa-device-name arun_device \
--bootstrap-method Base32StringSeed \
--outfile /tmp/txt 
```