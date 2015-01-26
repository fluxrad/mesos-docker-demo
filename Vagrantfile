# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "mesos1" do |mesos1|
      mesos1.vm.box = "ubuntu/trusty64"
      mesos1.vm.network "private_network", ip: "192.168.33.10"
      mesos1.vm.synced_folder "docker", "/srv/docker"
  end

  config.vm.define "mesos2" do |mesos2|
      mesos2.vm.box = "ubuntu/trusty64"
      mesos2.vm.network "private_network", ip: "192.168.33.11"
      mesos2.vm.synced_folder "docker", "/srv/docker"
  end

  config.vm.define "mesos3" do |mesos3|
      mesos3.vm.box = "ubuntu/trusty64"
      mesos3.vm.network "private_network", ip: "192.168.33.12"
      mesos3.vm.synced_folder "docker", "/srv/docker"
  end

  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/playbook.yml"
  end

end
