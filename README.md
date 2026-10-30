# Energiemonitor: Node-RED-Beispiel-Flows (deprecated)

**Status: deprecated.** Diese Flows sind die ältere Beispielsammlung des [KWF Energiemonitors](https://github.com/Verein-Kleinwohnformen/energiemonitor-docs). Das Ziel ist, alle Sensoren im [KWF Datenbank-Connector](https://github.com/Verein-Kleinwohnformen/kwf-energiemonitor-db) zu bündeln. Das Repo bleibt als Vorlage und als Beispiel eines echten Hauses bestehen, wird aber nicht mehr weiterentwickelt.

**Du willst einen Monitor bauen?** Starte mit der [Bauanleitung](https://github.com/Verein-Kleinwohnformen/energiemonitor-docs/blob/main/docs/bauanleitung.md). Der Energiemonitor ist kein Produkt des Vereins Kleinwohnformen, sondern eine offene Plattform.

## Inhalt

Die Datei `flows.json` enthält Flows für Node-RED auf der Balena-Umgebung ([Container](https://github.com/Verein-Kleinwohnformen/energiemonitor-balena-nodered)). Branches:

| Branch | Inhalt |
|---|---|
| `master` | Template: Übersicht der Konnektoren (Shelly Pro 3EM, Netatmo mit eigenem OAuth2-Flow, PZEM-017) |
| `weidenbaum` | Konfiguration eines echten Hauses, **enthält zusätzlich persönliche Steuerlogik** (Heizung, Frostschutz, zeitgesteuertes Lüften, Silence-Button). Nur als Beispiel gedacht, nicht als Vorlage zum Messen |
| `BA_OST` | Ursprungsversion der FH OST (historisch) |
| `tuya_deprecated` | Version mit Tuya-Sensoren (entfernt wegen schlechter Funkqualität und Datenverlust) |

## Einrichten

1. Node-RED-Container über Balena deployen.
2. Die Flows aus `flows.json` in Node-RED importieren (Menü, Import) oder dieses Repo mit dem integrierten Git von Node-RED klonen.
3. Für jeden Sensor `sensor_id` und `metering_point` gemäss deinem [Messschema](https://github.com/Verein-Kleinwohnformen/energiemonitor-docs/blob/main/docs/messpunkte.md) setzen und an den KWF Datenbank-Connector senden.
4. Zugangsdaten (zum Beispiel das Netatmo-Refresh-Token) trägst du **selbst in Node-RED** ein. Sie werden mit deinem `ENCRIPTION_KEY` verschlüsselt und gehören nie in ein Repo. Die Datei `flows_cred.json` ist deshalb in `.gitignore`.

Hinweise zu den Sensoren (Shelly, PZEM-017, Netatmo, Victron, Sensirion BLE) stehen in der [Bauanleitung](https://github.com/Verein-Kleinwohnformen/energiemonitor-docs/blob/main/docs/bauanleitung.md), Kapitel 9.

## Status der Funktionen

- Implementiert: Shelly Pro 3EM, Netatmo mit OAuth2-Flow, PZEM-017 (DC), Neustart bei Netzwerkproblemen, Senden an den KWF-Connector.
- Entfernt: Tuya-Sensoren, Thingsboard und Azure Table Storage. Der offizielle Netatmo-Block wird nicht mehr gepflegt, deshalb der manuelle OAuth2-Flow im Tab "Netatmo Authentication".

## Lizenz

Apache License 2.0, siehe [LICENSE](LICENSE). Fragen: [energiemonitor@kleinwohnformen.ch](mailto:energiemonitor@kleinwohnformen.ch)
