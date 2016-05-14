# README - DevOps

The Python script in this folder is used to deploy a CentOS7 image with 96GB memory and 8 processor cores to an ESXi hypervisor. Packer must be installed on the host machine and SSH access must be enabled on ESXi. Execute 

```
$ python packer-driver.py
```

to start the deployment. User will be prompted to enter the ESXi host address, SSH username/password for ESXi, the ESXi datastore name for primary OS storage (25GB), and an instance name for the virtual machine.