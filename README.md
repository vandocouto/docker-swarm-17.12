# Docker-ce Swarm 17.12
![alt text](imgs/swarm.png#center "Login")

## Clone do projeto

<pre>
$ https://github.com/vandocouto/docker-swarm-17.12.git
</pre>

## Arquivos hosts (Ajuste os IP's)
<pre>
[docker-ce]
master1     ansible_ssh_host=10.0.100
master2     ansible_ssh_host=10.0.100
master3     ansible_ssh_host=10.0.100

worker1     ansible_ssh_host=10.0.110
worker2     ansible_ssh_host=10.0.111
worker3     ansible_ssh_host=10.0.112

[swarm-master]
master1

[swarm-manager]
master2
master3

[swarm-worker]
worker1
worker2
worker3

[all:children]
docker-ce
swarm-master
swarm-manager
swarm-worker

[all:vars]
ansible_ssh_user=ubuntu
ansible_ssh_private_key_file=~/Dropbox/chave-aws/key.pem
</pre>
