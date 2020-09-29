# Apache Dockerfile

Wir haben ein Dockerfile erstellt, welches einen Apache Webserver installiert. 

Vom Docker-Hub kann das Image nun mit folgendem Befehl heruntergeladen werden:
```
docker pull thefortium/apache2_ubuntu_sample
```

Man kan das Image auch direkt ausführen, am einfachsten mit dem folgenden Befehl:
```
docker run -itd -p 8080:80 thefortium/apache2_ubuntu_sample
```
