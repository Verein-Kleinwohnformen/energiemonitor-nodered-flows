## KWF Energiemonitor Node-RED auf Balena

### Info
Dieses Repository beinhaltet das Template für Node-RED auf der Balena-Umgebung. Dieser Teil läuft auf der Energiemonitor-Hardware, fragt alle benötigten Daten ab und schickt sie an ein Dashboard sowie an eine Datenbank

![overview](./img/overview.jpg)

### Einrichten auf Node-RED
Node-RED Container über Balena deployen und im Node-RED History-Tab dieses Repository clonen. Verschiedene Konfigurationen (verschiedene KWF Wohneinheiten) können über Branches gehandhabt werden. Main soll ein Template sein mit einer Übersicht aller Konnektoren.


### Status
__Implementiert__
- Shelly Pro 3EM Stromverbrauch 230V auf 3 Phasen
- Tuya WLAN Temperatur und Feuchtigkeitssensor (nicht sehr zuverlässig, nicht empfohlen)
- Neustart bei Netzwerkproblemen

__Nicht implementiert__
- 12V Monitor über RS485 (Peacefair)
- Azure Table Storage (Datenbank)

### Frühere Versionen
Die frühere Version der FH OST befindet sich auf dem Branch "BA_OST"