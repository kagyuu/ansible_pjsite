#-*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  
  config.vm.box = "centos/7"
  config.vm.box_url = "https://app.vagrantup.com/centos/boxes/7"
  config.vm.box_url = "https://app.vagrantup.com/centos/boxes/7"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 2
    vb.memory = 1024
  end

  config.vm.define "redmine" do |server|
    server.vm.hostname = "redmine"
    server.vm.network :forwarded_port, id: "ssh", guest: 22, host: 2223, host_ip: "127.0.0.1"
    server.vm.network :forwarded_port, guest: 80, host: 11080, host_ip: "127.0.0.1"
    server.vm.network :forwarded_port, guest: 443, host: 11443, host_ip: "127.0.0.1"
  end
end
