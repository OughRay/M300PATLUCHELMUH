# Erklärung zum Vagrant file Apache2

## Konfiguration

Das die verschiedene Konfigurationen funktionieren muss die folgene Zeile geschrieben werden, diese hat den namen config.
```
Vagrant.configure(2) do |config|

```

Diese Zeile beschreibt welches OS installiert werden soll und welche Bit verion genutz werden soll, also Ubuntu 16.04 mit der 64 Bit version.  
```
config.vm.box = "ubuntu/xenial64"
```

Nun müssen wir die Ports frei schalten, hier werden die Ports 80 und 8080 freigeschalten. 
```
config.vm.network "forwarded_port", guest:80, host:8080, auto_correct: true
```

Nun werden die Ordner /var/www/html gesynct
```
config.vm.synced_folder ".", "/var/www/html"
```

Wir haben noch eine andere Konfiguration namens vb
```
config.vm.provider "virtualbox" do |vb|
```

Diese Zeile macht die Konfiguration von vb also wie viel RAM/ Arbeitsspeicher die VM benutzen soll, in unserem Fall sind das 512 Megabyte.
```
vb.memory = "512"
```

Nun wird die Konfiguration beendet.
```
end
```

## Shell

Im Vagrant file können noch Shell Befehle hinterlegt werden, das dies funktioniert muss die folgende Zeile geschrieben werden.
```
config.vm.provision "shell", inline: <<-SHELL
```

Dies sind Komentare.
```
# Packages vom lokalen Server holen
# sudo sed -i -e"1i deb {{config.server}}/apt-mirror/mirror/archive.ubuntu.com/ubuntu xenial main restricted" /etc/apt/sources.list
```

Nun wird die Ubuntu das neueste Update herunterladen und installieren.
```
sudo apt-get update
```

Hier wird Apache2 heruntergeladen und grad installiert und mit einem Y die installation bestätigen.
```
sudo apt-get -y install apache2
```

Zuletzt wird die Shell Befehle beendet.
```
SHELL
end
```

  
  
