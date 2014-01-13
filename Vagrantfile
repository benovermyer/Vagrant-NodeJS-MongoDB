Vagrant.configure("2") do |config|
  config.vm.box = "saucy64"
  config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/saucy/current/saucy-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.hostname = "nodejsdev.local"
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end
  config.vm.network :forwarded_port, guest: 80, host: 8888

  config.vm.provision "shell", path: "provision.sh"
end