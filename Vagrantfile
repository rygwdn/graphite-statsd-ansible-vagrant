# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "graphite" do |graphite|
    #graphite.vm.box = <centos 6.5 box name>
    #graphite.vm.box_url = <centos 6.5 box url>

    graphite.vm.network :private_network, ip: "192.168.5.20"

    graphite.vm.provision "ansible" do |ansible| 
      ansible.playbook = "graphite.yml"
    end 
  end

  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", "1024"]
  end

end
