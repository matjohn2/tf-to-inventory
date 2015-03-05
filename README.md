# Terraform to Inventory

This is a small python script that generates an Ansible [inventory](http://docs.ansible.com/intro_inventory.html)  from a [Terraform](https://terraform.io/) state file. You can spin up a bunch of VMs using Terraform and then provision them with Ansible.

## Usage

```bash
# run from the directory where your terraform.tfstate file is located
python tf-to-inventory.py
```

### Openstack 
The script will favour a floating IP for the ansible inventory if it exists. Failing back to regular IPv4 address of the instance.
see hosts.openstack for an example hosts file.

### AWS

AWS Specific usage here.
see hosts.aws for an example hosts file.

## Acknowledgement

Initially inspired by the [zookeeper-ansible-terraform](https://github.com/ianunruh/zookeeper-ansible-terraform) recipe. 
@chourobin adopted much of the code and added support for Amazon EC2 instances.
@matjohn2 forked to add support for Openstack based on the Terraform Openstack provider [PR Here](https://github.com/hashicorp/terraform/pull/924)

## License

MIT
