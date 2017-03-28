VAGRANTFILE_API_VERSION = "2"
PROJECT = 'teamvillage'
PROJECT_PATH = "/Users/BiT/Documents/Dev/Web/#{PROJECT}"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1500
  end

  config.vm.hostname = 'web'

  #config.vm.network "private_network", ip: "192.168.0.2"
  config.vm.network "forwarded_port", guest: 3000, host: 3000

  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.synced_folder PROJECT_PATH, "/vagrant/#{PROJECT}"

  config.ssh.forward_agent = true

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'play.yml'
  end
end

