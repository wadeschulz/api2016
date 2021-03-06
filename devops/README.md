# README - DevOps

# 01-deploy

The Python script in this folder is used to deploy a CentOS7 image with 96GB memory and 8 processor cores to an ESXi hypervisor. Packer must be installed on the host machine and SSH access must be enabled on ESXi. Execute 

```
$ python packer-driver.py

ESXI server address: <HOSTNAME OR IP>
ESXI SSH username: <SSH USERNAME>
ESXI SSH password: <PASSWORD>
Datastore name: <DATASTORE NAME FOR OS STORAGE DEVICE>
VM/Build name: <VM INSTANCE NAME>
```

to start the deployment. User will be prompted to enter the ESXi host address, SSH username/password for ESXi, the ESXi datastore name for primary OS storage (25GB), and an instance name for the virtual machine. Additional configuration options to adjust memory, CPU, storage, and OS-level configuration can be found in the centos7/packer-config.json and centos7/ks.cfg files.

# Drive Configuration

Prior to deploying Docker with the Ansible scripts below, two drives should be created:
* 50GB drive configured as a logical volume with a thinpool for Docker storage
* 500GB (or other appropriate size for data) configured as an ext4 volume

# 02-config

```
$ ansible-playbook -i hosts -k site.yml

SSH password:
SUDO password[defaults to SSH password]:
Enter a password for root:
confirm Enter a password for root:
Enter a password for the deploy user:
confirm Enter a password for the deploy user:
```