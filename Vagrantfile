VAGRANTFILE_API_VERSION = "2"

Vagrant.require_version ">= 1.6.5"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "puphpet/ubuntu1404-x64"
  config.vm.box_check_update = true

  config.vm.network :private_network, ip: "192.168.55.110"

  config.vm.synced_folder "../", "/home/vagrant/projects"

  config.vm.provider "virtualbox" do |vm|
    vm.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vm.customize ["modifyvm", :id, "--cpus", 2]
    vm.customize ["modifyvm", :id, "--memory", 2048]
  end

  config.vm.provider "vmware_fusion" do |vm|
    vm.memory = 2048
    vm.cpus = 2
  end

  config.vm.provision "shell", path: "provision.sh", privileged: false
end
