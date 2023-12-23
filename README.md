# Azure Arc

Managing external resources in Azure with Arc.

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

## Azure Arc

Make sure you check all the [prerequisites][1].

As of the time of this writing, [Arm64][3] are not supported:

> The Azure Connected Machine agent does not run on x86 (32-bit) or ARM-based architectures.

Set up the base Azure resources:

```sh
terraform init
terraform apply -auto-approve
```

Now [register][2] the Arc servers using the Portal.


[1]: https://learn.microsoft.com/en-us/azure/azure-arc/servers/learn/quick-enable-hybrid-vm#prerequisites
[2]: https://learn.microsoft.com/en-us/azure/azure-arc/servers/learn/quick-enable-hybrid-vm
[3]: https://learn.microsoft.com/en-us/azure/azure-arc/servers/prerequisites#supported-operating-systems
