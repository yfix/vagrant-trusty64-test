Vagrant.configure(2) do |config|
  config.vm.box = "yfix/trusty64"
  config.vm.network :private_network, ip: "192.168.33.133"
  config.vm.network "forwarded_port", guest: 80, host: 13380
  config.vm.network "forwarded_port", guest: 22, host: 13322
  config.ssh.insert_key = false
  config.ssh.forward_agent = true
  config.vm.hostname = "yfix-trusty64.dev"
  config.vm.provider :virtualbox do |v|
    v.name = "yfix-trusty64.dev"
    v.memory = 512
    v.cpus = 2
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--ioapic", "on"]
  end
  config.vm.synced_folder "synced/", "/synced", type: "nfs"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/main.yml"
  end
end
