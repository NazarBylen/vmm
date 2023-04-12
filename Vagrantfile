Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/jammy64"

    config.vm.provider "virtualbox" do |vb|
        vb.memory = 1024
        vb.cpus = 1
    end

    config.vm.define "webserver", primary: true do |webserver|
        webserver.vm.hostname = "webserver"
        webserver.vm.network :private_network, ip: "192.168.56.10"
        webserver.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
            ansible.inventory_path = "inventory.ini"
            ansible.groups = {
                "web" => ["webserver"]
            }
        end
    end

    config.vm.define "databases" do |databases|
        databases.vm.hostname = "databases"
        databases.vm.network :private_network, ip: "192.168.56.11"
        databases.vm.provision "ansible" do |ansible|
            ansible.playbook = "./playbook.yml"
            ansible.inventory_path = "inventory.ini"
            ansible.groups = {
                "db" => ["databases"]
            }
        end
    end

end