# ESP8266 Setup Anleitung

Diese Anleitung beschreibt Schritt für Schritt, wie der ESP8266 geflasht und konfiguriert wird, inklusive WLAN- und IP-Einstellungen.

---

## 1. Flashen der Firmware

1. Schließe den ESP8266 an deinen Computer an.
2. Stelle sicher, dass die **Flash-Adresse auf `0x00000`** gesetzt ist.
3. Lade die gewünschte `.bin` Datei auf den ESP8266.
4. Warte, bis der Flash-Vorgang abgeschlossen ist.

> **Hinweis:** Verwende ein zuverlässiges USB-Kabel und stelle sicher, dass der ESP8266 während des Flashens nicht getrennt wird.

---

## 2. WLAN-Daten über Webserver eintragen

1. Starte den ESP8266. Wenn er noch keine WLAN-Daten hat, öffnet er automatisch das **Setup-Portal**:
   - SSID des ESP: `ESP8266-Setup`
2. Verbinde dich mit diesem WLAN.
3. Öffne einen Browser und gehe zu: `http://192.168.4.1`
4. Trage deine **WLAN-SSID** und **Passwort** ein.
5. Speichere die Daten. Der ESP8266 startet automatisch neu und verbindet sich mit deinem WLAN.

---

## 3. DHCP-Einstellungen im Router

1. Melde dich im Router an.
2. Suche die **DHCP-Tabelle** oder **verbundene Geräte**.
3. Finde die IP-Adressen, die dem ESP8266 zugewiesen wurden.
4. Setze diese IPs als **feste IP-Adresse / statische Zuweisung**, damit sie sich nicht ändern.
5. Notiere die IPs der jeweiligen Gegenübergeräte für später.

---

## 4. Firmware erneut flashen

1. Schließe den ESP8266 wieder an den Computer an.
2. Flash die `.bin` Datei erneut (Flash-Adresse `0x00000`).
3. Trage beim Webserver zusätzlich zu WLAN-Daten die **statischen IPs der Gegenübergeräte** ein.
4. Speichere die Daten und starte den ESP neu.

> Jetzt sind die Geräte mit festen IPs konfiguriert und können zuverlässig miteinander kommunizieren.

---

**Fertig!**  
Der ESP8266 ist nun einsatzbereit, mit WLAN verbunden und festen IP-Adressen für stabilen Betrieb.
