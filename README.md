# venus.sshtunnel
Set up a reverse ssh tunnel to a trusted host for GX devices behind NAT / Firewall


## Instructions

On the remote side, add a user
* sudo useradd sshtunnel-username

On the gx / venus side
* create a ssh keypair ssh-keygen -t rsa
* copy the public key from /home/root/.ssh/id_rsa.pub to /home/sshtunnel-username/.ssh/authorized_keys
* (optional) add your public key to /home/root/.ssh/authorized_keys
* test the connection once to accept the public key pair (ssh your-remote-host from the gx)
* checkout this repository
* chmod +x service/run
* copy sshtunnel.conf.template to /etc/sshtunnel.conf and configure
* test to execute service/run
* add ln -sf /data/venus.sshtunnel/service /service/venus.sshtunnel to /data/rc.local
