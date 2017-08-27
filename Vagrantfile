# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.box = 'ubuntu/xenial64'
  config.vm.box_check_update = false
  config.vm.network 'forwarded_port', guest: 3838, host: 3838, id: 'shinyserver', host_ip: '127.0.0.1', auto_correct: true
  config.vm.provider 'virtualbox' do |vb|
    vb.memory = '1024'
    vb.name = 'shiny-server'
  end
  config.vm.provision 'shell', path: 'provision.sh'
end
