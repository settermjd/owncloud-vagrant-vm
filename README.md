# ownCloud Vagrant Virtual Machine

This is a simple Vagrant virtual machine (VM) provisioned by Ansible for building ownCloud.

It was built using:

- VirtualBox 5.1.18
- Vagrant 1.9.4
- Ansible 2.3.0.0 (with Python 2.7.13)

The intent is that you can quickly build ownCloud, based on [the official build instructions](https://doc.owncloud.org/server/latest/admin_manual/installation/source_installation.html#apache-configuration-label).
I built it as a way of proofing those instructions.

I’m planning to make it more configurable as time goes on.
But for now, it is what it is.

## Installation

Clone the repository to your local filesystem, cd to the directory, and run `vagrant up`.
For example:

```console
git clone git@github.com:settermjd/owncloud-vagrant-vm.git
cd owncloud-vagrant-vm
vagrant up
```

That will begin the provisioning process.
It should end with the virtual machine being fully provisioned and ready to use.

After it’s provisioned, add the address of the VM to your local DNS configuration, such as by adding it to `/etc/hosts`.
Then, you can access the ownCloud installation from `http://<ip address of the vm>`.
