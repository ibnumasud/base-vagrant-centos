# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "openstack-packstack" do |openstack-packstack|

    openstack-packstack.vm.box = "centos/7"
    openstack-packstack.vm.hostname = "openstack-packstack"
    openstack-packstack.vm.synced_folder '.', '/vagrant', disabled: true
    openstack-packstack.vm.network :private_network, ip: "192.168.202.201"
    # openstack-packstack.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
end
