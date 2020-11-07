Dies ist meine schnellstart Entwiklungs-Umgebung mit in einem Docker Container.  Es dient dazu um schnell einen Server für Kundenprojekte in PHP aufzusetzen.

Kerneigenschaften:
- Server Apache
- PHP mit xdebug und SSL
- Mysql mit PHPmyAdmin
- Composer im Linuxkern
- Variable Container Namen für Projektbezug in .env

Der gemountete Root-Ordner ist www

### Windows Powershell Projekt erstellen
`cd zum verzeichnis`
`git clone https://github.com/rogergerecke/docker-linux-php-develop.git`

### PhpStorm fast Setup
Projekt aus bestehende Verzeichnis erstellen.  Konfiguration für Local-Built-In-Server ist Localhost oder Docker
http://localhost/test-its-server-works.php

### Docker Container auf einmal bilden und starten:
`docker-compose up -d`


#### Testen ob der Docker-Container gestartet ist:
- http://127.0.0.1/test-its-server-works.php
- http://127.0.0.1:8080 PhpMyAdmin

###### TODO
- add ARG vars vor folder and server
- auto genarate SSL und copy in Folder