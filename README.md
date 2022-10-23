# ansible-ocserv

## Introduction

`docker-ocserv` is an OpenConnect VPN Server boxed in a Docker image built by [Tommy Lau](https://github.com/TommyLau/docker-ocserv). I am inspired by it and created `ansible-ocserv` project. This project made of Ansible playbook to fast and automation deployment of OpenConnect VPN server and create a user.

## Dependency

To use `ansible-ocserv` project you need to have some packages for deploying it, in your Ansible machine you need this package:

* ansible

In OpenConnect VPN Server/s, you will need some of the packages listed below.

* docker
* docker-py
* openssl

For example, in Linux CentOS distribution you should run below command:

```bash
sudo yum install epel-release docker python-docker-py openssl
```

## Deploy

To deploy `docker-ocserv` project, after clone the project in your Ansible machine, enter your OpenConnect VPN server/s IP address in hosts file:

```bash
vi hosts
```

After that set information of your environment in variable file:

```bash
vi group_vars/all
```

Now for running Ansible Playbook you should run the beneath command:

```bash
ansible-playbook -i hosts main-playbook.yml
```

When Ansible Playbook run successfully completely, you can make OpenConnect client in your system and connect to OpenConnect VPN Server and enjoy it.

## Contact

[Project website: "https://github.com/hos7ein/ansible-ocserv"]

[Personal website: "https://fedorafans.com"]

**Author**: Hossein Aghaie <hossein.a97@gmail.com>

**Twitter**: Hossein Aghaie [@hos7ein](https://twitter.com/hos7ein)

## License

`ansible-ocserv` source code is available under the GPL-3.0 [License](/LICENSE).
