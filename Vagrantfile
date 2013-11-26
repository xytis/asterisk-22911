# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"

  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.network :public_network, ip: "192.168.1.211"

  config.vm.provider :virtualbox do |vb|
    # Don't boot with headless mode
    #vb.gui = true
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
  end

  config.vm.synced_folder "config", "/etc/asterisk"

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provisioning/vagrant.yml"
    ansible.extra_vars = { data_dir: "/vagrant" }
  end
end
