Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-6.9"

  config.vm.network "private_network", type: "dhcp"
  config.vm.network "forwarded_port", guest: 80, host: 8081

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
