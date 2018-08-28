Vagrant.configure("2") do |config|
  config.vm.define "node1" do |node1|
    node1.vm.box = "centos/7"
    node1.vm.hostname = 'work-node1'
    node1.vm.network :public_network, ip: "172.16.202.96"
    node1.vm.network "forwarded_port", guest: 80, host: 28080

    node1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 1500]
      v.customize ["modifyvm", :id, "--name", "node1"]
    end
  end

 
  config.vm.define "node2" do |node2|
    node2.vm.box = "centos/7"
    node2.vm.hostname = 'work-node2'

    node2.vm.network :public_network, ip: "172.16.202.97"

    node2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 1500]
      v.customize ["modifyvm", :id, "--name", "node2"]
    end
  end
end
