# -*- mode: ruby -*-
# vi: set ft=ruby :

# 1. Скрипт для встановлення Java та ЗАПУСКУ додатка
$install_and_run = <<-'SHELL'
  echo ">>> Updating packages and installing OpenJDK 17..."
  sudo apt-get update
  sudo apt-get install -y openjdk-17-jdk

  echo ">>> Starting the Java application..."
  cd /vagrant
  chmod +x gradlew
  # Запускаємо в фоновому режимі, щоб Vagrant міг завершити процес up
  nohup ./gradlew bootRun > /var/log/app.log 2>&1 &
  
  echo ">>> Application is starting in the background. Check http://192.168.100.100:8080/dogs in a minute."
SHELL

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/jammy64"
  config.vm.network "private_network", ip: "192.168.100.100"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 2
    vb.memory = 4096
    vb.name = "Java_Vagrant_Final"
  end

  # Використовуємо один надійний provisioner для всього
  config.vm.provision "shell", inline: $install_and_run

end