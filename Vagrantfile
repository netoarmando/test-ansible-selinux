# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "netoarmando/ci-master-f30"
  config.vm.box_version = "0.0.0"

  config.vm.provision :ansible do |ansible|
    ansible.limit = "all"
    ansible.playbook = "provision.yaml"
    ansible.extra_vars = "vars.yaml"
  end

  config.vm.synced_folder "./", "/vagrant", type: "nfs"

end
