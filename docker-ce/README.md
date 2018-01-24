# Docker-ce Swarm 17.12

## Clone do projeto

<pre>
$ https://github.com/vandocouto/docker-swarm-17.12.git
</pre>

## Arquivos hosts (Ajuste os IP's)
<pre>
[docker-ce]
master1     ansible_ssh_host=200.98.28.210
manager1    ansible_ssh_host=200.98.0.26
worker1     ansible_ssh_host=200.98.29.86

[swarm-master]
master1

[swarm-manager]
manager1

[swarm-worker]
worker1

[all:children]
docker-ce
swarm-master
swarm-manager
swarm-worker

[all:vars]
ansible_ssh_user=administrator
ansible_ssh_private_key_file=~/Dropbox/chave-aws/terceirotempo.pem
</pre>