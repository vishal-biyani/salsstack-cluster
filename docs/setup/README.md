## [Go back home](https://github.com/vishal-biyani/saltstack-cluster)

# Setup

The setup uses a simple multi Vagrant box setup to play around with Saltstack. You need working Vagrant on your machine to use this demo. If you don't have Vagrant, you can install Vagrant and Virtualbox from links below:

## Prerequisites

- [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads.html)

* Please note that the Vgarant command need to be run from root directory of this project as Vagrantfile is in root dirrectory *

Before you run Vagrant up - change following parameters in Vagrantfile as per your need/taste. I typically start 1 master and 2/3 node cluster with 2GB for Master and 512MB/1GB for nodes based on what I need to build.

## Configure

```
MASTER_MEMORY=2048
AGENT_MEMORY=512
MASTER_INSTANCES=1
AGENT_INSTANCES=2
```
Also if you face issue with network or getting box up, try changing the subnet in Vagrantfile 

```
SALT_SUBNET="192.168.17"
SALT_MASTER_ADDRESS="192.168.17.99"
```
## Run

Now run ```vagrant up``` which will download the base boxes and then setup the cluster. If you don't have the base boxes, the download can take some time based on connection speed.

Once `vagrant up` runs successfully, you should see one master and multiple agents based on your configuration. With default configuration here is what I see:

```
Current machine states:

salt_master               running (virtualbox)
salt_agent_0              running (virtualbox)
salt_agent_1              running (virtualbox)
```

You can get into any box by using ```vagrant ssh``` command (Works better with Git bash/Cygwin on Windows)

```
vagrant ssh salt_master
vagrant@smaster:~$

```

