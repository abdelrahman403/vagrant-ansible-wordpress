## Wordpress Development Environment With Vagrant & Ansible

Uses Vagrant to provision a virtual machine running on Centos7 for Wordpress development. Complete the installation by navigating to http://127.0.0.1:8080 and finishing the Wordpress wizard.

---

Ansible playbooks for:

- Add epel & webtatic & mariadb repos to the server.
- Add system user & group and install required system packages.
- Install nginx web server.
- Install php7 & php-fpm and some dependencies.
- Install mariadb server & client and secure db.
- Create database and db user.

## Prerequisites

- Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Install [Vagrant](http://www.vagrantup.com/) (tested with 2.1.5)

## Usage:

- Clone this repository to the root of your project directory
  ```bash
  git clone https://github.com/abdelrahman403/vagrant-ansible-wordpress.git
  ```
- Change the variables at `group_vars/all`
- In your project directory, run `vagrant up`

### Port forwarding:

Nginx works on port 80 on the guest is forwarded to port 8080 on the host.
