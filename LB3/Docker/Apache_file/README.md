# Apache Dockerfile

Wir haben ein Dockerfile erstellt, welches einen Apache Webserver installiert. 

Vom Docker-Hub kann das Image nun mit folgendem Befehl heruntergeladen werden:
```
docker pull XXX/apache2_ubuntu_sample
```

Man kan das Image auch direkt ausführen, am einfachsten mit dem folgenden Befehl:
```
docker run -itd -p 8080:80 tXXX/apache2_ubuntu_sample
```
