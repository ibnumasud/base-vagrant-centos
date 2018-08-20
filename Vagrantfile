# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "openstackPackstack" do |openstackPackstack|

    openstackPackstack.vm.box = "centos/7"
    openstackPackstack.vm.hostname = "openstackPackstack"
    openstackPackstack.vm.synced_folder '.', '/vagrant', disabled: true
    # openstackPackstack.vm.network :private_network, ip: "192.168.202.201"
    openstackPackstack.vm.network :public_network, ip: "10.14.3.158"

    openstackPackstack.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", 8192]
      vb.customize ["modifyvm", :id, "--cpus", 2]
    end


    # openstackPackstack.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
end
