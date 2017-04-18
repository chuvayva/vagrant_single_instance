VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1500
  end

  config.vm.hostname = 'web'

  config.vm.network "forwarded_port", guest: 3000, host: 3000

  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.ssh.forward_agent = true

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'play.yml'
  end
end

