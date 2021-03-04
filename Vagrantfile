Vagrant.configure("2") do |config|

  config.vm.define "client" do |client|
#    client.landrush.enabled = true
#    client.vm.hostname="client.vagrant.test"
    client.vm.box = "centos/7"
    client.vm.network "private_network", ip: "172.16.1.200",netmask:"255.240.0.0"
    client.vm.provision :ansible do |ansible|
          #ansible.verbose = "vvvv"
          ansible.playbook= "playbook.yml"
    end
  end

  config.vm.define "dataserver" do |dataserver|
  #  dataserver.landrush.enabled = true
    dataserver.vm.hostname="dataserver.vagrant.test"
    dataserver.vm.box = "centos/7"
    dataserver.vm.network "private_network", ip: "172.16.1.202",netmask:"255.240.0.0"
    dataserver.vm.provision :ansible do |ansible|
          ansible.playbook= "playbook.yml"
          ansible.verbose = "vv"
    end
  end
  
  config.vm.define "redirector" do |redirector|
  #  dataserver.landrush.enabled = true
    redirector.vm.hostname="redirector.vagrant.test"
    redirector.vm.box = "centos/7"
    redirector.vm.network "private_network", ip: "172.16.1.203",netmask:"255.240.0.0"
    redirector.vm.provision :ansible do |ansible|
          ansible.playbook= "playbook.yml"
    end
  end
end
