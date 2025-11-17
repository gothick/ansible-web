# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    # Base VM OS configuration.
    config.vm.box = "bento/ubuntu-24.04"
    config.ssh.insert_key = false
    config.vm.synced_folder '.', '/vagrant', disabled: true

    # General VirtualBox VM configuration.
    config.vm.provider :virtualbox do |v|
      v.gui = false
      v.memory = 4096
      v.cpus = 2
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--ioapic", "on"]
    end

    # Varnish.
    config.vm.define "vagrant-web" do |machine|
      machine.vm.hostname = "vagrant-web.test"
      machine.vm.network :private_network, ip: "192.168.56.2"
      machine.vm.network "forwarded_port", guest: 80, host: 8181 # Because Jenkins is on 8080
      machine.vm.network "forwarded_port", guest: 443, host: 4443
      machine.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yml"
        ansible.inventory_path = "inventories/vagrant.yml"
        ansible.limit = "all"
        ansible.extra_vars = {
          ansible_user: 'vagrant',
          is_vagrant: true,
          ansible_ssh_private_key_file: "~/.vagrant.d/insecure_private_key"
        }
      end

    end
  end
