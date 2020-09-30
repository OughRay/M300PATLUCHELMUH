# LB3 Dokumentation vom Team PATLUCHELMUH

# Einleitung
In diesem Dokument beschreiben wir die Arbeit von der LB3. Bevor wir mit dem Projekt angefangen haben wir die verschiedenen Aufgaben unterteilt. 

# Inhaltsverzeichnis
* Was ist Docker?
    * Docker Befehle
* Was ist Kubernetes
* Warum brauche ich Kubernetes und was kann ich damit tun?
* Umgebung
* Netzwerkplan für Nextcloud
* Unsere Docker Projekte
* Testfälle Apache 2
* Testfälle Mail2
* Testfälle Nextcloud


# Was ist Docker?
Docker ist eine Freie Software zur Isolierung von Anwendungen mit Hilfe von Containervirtualisierung. Docker vereinfacht die Bereitstellung von Anwendungen, weil sich Container, die alle nötigen Pakete enthalten, leicht als Dateien transportieren und installieren lassen. Die Docker-Technologie verwendet den Linux Kernel und seine Funktionen wie Cgroups und namespaces, um Prozesse zu isolieren, damit diese unabhängig voneinander ausgeführt werden können. Diese Unabhängigkeit ist der Zweck der Container – die Fähigkeit, mehrere Prozesse und Apps getrennt voneinander betreiben zu können. So wird Ihre Infrastruktur besser genutzt und gleichzeitig die Sicherheit bewahrt, die sich aus der Arbeit mit getrennten Systemen ergibt.

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
Kubernetes ist ein Open-Source-System zur Automatisierung der Bereitstellung, Skalierung und Verwaltung von Container-Anwendungen, das ursprünglich von Google entworfen und an die Cloud Native Computing Foundation gespendet wurde. Es zielt darauf ab, eine Plattform für das automatisierte Bespielen, Skalieren und Warten von Anwendungscontainern auf verteilten Hosts zu liefern. Es unterstützt eine Reihe von Container-Tools, einschliesslich Docker. Google hat das Kubernetes-Projekt 2014 als Open-Source-Projekt zur Verfügung gestellt. Kubernetes baut auf anderthalb Jahrzehnten Erfahrung auf, die Google mit der Ausführung von Produktions-Workloads in großem Maßstab hat, kombiniert mit den besten Ideen und Praktiken der Community.




# Warum brauche ich Kubernetes und was kann ich damit tun?
Kubernetes hat eine Reihe von Funktionen. Es kann gesehen werden als:

eine Containerplattform
eine Microservices-Plattform
eine portable Cloud-Plattform und vieles mehr.
Kubernetes bietet eine containerzentrierte Managementumgebung. Es koordiniert die Computer-, Netzwerk- und Speicherinfrastruktur im Namen der Benutzer-Workloads. Dies bietet einen Großteil der Einfachheit von Platform as a Service (PaaS) mit der Flexibilität von Infrastructure as a Service (IaaS) und ermöglicht die Portabilität zwischen Infrastrukturanbietern.





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
* Luca Miani - @oughray
* Patrick Schwab - @psychodellic
* Helmina Jusufi - @helminajusufi
* Muhammed Ercan - @Muhammedercan
## Git-Client wurde verwendet
1.	SSH key-Link in die Konsole einfügen
* In der Konsole den den git clone befehl ausführen.
* Mit den richtigen logindaten anmelden.
* (In der VM Console) Unter Source Controll das Repository Stagen und hinzufügen
## Persönlicher Wissenstand im Bezug auf die wichtigsten Themen ist dokumentiert (Containerisierung / Docker, Microservices)
### Luca Miani
Ich habe bis dato nicht mit Docker oder Container gearbeitet. Jedoch konnte ich mich gut einlesen in das Thema und schon loslegen. Einen eigenen Github Acount hatte ich schon vor diesem Modul. Jedoch hatte ich am Anfang dieses Moduls auch keine Erfahrungen mit Vagrant. Dies lernte ich jedoch im Laufe dieses Projektes kennen. Dazu lies ich verschiedene Beiträge und machte mich schlau auf Github. Ausserdem konnte ich bei Fragen immer wieder mein Team fragen, welches mir auch weiterhilf. Das Arbeiten auf der TBZ Cloud fand ich sehr angenehm. Ich konnte ausserdem einiges lernen im Bereich Systemsicherheit. In das Thema SSH habe ich mich ein wenig vertieft und konnte somit auch dies so im Projekt einsetzen.
### Muhammed Ercan
Im Geschäft arbeite ich mehrheitlich mit Macs. Deshalb habe ich nicht viel mit Docker oder Microservices zu tun. Am Anfanh hatte ich ein wenig Schweirigkeiten, doch mit der Zeit habe ich immer mehr verstanden. Weil Mac OS und Linux sehr ähnlich sind, hatte ich schon einige Erfahrungen mit Linux. Ausserdem habe ich mehrere Server mit Linux aufgesetzt und diese betrieben. Des weiteren habe ich noch einige Services drauf lauffen lassen. Jedoch hatte ich noch vor dem Modul keinen Github Account. Daher schaute ich am Anfang einige Blogs zu Github. Daher kamen mit der Zeit Kentnisse auch über Mark Down und Github. Ich habe zusammen mit Helmina Jusufi im Modul Systemsicherheit gearbeitet. Daher hatten wir von diesem Modul auch Erfahrungen mit der Sicherheit eines Systems. Zu den verschiedenen Vagrant Files habe ich nicht viel gewusst, daher konnte ich auch einiges zu den Vagrant-Files dazulernen. Ausserdem hat mir das Arbeiten auf TBZ Cloud gefallen.
### Patrick Schwab
Mit den Themen Linux hatte ich schon zuvor zutuhn, doch mit Github oder ähnliche Systeme hatte ich zuvor noch nie gearbeitet. Ich kannte die Grundlagen von MIcroservices oder Docker. Deshalb konnte ich mit meinem Team schon früh ins Projekt starten. Ich habe privat schon mit Linux gearbeitet. Jedoch muss ich sagen, dass ich über eine längere Zeit hinweg nicht mehr damit gearbeitet habe. Daher habe ich einige coole Funnktionen schon vergessen. Mit Github hatte ich am anfang Problem edoch danach gieng es sehr einfach, da ich mir mehrere Tutorials und Dokus angeschaut und durchgelesen habe. Ich habe viel über Container gelernt und selbst gesehen welche Vorteile dies gegen den normalen VM hat. Ich finde Git macht in vielen Anwendungsbereichen viel Sinn und werde versuchen, dies in Zukunft mehr zu gebrauchen. Was mir auch gefallen hat, ist das Arbeiten mit diesem Team. Jeder hatte jeden respektiert und wir haben alle gut arbeiten können.
### Helmina Jusufi
ich wusste am Anfang nicht, was Container oder Docker sind. Deshlab habe ich am Anfang viel mit Muhammed angeschaut. Mit der Zeit haben wir immer mehr verstanden.  Zudem haben wir Testserver im Geschäft die ich selber aufsetzen durfte und auf denen ich einiges ausprobieren konnte, somit bin ich vertraut mit einigen Befehlen. Für die Systemsicherheit interssiere ich mich sehr, daher habe ich in diesem Modul viel dazulernen können. Ich kannte Github vorher noch nicht. Ich habe nur davon gehört und in diesem Modul habe ich mich zum ersten Mal richtig damit auseinandergesetzt. Auch von Vagrant habe ich zum ersten Mal gehört und konnte auch dazu neues lernen. Die Unterlagen, welche uns zur Verfügung stehen, haben mir geholfen mich schnell in dieses Modul einzulesen und gleich loszulegen. Das Arbeiten auf der TBZ Cloud empfand ich ebenfalls wie meine Teammitglieder als angenehm.
# K3
## Bestehenden Docker-Container kombinieren
Eigene Container wurden miteinander Verbunden. Wir haben eine Nexcloud Umgebung aufgebaut mit einem MariaDB Container und einem Nexcloud Container, der Nexcloud Container beinhaltet noch einen Apache2 Dienst um die Webseite anzeigen zu lassen. 

## Backend 
Als Backend haben wir die MariaDB als Datenbank und den Apache2 Dienst um die Nexcloud Webseite anzeigen zulassen.

## Frontend
Haben wir den Nexcloud dienst um Daten zum Beispiel auf der Webseite abspeicher zu können. 

## Volumes persistente Datenablage
Die ganzen Daten des Nextcloud Docker Container (File-Uploads) sind in /var/www/html gesichert
Der Docker Dienst wird alle Daten in den Volumes speichern /var/lib/docker/volumes/.. 
Das heisst sobald der Docker Container ausgeschaltet wird, warden alle Daten verloren.
Ein neues Verzeichnis sollte für das Sichern der Daten . Um dies zu machen werden wir ein Verzeichnis für den Nextcloud Container und ein Verzeichnis für die DB einrichten.
Nextcloud:
•	`/var/www/html/` Der Ordner wo alle Nextcloud Daten liegen werden
•	`$ docker run -d \
•	-v nextcloud:/var/www/html \
nextcloud`
Datenbank:
•	`/var/lib/mysql MySQL / MariaDB Daten
•	$ docker run -d \
•	-v db:/var/lib/mysql \
mariadb`


## Eingerichtete Umgebung ist dokumentiert
Folgende Container wurden erstellt
Docker | Funktion
------------ | -------------
Datenbank | Docker mit MariaDB mit der Datenbank für Nexcloud Accounts
Web | Docker mit Apache2 und Nexcloud Dienst um die webseite anzeigen zu lassen

## Netzwerkplan



# K5
## Reflexion
Hier wird über unsere Arbeit reflektiert

### Reflexion Muhammed Ercan
Schon am ersten Tag, war es für mich interessant in diesem Modul. Die LB3 war für mich interessant und lehreich. Das Projekt hatte mir Spass gemacht, auch wenn es eher kürzer ausgefallen ist, als wie gewohnt. Innerhalb dieses Projektes war es möglich vieles zu lernen. Diese Chance habe ich genützt, um mich mit meinem Team stetig auszutauschen. Auch zum ersten Mal habe ich mit der TBZ Cloud gearbeitet. Das hat mir gefallen, weil ich das Gefühl hatte, dass es viel schneller ist. Das Arbeiten an der Fach Hochschule gefiel mir sehr. Die Lehrperson war immer wieder bei Fragen erreichbar. Somit war es für mich eine gute Mischung aus Inputs vom Lehrer und dem Selbst Orientierten Lernen. Ich freue mich auf die weiteren Module.

### Reflexion Helmina Jusufi
### Arbeit
In diesem Modul habe ich sehr viel neues kennengelernt. Beim Einrichten der Umgebung habe ich gesehen, was es für verschiedene Möglichkeiten gibt. Ich habe gelernt was VirtualBox ist, ich habe GitHub kennengelernt, zudem habe ich mich bei der Umsetzung mit Vagrant auseinandergesetzt, welches ich vorher auch noch nicht kannte. Der Lehrer war für Fragen immer offen und konnte mir auch sehr gut helfen. Die LB3 war etwas schwieriger, jedoch konnte ich vieles dazu lernen. 
### Zusammenarbeit
Die Zusammenarbeit im Team war ausgezeichnet. Wir haben uns alle zuerst eingelesen und alle Fragen im Team geklärt. Danach haben wir uns die Aufgaben aufgeteilt und haben uns alle an die Aufteilung der Aufgaben gehalten. Dies hat uns die Arbeit am Projekt sehr erleichtert. Wir konnten alle sehr gut miteinander umgehen. Da Muhammed Ercan, Luca Miani und ich bereits oft miteinander Projekte geführt haben und bei Schulaufträgen gemeinsam in einer Gruppe waren, fiel uns die Zusammenarbeit noch leichter. Somit sind wir sehr schnell zum Ziel gekommen und hatten keine Probleme bei der Umsetzung.

### Reflexion Luca Miani
Obwohl ich schon ein wenig Vorwissen hatte, konnte ich in diesem Modul sehr viel neues lernen. Ich habe Vagrant sehr gut kennengelernt und kann nun gut damit umgehen. Da ich schon oft mit Linux gearbeitet habe und es sehr gerne mache, hat mir diese LB sehr Spass gemacht. Bei Problemen habe ich mich beim Lehrer oder bei meinen Teamkollegen gewendet. Die Zusammenarbeit mit Muhammed Ercan, Helmina Jusufi und Patrick Schwab war sehr gut. Wir sind gut miteinander ausgekommen, haben uns gegenseitig unterstützt und unsere Arbeiten zeitgerecht fertiggestellt. Was ich auch sehr gut fand war, dass wir mit Github gearbeitet haben und so alle jederzeit ganz einfach Zugriff darauf hatten. Das Arbeiten mit den Containern machte mir Spass. Ich habe nich nie mit Containern gearbietet, deshlab war es so spannend. 

### Reflexion Patrick Schwab
Ich habe für die Zukunft gelernt, dass die Vagrant Files einen grossen Wert haben. Ausserdem weiss ich nun, dass ich im Team mehr Spass am Lernen habe als allein und es nicht darauf ankommt, ob ich mit meinen Freunden in einer Gruppe bin oder mit anderen Mitschülern, die ich weniger gut kenne. Dazu kommt, dass ich viele neue Funktionen kennenlernen durfte im Bezug auf Virtuelle Maschinen, Systemsicherheit und Vagrant Files. Das Arbeiten mit Github hat mir ausserdem auch Spass gemacht, weil man alles für jeden verfügbar hat. Ich konnte mein vorheriges Wissen in dieser LB3 gut miteinbeziehen. Das Team war immer da bei Fragen.


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
