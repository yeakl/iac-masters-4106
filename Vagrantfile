Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"

  ENV['VAGRANT_SERVER_URL'] = 'https://vagrant.elab.pro'
  # Количество требуемых машин
  SERVERS = 3
  # Имя сетевого интерфейса для организации моста
  BRIDGE = "en0: Wi-Fi (Wireless)"

  def create_host(config, hostname, ip)
    config.vm.define hostname do |host|
      host.vm.network "private_network", ip: ip
      host.vm.network "public_network", bridge: BRIDGE
      host.vm.hostname = hostname
      host.vm.provision "shell", inline: "apt-get update && apt-get install -y python2-minimal"
      yield host if block_given?
    end
  end

  (1..SERVERS).each do |machine_id|
    create_host(config, "srv#{machine_id}", "192.168.56.#{200+machine_id}")
  end

end
