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
# K2
## GitHub oder Gitlab-Account ist erstellt
## Github Accounts wurde von allen 3 Gruppenmitglieder erstellt. Unsere Benutzernamen sind folgende
•	Luca Miani - @oughray
•	Patrick Schwab - @psychodellic
•	Helmina Jusufi - @helminajusufi
•	Muhammed Ercan - @Muhammedercan
## Git-Client wurde verwendet
1.	SSH key-Link in die Konsole einfügen
•	In der Konsole den den git clone befehl ausführen.
 
•	Mit den richtigen logindaten anmelden.
 
•	(In der VM Console) Unter Source Controll das Repository Stagen und hinzufügen
## Persönlicher Wissenstand im Bezug auf die wichtigsten Themen ist dokumentiert (Containerisierung / Docker, Microservices)
### Luca Miani
Ich arbeite ab und zu im Geschäft mit Linux. Ausserdem habe ich Zuhause mehrere Linux Server. Daher behaupte ich, dass ich sicherlich Kenntnisse habe mit Linux. Einen eigenen Github Acount hatte ich schon vor diesem Modul. Jedoch hatte ich am Anfang dieses Moduls auch keine Erfahrungen mit Vagrant. Dies lernte ich jedoch im Laufe dieses Projektes kennen. Dazu lies ich verschiedene Beiträge und machte mich schlau auf Github. Ausserdem konnte ich bei Fragen immer wieder mein Team fragen, welches mir auch weiterhilf. Das Arbeiten auf der TBZ Cloud fand ich sehr angenehm. Ich konnte ausserdem einiges lernen im Bereich Systemsicherheit. In das Thema SSH habe ich mich ein wenig vertieft und konnte somit auch dies so im Projekt einsetzen.
### Muhammed Ercan
Im Geschäft arbeite ich mehrheitlich mit Macs. Weil Mac OS und Linux sehr ähnlich sind, hatte ich schon einige Erfahrungen mit Linux. Ausserdem habe ich mehrere Server mit Linux aufgesetzt und diese betrieben. Des weiteren habe ich noch einige Services drauf lauffen lassen. Jedoch hatte ich noch vor dem Modul keinen Github Account. Daher schaute ich am Anfang einige Blogs zu Github. Daher kamen mit der Zeit Kentnisse auch über Mark Down und Github. Ich habe zusammen mit Helmina Jusufi im Modul Systemsicherheit gearbeitet. Daher hatten wir von diesem Modul auch Erfahrungen mit der Sicherheit eines Systems. Zu den verschiedenen Vagrant Files habe ich nicht viel gewusst, daher konnte ich auch einiges zu den Vagrant-Files dazulernen. Ausserdem hat mir das Arbeiten auf TBZ Cloud gefallen.
### Patrick Schwab
Mit den Themen Linux hatte ich schon zuvor zutuhn, doch mit Github oder ähnliche Systeme hatte ich zuvor noch nie gearbeitet. Ich habe privat schon mit Linux gearbeitet. Jedoch muss ich sagen, dass ich über eine längere Zeit hinweg nicht mehr damit gearbeitet habe. Daher habe ich einige coole Funnktionen schon vergessen. Mit Github hatte ich am anfang Problem edoch danach gieng es sehr einfach, da ich mir mehrere Tutorials und Dokus angeschaut und durchgelesen habe. Ich habe viel über Container gelernt und selbst gesehen welche Vorteile dies gegen den normalen VM hat. Ich finde Git macht in vielen Anwendungsbereichen viel Sinn und werde versuchen, dies in Zukunft mehr zu gebrauchen. Was mir auch gefallen hat, ist das Arbeiten mit diesem Team. Jeder hatte jeden respektiert und wir haben alle gut arbeiten können.
###Helmina Jusufi
Auch Ich habe einige Male in der Schule mit Linux gearbeitet. Zudem haben wir Testserver im Geschäft die ich selber aufsetzen durfte und auf denen ich einiges ausprobieren konnte, somit bin ich vertraut mit einigen Befehlen. Für die Systemsicherheit interssiere ich mich sehr, daher habe ich in diesem Modul viel dazulernen können. Ich kannte Github vorher noch nicht. Ich habe nur davon gehört und in diesem Modul habe ich mich zum ersten Mal richtig damit auseinandergesetzt. Auch von Vagrant habe ich zum ersten Mal gehört und konnte auch dazu neues lernen. Die Unterlagen, welche uns zur Verfügung stehen, haben mir geholfen mich schnell in dieses Modul einzulesen und gleich loszulegen. Das Arbeiten auf der TBZ Cloud empfand ich ebenfalls wie meine Teammitglieder als angenehm.



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
