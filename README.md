## KWF Energiemonitor Node-RED auf Balena

### Info
Dieses Repository beinhaltet das Template für Node-RED auf der Balena-Umgebung. Dieser Teil läuft auf der Energiemonitor-Hardware, fragt alle benötigten Daten ab und schickt sie an ein Dashboard sowie an eine Datenbank

![overview](./img/overview.jpg)

### Einrichten auf Node-RED
Node-RED Container über Balena deployen und im Node-RED History-Tab dieses Repository clonen. Verschiedene Konfigurationen (verschiedene KWF Wohneinheiten) können über Branches gehandhabt werden. Main soll ein Template sein mit einer Übersicht aller Konnektoren.


### Status
__Implementiert__
- Shelly Pro 3EM Stromverbrauch 230V auf 3 Phasen
- Netatmo Wetterstation innen und aussen
- Daten senden an Thingsboard
- Daten senden an Azure Table Storage (Datenbank)
- Neustart bei Netzwerkproblemen

__Nicht implementiert__
- 12V Monitor über RS485 (Peacefair)

__Entfernt__
- Support für Sensoren mit Tuya. Schlechte Erfahrungen mit Qualität und Antennenleistung

### Frühere Versionen
Die frühere Version der FH OST befindet sich auf dem Branch "BA_OST"
Die Version mit Tuya Sensoren befindet sich auf dem Branch "tuya_deprecated"