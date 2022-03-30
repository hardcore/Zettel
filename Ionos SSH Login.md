# SSH Setup für Ionos Webhosting anlegen
## Screenshot
<img width="777" alt="Bildschirmfoto 2022-03-30 um 21 11 06" src="https://user-images.githubusercontent.com/58683/160913080-833422a7-49e7-4678-95d0-5be85ac21ac9.png">

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

