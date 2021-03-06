Nginx Projekt mit Hello World aus dem Docker Workshop

1. Im Hauptverzeichnis ist das Hello World Beispiel zu finden.
Dieses könnt ihr, wie gezeigt, mit "docker build ..." als Image erstellen.
Gestartet wird ein Container mit "docker run ...".

2. Im Ordner "loadbalancing" findet ihr eine erweiterte Variante, in dem 2 Nginx Webserver ("Hello World 1" & "Hello World 2") über "docker-compose.yml" gestartet werden.
Zusätzlich ist ein "Load Balancer" (./loadbalancing/nginx/config.conf) integriert, der entscheidet, ob "Hello World 1" oder "Hello World 2" angezeigt wird.
Zum Thema Load Balancer googelt ihr am besten, falls ihr diesen Begriff nicht kennen solltet.
Das Projekt könnt ihr über den Befehl "docker-compose up -d --build" starten.

Generell weitere Befehle:

- docker images:                                  Anzeige aller vorhandener Images
- docker pull <IMAGE_TAG>:                        Herunterladen eines bestimmten Docker Images (eine Auswahl findet ihr unter https://hub.docker.com/search?type=image)
- docker ps:                                      Anzeige aller laufenden Container
- docker ps -a:                                   Anzeige aller existierenden Container
- docker start <CONTAINER_NAME>/<CONTAINER_ID>:   Start eines bereits existierenden Docker Containers
- docker stop <CONTAINER_NAME>/<CONTAINER_ID>:    Stoppen des laufenden Containers
- docker rm <CONTAINER_NAME>/<CONTAINER_ID>:      Löschen eines vorhandenen Containers (hierzu muss der Container erst aber gestoppt sein)
- docker-compose down:                            Beenden der docker-compose Instanz (muss innerhalb des Verzeichnisses der betreffenden docker-compose.yml geschehen)
