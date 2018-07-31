# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.ssh.private_key_path = File.expand_path('~/.vagrant.d/insecure_private_key')
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  
  config.vm.define "ansiblenodejs" do |ansiblenodejs|

  ansiblenodejs.vm.box = "centos/7"
  ansiblenodejs.vm.hostname = "ansiblenodejs"
  ansiblenodejs.vm.synced_folder '.', '/vagrant', disabled: true
  ansiblenodejs.vm.network :private_network, ip: "192.168.202.204"
    ansiblenodejs.vm.provision :ansible do |ansible|
      ansible.playbook = "playbook.yml"
      ansible.become = true
    end
  end
end
