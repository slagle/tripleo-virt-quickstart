# tripleo-virt-quickstart

These steps have been tested on CentOS 7 host.

Setup
-----

If necessary, create a non-root user with sudo access, and become that user:

    useradd -G wheel centos
    passwd centos # Set a password
    su - centos

Further configure the user so that it can ssh as root into the host without a
password prompt.

The rest of the example commands assume using a non-root user with sudo
access.

Ensure the CentOS installation is up to date:

    sudo yum -y update

Install git if needed:

    sudo yum -y install git

Installation
------------

Use any non-root user (e.g., the user created above):

    git clone https://github.com/slagle/tripleo-virt-quickstart.git
    cd tripleo-virt-quickstart
    ./bootstrap.sh

Running
-------
    ./run.sh

Login to undercloud
-------------------

After run.sh, use the following command to login to the running undercloud vm.

    ssh -F ~/.quickstart/ssh.config.ansible undercloud
