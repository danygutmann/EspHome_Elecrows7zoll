# ESPHome Elecrow 7 Zoll

Dieses Repository enthält Beispiel- und Standardkonfigurationen für ein ESPHome-Projekt mit einem **Elecrow 7-Zoll-Display** auf Basis eines **ESP32-S3**.

## Enthaltene Default-Dateien

Im Repository werden nach und nach mehrere Default-Konfigurationen abgelegt.  
Aktuell ist folgende Datei enthalten:

- `default_lamda.yaml`

> Hinweis: Es werden noch weitere Default-Dateien ergänzt.

---

## Beschreibung von `default_lamda.yaml`

Die Datei `default_lamda.yaml` ist eine grundlegende ESPHome-Konfiguration für ein 7-Zoll-RGB-Display mit Touch-Unterstützung.  
Sie dient als Startpunkt für eigene Anpassungen und Tests.

#### Anzeige per Lambda
Die Anzeige wird aktuell über eine Lambda-Funktion gezeichnet.  
Dabei werden folgende Elemente dargestellt:
- ein roter Hintergrund
- ein weißer Rahmen
- der Text `DIS08070H`

Diese Konfiguration ist gut geeignet, um die grundlegende Display-Ausgabe und den touchscreen schnell zu testen.





## Hinweise

Die Datei `default_lamda.yaml` ist als Basisbeispiel gedacht und kann individuell erweitert oder angepasst werden.
Ich habe einige Zeit gebraucht einen soliden Startpunkt zu bekommen, ggt hilft es jendamden ;-)
