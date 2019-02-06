ansible-ocserv
--------------

### Introduction ###

`docker-ocserv` is an OpenConnect VPN Server boxed in a Docker image built by <a href="https://github.com/TommyLau/docker-ocserv" target="_blank">**Tommy Lau**</a>. I am inspired by it and created `ansible-ocserv` project. This project made of Ansible playbook to fast and automation deployment of OpenConnect VPN server and create a user.


### Dependency ###
To use `ansible-ocserv` project you have need some packages for deploying it,  which one of them is ansible. If you using CentOS you should run below command in your Ansible machine :

```
yum install ansible
```

In your OpenConnect VPN Server/s, you have need few packages. In CentOS Linux distribution you should run below command :

```
yum install epel-release docker python-docker-py openssl
```

### Deploy ###
To deploy `docker-ocserv` project, after clone the project in your Ansible machine, enter your OpenConnect VPN server/s IP address in hosts file:

```
vi hosts
```

After that set information of your environment in variable file:

```
vi group_vars/all
```

Now for run Ansible Playbook you should run the beneath command:

```
ansible-playbook -i hosts main-playbook.yml
```

When Ansible Playbook run successfully completely, you can make OpenConnect client in your system and connect to OpenConnect VPN Server and enjoy it.


## Contact

Hossein Aghaie [@hos7ein](http://twitter.com/hos7ein)


## License

ansible-ocserv source code is available under the GPL-3.0 [License](/LICENSE).
