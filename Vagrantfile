# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.ssh.private_key_path = File.expand_path('~/.vagrant.d/insecure_private_key')
  config.ssh.insert_key = false

  
  config.vm.define "ansibleapp1" do |ansibleapp1|

  ansibleapp1.vm.box = "centos/7"
  ansibleapp1.vm.hostname = "ansibleapp1"
  ansibleapp1.vm.synced_folder '.', '/vagrant', disabled: true
  ansibleapp1.vm.network :private_network, ip: "192.168.202.201"
  # ansibleapp1.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
  config.vm.define "ansibleapp2" do |ansibleapp2|

    ansibleapp2.vm.box = "centos/7"
    ansibleapp2.vm.hostname = "ansibleapp2"
    ansibleapp2.vm.synced_folder '.', '/vagrant', disabled: true
    ansibleapp2.vm.network :private_network, ip: "192.168.202.202"
    # ansibleapp1.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
  config.vm.define "ansibledb" do |ansibledb|

    ansibledb.vm.box = "centos/7"
    ansibledb.vm.hostname = "ansibledb"
    ansibledb.vm.synced_folder '.', '/vagrant', disabled: true
    ansibledb.vm.network :private_network, ip: "192.168.202.203"
    # ansibleapp1.vm.provision :shell, path: "provision.sh", keep_color: "true"
  end
end
