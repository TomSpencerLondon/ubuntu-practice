IMAGE_NAME = "bento/ubuntu-20.04"

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false

  config.vm.define "lfs" do |lfs|
    lfs.vm.box = IMAGE_NAME
    lfs.vm.network "private_network", ip: "192.168.56.10"
    lfs.vm.network "forwarded_port", guest: 6443, host: 6443
    lfs.vm.hostname = "lfs"
    lfs.vm.provider "virtualbox" do |v|
      v.name = "lfs"
      v.memory = 3072
      v.cpus = 2
    end
  end

end
