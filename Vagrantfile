Vagrant.configure(2) do |config|
  config.vm.box = "yfix/trusty64"
  config.vm.network :private_network, ip: "192.168.33.133"
  config.ssh.insert_key = false
  config.vm.provider :virtualbox do |v|
    v.name = "yfix-trusty64.dev"
    v.memory = 512
    v.cpus = 2
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--ioapic", "on"]
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/main.yml"
  end
end