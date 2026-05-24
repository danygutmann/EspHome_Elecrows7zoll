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

### Inhalt der Konfiguration

#### Allgemeine Gerätekonfiguration
- Gerätename: `dis08070h-minimal`
- Friendly Name: `dis08070h-minimal`
- Verwendung von `esp-idf`
- Aktiviertes PSRAM für speicherintensive Display-Anwendungen

#### Boot-Verhalten
Beim Start wird automatisch die Hintergrundbeleuchtung des Displays aktiviert.  
Die Helligkeit wird dabei zunächst auf **35 %** gesetzt.

#### Netzwerk und Zugriff
Die Datei enthält die grundlegenden ESPHome-Komponenten für:
- WLAN-Verbindung
- API-Anbindung
- OTA-Updates
- Captive Portal

Die WLAN-Zugangsdaten werden über `secrets` eingebunden.

#### Hintergrundbeleuchtung
Die Display-Beleuchtung wird über PWM gesteuert:
- Ausgang über `ledc`
- Pin: `GPIO2`
- als monochromatisches Licht in ESPHome eingebunden

#### I²C
Für Peripherie wie den Touch-Controller ist I²C aktiviert:
- SDA: `GPIO19`
- SCL: `GPIO20`

#### Schriftart
Es wird die Schriftart **Roboto** über Google Fonts geladen.

#### Display
Das Display ist als `rpi_dpi_rgb` konfiguriert mit:
- Auflösung: **800 x 480**
- definierter RGB-Pinbelegung
- individuellen Timing-Werten für Synchronisation und Pixeltakt

#### Anzeige per Lambda
Die Anzeige wird aktuell über eine Lambda-Funktion gezeichnet.  
Dabei werden folgende Elemente dargestellt:
- ein roter Hintergrund
- ein weißer Rahmen
- der Text `DIS08070H`

Diese Konfiguration ist gut geeignet, um die grundlegende Display-Ausgabe schnell zu testen.

#### Touchscreen
Ein `gt911`-Touchscreen ist eingebunden.  
Bei einer Berührung werden die Koordinaten im Log ausgegeben.  
Zusätzlich wird beim Loslassen eine Log-Meldung erzeugt.

---

## Ziel der Default-Dateien

Die Default-Dateien in diesem Repository sollen als Ausgangsbasis dienen für:

- erste Funktionstests
- Display- und Touch-Tests
- eigene Oberflächen mit ESPHome
- Anpassungen für verschiedene Elecrow-Displays oder Projektvarianten

---

## Geplante Erweiterungen

Weitere Default-Dateien können künftig z. B. enthalten:

- alternative Display-Layouts
- andere Lambda-Beispiele
- vorbereitete LVGL-Konfigurationen
- erweiterte Touch-Funktionen
- Beispielseiten für Home-Assistant-Integration

---

## Hinweise

Die Datei `default_lamda.yaml` ist als Basisbeispiel gedacht und kann individuell erweitert oder angepasst werden.
