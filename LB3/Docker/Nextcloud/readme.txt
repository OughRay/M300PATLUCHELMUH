# Final Project Nextcloud

Dieses Compose-File erstellt einen Nextcloud Container, sowie einen MariaDB Container. Das Nextcloud Web-Interface wird an den `TCP-Port 1234` auf dem Host weitergeleitet. Der MariaDB Container beinhaltet eine MySQL-Datenbank, welche ein Volume vom Verzeichnis `./db` hat, damit die Datenbank persistent bleibt und vom Host aus gesichert, veschoben etc. werden kann. Damit die Datenbank von einem externen Service verwendet werden kann, müsste der `TCP-Port 3306` an den Host weitergeleitet werden. Diese MySQL Datenbank sollte jedoch nur für die Anfälligen Nextcloud Daten dienen, daher hat er kein Management Interface (zB. phpMyAdmin) und der `TCP Port 3306` wurde nicht an den Host geleitet.

Die Logins sehen aktuell wie folgt aus:

 * MariaDB Datenbank:

| Username  | Password |
|:---------:|:--------:|
|   root    |   m300   |



* Nextcloud Benutzer:

| Username  | Password |
|:---------:|:--------:|
|   m300   |   m300   |


Dieses Docker-Compose File kann mit folgendem Befehl ausgeführt werden:

```
docker-compose up -d
```
###### Das "-d" sorgt dafür, dass der Dialog der Container nicht angezeigt wird. Wird dies nicht gemacht, kann man zwar den Log in der Konsole sehen, jedoch wird die Konsole gleichzeitig auch mit den Container Logs Blokiert.
