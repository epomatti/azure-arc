# Azure ARC

Managing external resources in Azure with ARC.

## AWS Instances

Set up the config:

```sh
cd aws

cp config/template.tfvars .auto.tfvars
```

Create the resources on AWS:

```sh
terraform init
terraform apply -auto-approve
```

## Azure ARC

https://learn.microsoft.com/en-us/azure/azure-arc/servers/learn/quick-enable-hybrid-vm
