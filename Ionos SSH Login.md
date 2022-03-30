# SSH Setup für Ionos Webhosting anlegen
## SSH Setup auf lokaler Maschine einrichten
Hosteintrag anlegen:
```
➜ cat ~/.ssh/config
Host domain.name
    HostName accessxxxxxxx.webspace-data.io
    User u10xxxxx
```
Optional: Rechte anpassen
```
➜ chmod 600 ~/.ssh/config
```
## Public Key zu Ionos übertragen
Das File "authorized_keys" auf Server anlegen und mit Public Key befüllen
```
cat ~/.ssh/id_rsa.pub | ssh domain.name "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"
```
