VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false

  config.vm.define "mysql-master" do |server|
    server.vm.box = "bento/centos-6.7"
    server.vm.hostname = "mysql-master"
    server.vm.network "private_network", ip: "192.168.50.4"
    server.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
    end
  end

  config.vm.define "mysql-slave" do |server|
    server.vm.box = "bento/centos-6.7"
    server.vm.hostname = "mysql-slave"
    server.vm.network "private_network", ip: "192.168.50.3"
    server.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 1
    end
  end

end
