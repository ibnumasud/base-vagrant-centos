# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "ansible-app1" do |ansible-app1|

  ansible-app1.vm.box = "centos/7"
  ansible-app1.vm.hostname = "ansible-app1"
  ansible-app1.vm.synced_folder '.', '/vagrant', disabled: true
  ansible-app1.vm.network :private_network, ip: "192.168.202.201"
  # ansible-app1.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
  config.vm.define "ansible-app2" do |ansible-app2|

    ansible-app2.vm.box = "centos/7"
    ansible-app2.vm.hostname = "ansible-app2"
    ansible-app2.vm.synced_folder '.', '/vagrant', disabled: true
    ansible-app2.vm.network :private_network, ip: "192.168.202.202"
    # ansible-app1.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
  config.vm.define "ansible-db" do |ansible-db|

    ansible-db.vm.box = "centos/7"
    ansible-db.vm.hostname = "ansible-db"
    ansible-db.vm.synced_folder '.', '/vagrant', disabled: true
    ansible-db.vm.network :private_network, ip: "192.168.202.203"
    # ansible-app1.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
end
