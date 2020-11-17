Für die PHP 7.4 entwiklung ein einfacher Server mit folgenden Eigenschaften:

##### Kerneigenschaften:
- Server Apache 2.4
- PHP 7.4 mit xdebug und SSL
- Mysql 5.7 mit PHPmyAdmin
- Debian Linux
- Composer im Linux
- Docker/ .env für Variablen zur einstellung für's Projekt
- Redis 6.0

Die PHP Datein müssen in dem www/ Ordner liegen dorthin ist mit docker-compose.yml gemountet.

### Schnellstrart Anleitung

Als erstes die Windows Powershell als Admin starten und in den Ordner von den PhpStormProjects wechseln. 

Press Windows+R to open the Run dialog box, and then type “powershell” in the text box. You can either click “OK” (or press the Enter) to open a regular PowerShell window, or press Ctrl+Shift+Enter to open an elevated PowerShell window.
                                                                                                         


#### 1. Mit der Windows Powershell ein Projekt erstellen
```
# ins PhpStorm verzeichniss wechseln
cd PhpStormProjects

# dort mit git ein neues Projekt Verseichniss anlegen
git clone https://github.com/rogergerecke/docker-linux-php-develop.git projekt_ordner_name
```

#### 2. Schnell mit PhpStorm ein Projekt aus bestehenden Datein anlegen
Projekt aus bestehende Verzeichnis erstellen im.  

```
# Konfiguration für Local-Built-In-Server ist Localhost oder Docker
http://localhost/test-its-server-works.php
```

#### 3. Docker Container auf einmal bilden und starten:
```
# Befehl zum Container erstellen und starten mit in der Powershell
docker-compose up -d
```


#### 5. Testen ob der Docker-Container gestartet ist:
Im Browser die folgenden URL's aufrufen um die Funktion vom Server zu testen.
- http://127.0.0.1/test-its-server-works.php
- http://127.0.0.1:8080 PhpMyAdmin

##### Nach der Installation
Nach der Installation kann man in PhpStorm direkt über den Reiter Service den 
Container starten, stopen und sehen welche Variablen geladen sind.

###### TODO
- add ARG vars vor folder and server
- auto genarate SSL und copy in Folder with bash
- .env with default config