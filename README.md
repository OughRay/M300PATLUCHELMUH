# Dokumentation vom Team PATLUCHELMUH über das Modul 300 Plattformübergreifende Service

# Inhaltsverzeichnis
* Team
* Umgebung auf der TBZ Cloud
  * VPN einrichten
* Vagrant Erklärung
  * Funktionsweise & Konzepte
  * Unsere Vagrant files
  * Erklärung vom Vagrant file
* Testing
  * Testfälle
  * Testergebnisse
* Fazit
* Reflexion
* Wissensgewinn


# Team Übersicht
  * Luca Miani 
  * Patrick Schwab 
  * XX 
  * XX

# Umbebung auf TBZ Cloud einrichten und Zugriff erhalten 
Auf jedem Client muss das VPN WireGuard installiert und konfiguriert werden.

Ist die VM zugreifbar können in einem zweiten Schritt die Services, z.B. ein Web Server, mittels Portweiterleitung im Internet zur Verfügung gestellt werden.

## VPN einrichten
Das konventionelle VPN bezeichnet ein virtuelles privates (in sich geschlossenes) Kommunikationsnetz. Virtuell in dem Sinne, dass es sich nicht um eine eigene physische Verbindung handelt, sondern um ein bestehendes Kommunikationsnetz, das als Transportmedium verwendet wird. Das VPN dient dazu, Teilnehmer des bestehenden Kommunikationsnetzes an ein anderes Netz zu binden.

Installieren von [WireGuard](https://www.wireguard.com/install/) auf dem Client, dass kann ein Notebook, Raspberry Pi o.ä. sein.

In den Unterlagen zum Modul/Kurs finden Sie eine Vorlagen, z.B. wg1-template.conf und eine Liste von IP-Adressen der Server und Ihren Key und IP-Adresse für das VPN Netzwerk.

Vervollständigen Sie die Vorlage und ersetzen dabei die Einträge <replace IP> und <replace Key> durch Ihre Werte laut Liste.

Die Konfigurationsdatei sieht in etwa so aus:

```[Interface]
Address = <replace IP>/24
PrivateKey = <replace Key>

[Peer]
PublicKey = xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Endpoint  = yyyyyyyyyyyyyyyyyy:518zz

AllowedIPs = 192.168.xx.0/24

# This is for if you're behind a NAT and
# want the connection to be kept alive.
# PersistentKeepalive = 25
```
Handelt es sich beim Client z.B. um einen Raspberry Pi, welcher für andere im VPN sichtbar sein soll, aktivieren Sie den Eintrag `PersistentKeepalive` bzw. kommentieren diesen aus.

**Vorsicht:** Dadurch ist die IP-Adresse und alle Ports für alle im VPN sichtbar. Sollte in Unternehmensnetzwerken nur nach Rücksprache mit dem Sicherheitsverantwortlichen aktiviert werden.

Starten Sie die WireGuard Software und fügen die ergänzte Vorlage WireGuard als Tunnel hinzu:

![](images/wireguard-add.png)

Und aktivieren Sie den Tunnel:

![](images/wireguard-activate.png)

Die VMs sind nun mittels IP-Adresse inkl. allen Ports im VPN sichtbar. Zugriff auf VM mittels ssh ubuntu@X.X.X.X

# Vagrant Erklärung

Vagrant ist eine Ruby-Anwendung (open-source) zum Erstellen und Verwalten von virtuellen Maschinen (VMs).

Die Ruby-Anwendung dient als Wrapper (engl. Verpackung, Umschlag) zwischen Virtualisierungssoftware wie VirtualBox, VMware und Hyper-V und Software-Konfiguration-Management-Anwendungen bzw. Systemkonfigurationswerkzeugen wie Chef, Saltstack und Puppet.

**Wichtig:** Die Virtuellen Maschinen entsprechen lauffähigen Servern.

## Funktionsweise & Konzepte

**CLI**
Vagrant wird über die Kommandozeile (CLI) bedient.

Die wichtigsten Befehle sind:

|Befehl  |Beschreibung
|--------|----------
|vagrant init|	Initialisiert im aktuellen Verzeichnis eine Vagrant-Umgebung und erstellt, falls nicht vorhanden, ein Vagrantfile
|vagrant up|	Erzeugt und Konfiguriert eine neue Virtuelle Maschine, basierend auf dem Vagrantfile                               
|vagrant ssh|	Baut eine SSH-Verbindung zur gewünschten VM auf                                                                   
|vagrant status|	Zeigt den aktuellen Status der VM an                                                                           
|vagrant port|	Zeigt die Weitergeleiteten Ports der VM an                                                                     
|vagrant halt|	Stoppt die laufende Virtuelle Maschine
|vagrant destroy|	Stoppt die Virtuelle Maschine und zerstört sie.

Weitere Befehle sind unter: [Vagrant.com](https://www.vagrantup.com/docs/cli/)

## Unsere Vagrant files

Bis jetzt haben wir das 

``` 
vagrant init ubuntu/trusty64
sudo apt-get update
sudo apt install apache2
vagrant up
```

## Erklärung vom Vagrant file

Initialisiert im aktuellen Verzeichnis eine Vagrant-Umgebung und erstellt, falls nicht vorhanden, ein Vagrantfile.
```
vagrant init ubuntu/trusty64
```

Die Ubuntu VM laded die neusten Updates runter und installiert diese.
```
sudo apt-get update
```

Der neuste Apache2 Dienst wird runtergeladen und installiert. 
```
sudo apt install apache2
```

Erzeugt und Konfiguriert eine neue Virtuelle Maschine, basierend auf dem Vagrantfile.
```
vagrant up
```
# Testing

## Testfälle

## Testergebnisse

# Fazit

# Reflexion

# Wissensgewinn

