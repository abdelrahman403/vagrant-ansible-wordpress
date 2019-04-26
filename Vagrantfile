# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure("2") do |config|
  config.vm.box = "centos7_serv"

  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"
  #config.vm.network "public_network", bridge: 'wlp10s0', ip: '192.168.1.14'  
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provider "virtualbox" do |vb|
    vb.name = "wordpress_site"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "wordpress/site.yml"
  end	
  
end
