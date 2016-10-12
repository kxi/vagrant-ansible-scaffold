VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.define "cms-dc1" do |server|
    server.vm.box = "centos/6"
    server.ssh.forward_agent = true
    server.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end
    server.vm.network "private_network", ip: "192.168.50.5"
  end
  config.ssh.insert_key = false
  config.vm.define "cms-dc2" do |server|
    server.vm.box = "centos/6"
    server.ssh.forward_agent = true
    server.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end
    server.vm.network "private_network", ip: "192.168.50.6"
  end
end
