# venus.sshtunnel
Set up a reverse ssh tunnel to a trusted host for GX devices behind NAT / Firewall


## Instructions

On the remote side, add a user
* sudo useradd sshtunnel-username

On the gx / venus side
* create a ssh keypair ssh-keygen -t rsa
* copy the public key to /home/sshtunnel-username/.ssh/authorized_keys
