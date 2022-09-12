# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_API_VERSION = "2"

Vagrant.configure(VAGRANT_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end

  ## Rockylinux/8 instance
  config.vm.define "rocky-8" do |rocky|
    rocky.vm.box = "rockylinux/8"
    rocky.vm.hostname = "rocky-8"
    rocky.vm.network "private_network", ip: "192.168.56.91"
  end
  ## CentOS/8 instance
  config.vm.define "centos-8" do |centos|
    centos.vm.box = "geerlingguy/centos8"
    centos.vm.hostname = "centos-8"
    centos.vm.network "private_network", ip: "192.168.56.92"
  end
  ## Ubuntu/2004 instance
  config.vm.define "ubuntu-2004" do |ubuntu|
    ubuntu.vm.box = "geerlingguy/ubuntu2004"
    ubuntu.vm.hostname = "ubuntu2004"
    ubuntu.vm.network "private_network", ip: "192.168.56.93"
  end
end
