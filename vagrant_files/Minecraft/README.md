# Erklärung zum Vagrant file Minecraft

Mitels dem Vagrantfile und dem minecraft_bootstrap kann ein Minecraft Server in unter 5 Minuten erstellt werden.

### Was benötigt wird: 
  * Eine Maschiene mit Vagrant 
  * unser Vagrantfile und unser minecraft_bootstrap file
  * Auf der Hauptmaschine den Port 25565 in der Firewall freigeben 
  
## Die Konfiguration

Als erstes muss man deklarieren das die verschiedene Konfigurationen namens config durchgeführt werden sollen.
```
Vagrant.configure("2") do |config|
```

Diese Zeile beschreibt welches OS installiert werden soll und welche Bit verion genutz werden soll, also Ubuntu 16.04 mit der 64 Bit version.
```
config.vm.box = "ubuntu/xenial64"
```

Nun werden die Konfigurationen namens vb gemacht.
```
config.vm.provider "virtualbox" do |vb|
```

Hier wird deklariert wie viel RAM/ Arbeitsspeicher die VM benutzen soll, bei uns sind das 2 Gigabyte. 
```
vb.memory="2048"
```

Nun wird der Port 25565 in der Firewall geöffnet.
```
config.vm.network "forwarded_port", guest: 25565, host: 25565, protocol: "tcp"
```

Hier wird dem Vagrantfile der Ort des Shell/ Bash Script files gezeigt, diese shell Befehle können auch in dem Vagrant file hinterlegt werden, doch da wir es etwas schöner haben wollten haben wir ein extra file dafür erstellt.
```
config.vm.provision :shell, :path => "minecraft_bootstrap"
```

Und zum Schluss wird es noch beendet.
```
  end
end
```

## Shell file






#!/bin/bash
sudo apt update -y
sudo apt install openjdk-8-jre-headless -y
ufw allow 25565
WORK_DIR='/home/vagrant/minecraft' 
mkdir ${WORK_DIR}
cd ${WORK_DIR}
wget https://launcher.mojang.com/v1/objects/c5f6fb23c3876461d46ec380421e42b289789530/server.jar
touch ${WORK_DIR}/eula.txt
cat > ${WORK_DIR}/eula.txt <<EULA
# By changing the setting below to TRUE you are indicating your agreement to our EULA (https://account.mojang.com/documents/minecraft_eula).
eula=TRUE
EULA
touch ${WORK_DIR}/start.sh
cat > ${WORK_DIR}/start.sh <<START
screen -dmS minecraft java -Xms1024M -Xmx1024M -jar server.jar nogui
START
chmod +x ${WORK_DIR}/start.sh
echo "Your Minecraft Server is online please use IP __10.1.31.8:25565__"
sh ${WORK_DIR}/start.sh
