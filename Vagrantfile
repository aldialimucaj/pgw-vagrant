VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
 
  config.vm.box = "ubuntu/trusty64"

  config.push.define "atlas" do |push|
    push.app = "alimucaj/playground"
  end
  
  config.vm.hostname = hostname = "playground"
  config.vm.network "public_network"
  
  # Configure Virtualbox settings
  config.vm.provider :virtualbox do |vb|
    vb.name = hostname
    vb.customize ["modifyvm", :id, "--memory", "1024"]
    vb.customize ["modifyvm", :id, "--ioapic", "on"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
    vb.customize ["modifyvm", :id, "--ostype", "Ubuntu_64"]
  end

end
