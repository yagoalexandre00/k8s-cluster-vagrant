Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "public_network"
  config.vm.provision "shell", inline: <<-SCRIPT
    sudo apt update && sudo apt upgrade -y
  SCRIPT

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end

  config.vm.define "master" do |master|
    master.vm.hostname = "master"
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.hostname = "worker-1"
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.hostname = "worker-2"
  end
end
