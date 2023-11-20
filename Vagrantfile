# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Configuration de la machine virtuelle
  config.vm.box = "debian/buster64"

  # Activer l'interface graphique
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "1024"
  end

  # Configuration du réseau
  # config.vm.network "private_network", type: "dhcp"

  # Configuration du provisionneur Ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbooks/setup.yml"
    ansible.inventory_path = "hosts"
    ansible.limit = "all"
    ansible.verbose = "v"
    ansible.extra_vars = {
      ansible_user_id: "vagrant"
    }
  end

  # Configuration SSH (optionnel)
  config.ssh.insert_key = false
end
