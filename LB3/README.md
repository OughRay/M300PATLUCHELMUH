# LB3 Dokumentation vom Team PATLUCHELMUH

# Einleitung
In diesem Dokument beschreiben wir die Arbeit von der LB3.

# Inhaltsverzeichnis
* Was ist Docker?
    * Docker Befehle
* Was ist Kubernetes
* Umgebung
* Netzwerkplan für Nextcloud
* Unsere Docker Projekte
* Testfälle Apache 2
* Testfälle Mail2
* Testfälle Nextcloud


# Was ist Docker?
Docker ist eine Freie Software zur Isolierung von Anwendungen mit Hilfe von Containervirtualisierung. Docker vereinfacht die Bereitstellung von Anwendungen, weil sich Container, die alle nötigen Pakete enthalten, leicht als Dateien transportieren und installieren lassen.

## Docker Befehle
|Befehl  |Beschreibung
|--------|----------
|docker attach|	Attach local standard input, output, and error streams to a running container
|docker build|	Build an image from a Dockerfile                               
|docker builder|	Manage builds                                                                   
|docker commit|	Create a new image from a container’s changes                                                                         
|docker config|	Manage Docker configs                                                                    
|docker create|	Create a new container
|docker images|	List images
|docker info| Display system-wide information
|docker import|Import the contents from a tarball to create a filesystem image
|docker kill|Kill one or more running containers
|docker network|Manage networks
|docker pause|Pause all processes within one or more containers
|docker ps|List containers
|docker pull|Pull an image or a repository from a registry
|docker rename|Rename a container
|docker restart|docker restart
|docker stop|Stop one or more running containers
|docker start|Start one or more stopped containers

# Was ist Kubernets
Kubernetes ist ein Open-Source-System zur Automatisierung der Bereitstellung, Skalierung und Verwaltung von Container-Anwendungen, das ursprünglich von Google entworfen und an die Cloud Native Computing Foundation gespendet wurde. Es zielt darauf ab, eine Plattform für das automatisierte Bespielen, Skalieren und Warten von Anwendungscontainern auf verteilten Hosts zu liefern. Es unterstützt eine Reihe von Container-Tools, einschliesslich Docker.

# K1
Für unsere Umgebung benutzen wir ProxMox VE das auf einem Server bei Luca zu Hause installiert ist. So können wir direkt Container erstellen und haben keine Einschränkungen an Leistung.
## VirtualBox
Musste nicht installiert werden, da wir ProxMox benutzen
## Vagrant
War schon aus der vorherigen LB2 installiert
## Visualstudio-Code
Wurde auf den Clients unseres Teams installiert
## Git-Client
Wurde auf den Clients unseres Teams installiert
## SSH-Key für Client erstellt
1.	SSH Key erstellen
•	Key wird erstellt
 
•	Namen des Files ermitteln
 
•	Den Inhalt über Cat aufrufen und den Key Kopieren
 
2.	SSH key auf Github hinzufügen
•	Unter SSH keys den kopierten Code einfügen.


### Testfall für Apache 2 

| Die zu testende Aktion                                     | Erwartete Ausgabe/Aktion                                      | Tatsächliche Ausgabe/Aktion                     | 
| -----------------------                                    | -------------------------                                     |----------------------------                     |
| Im Browser auf 10.0.0.16 verbinden                         | Apache2 Default Page öffnet sich                  | Apache2 Default Page erscheint     |
| Docker file ausführen                     | Docker Container wird erstellt                        |Docker Container wurde erfolgreich erstellt          |
| In den Container verbinden             | verbindung mit dem Container wird erstellt              |verbindung mit dem Container wurde erfolgreich erstellt |


### Testfall für Nextcloud 

| Die zu testende Aktion                                     | Erwartete Ausgabe/Aktion                                      | Tatsächliche Ausgabe/Aktion                     | 
| -----------------------                                    | -------------------------                                     |----------------------------                     |
|
