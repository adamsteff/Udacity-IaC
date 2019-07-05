# Udacity-IaC
Project: Deploy a high-availability web app using CloudFormation


## Step 1
Run servers.yml
`aws cloudformation create-stack --stack-name network --template-body file://network.yml --parameters file://network-params.json --capabilities CAPABILITY_IAM`

## Step 2
Run bastion-server.yml
`aws cloudformation create-stack --stack-name bastion-host-server --template-body file://bastion-server.yml --parameters file://bastion-server-params.json --capabilities CAPABILITY_IAM`

## Step 3
Run application-servers.yml
`aws cloudformation create-stack --stack-name application-servers --template-body file://application-servers.yml --parameters file://application-servers-params.json --capabilities CAPABILITY_IAM`

