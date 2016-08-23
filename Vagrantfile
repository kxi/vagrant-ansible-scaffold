VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.define "test-server" do |server|
    server.vm.box = "bento/centos-6.7"
    server.ssh.forward_agent = true
    server.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end
    server.vm.network "private_network", ip: "192.168.50.5"
  end
end
