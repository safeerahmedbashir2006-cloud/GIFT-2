# Gift 2 — Abschlussbericht, 16. November 2026

Die bestehende Geschichte und die vorhandenen Medien wurden beibehalten. Der sichtbare Name wurde auf Wunsch nachträglich auf **Gift 2** geändert. Diese Fassung enthält gezielte Korrekturen und ein vollständiges Offline-Installationssystem.

## Korrigiert

- **Fotos:** Alle 38 Originalfotos sind weiterhin vorhanden und ihren bisherigen Bereichen zugeordnet. Die Flurbilder hängen zwischen den Säulen. Abstände, Wandorientierung und Rahmen wurden geprüft. 190 Sichtlinien zu Bildmitten und Ecken sind in der erzeugten 3D-Geometrie frei.
- **Bühne:** Die schmale zusätzliche Anzeige vor dem breiten Seitenbildschirm wurde mit diesem zusammengeführt. Der zentrale Titel bleibt mittig; Robinas Porträt steht in einem eigenen, seitlich getrennten Bereich. Die gegenüberliegende Dekorfläche ist symmetrisch angeordnet. Das Rednerpult wurde aus der Porträt-Sichtlinie verschoben.
- **Publikum:** Die doppelte Drehung der vorbereiteten Sitzfigur wurde entfernt. Beide Sitzvorlagen richten ihre Gesichter zur Bühne. Die Sitzpose wird vor dem Einfrieren der Geometrie korrekt ausgewertet. Nahe Gäste behalten die dezenten Kopf- und Klatschbewegungen.
- **Neuladen:** Frühere gespeicherte Spielpositionen werden nicht mehr übernommen. Jeder vollständige Seitenaufruf beginnt mit der schwarzen Limousinen-Einleitung. Innerhalb derselben Sitzung funktionieren Pass, Galerie- und Gala-Fortschritt weiter. Fokusverlust, Internetunterbrechung und Cache-Fertigstellung lösen keinen Neustart aus.
- **Abschluss:** Krönung, zehnsekündige persönliche Nachricht und Schlussvideo folgen weiterhin automatisch. Keine Sprachwahl und kein Weiter-Klick sind erforderlich. Eine Tonfreigabe kann der Browser aus technischen Gründen trotzdem verlangen.
- **Leistung:** Instancing, Sicht- und Entfernungsbegrenzung bleiben erhalten. Die automatische Anpassung reduziert zuerst teure Effekte und Animationsarbeit, danach bei Bedarf die Renderauflösung. Im ausgeglichenen Profil entfällt die aufwendige zusätzliche Würfelspiegelung der Limousine. Fotos behalten ihre eigene Auflösung. Zielprofile: 30 FPS und, für stärkere Geräte, 60 FPS. Während des Schlussfilms pausiert die 3D-Berechnung.
- **Veröffentlichung:** Entwicklungs- und Bearbeitungssteuerungen wurden aus den normalen Menüs entfernt. Das Hosting-Paket enthält Startdatei, `test.html`, Medien, Offline-Dateien und Lizenzhinweise. Die bestehende Zugriffsfreigabe wurde nicht erweitert.

## Offline-System

Die Installation umfasst 72 logische Dateien mit insgesamt etwa 33,3 MB. Jeder Inhalt wird anhand seiner vollständigen Länge und SHA-256-Prüfsumme geprüft. Erst nach erfolgreicher Gesamtprüfung erscheint **„Offline ready · all media verified“**. Unvollständige oder beschädigte Downloads werden nicht als fertig gemeldet; Wiederholung nach einer Verbindung ist möglich.

Unveränderte Medien werden über ihren Inhalts-Hash gemeinsam gespeichert. Beim tatsächlichen Browser-Test wurde eine Speichergrenze beim Update entdeckt und die vorherige doppelte Speicherung behoben. Video-Teilabrufe werden aus dem vollständigen lokalen Video bedient. Beim ersten Online-Abspielen bleiben noch nicht gespeicherte Videos streambar. Die Cache-Aktivierung setzt das Spiel niemals zurück.

Einmal die HTTPS-Seite online öffnen und warten, bis die vollständige Offline-Bereitschaft bestätigt wird. Danach denselben Browser und dasselbe Profil verwenden. Das Löschen von Website-Daten oder eine spätere automatische Speicherbereinigung des Browsers kann eine erneute Installation nötig machen. Die einzelne herunterladbare HTML-Datei enthält ihre Medien direkt und kann unabhängig davon lokal geöffnet werden.

## Tatsächlich ausgeführte Tests

| Prüfung | Ergebnis und Umfang |
|---|---|
| Offline im echten Chrome-Browser | Nach vollständiger Installation wurde der Vorschau-Server gestoppt. Alle 72 Dateien waren weiterhin lesbar; Längen und Prüfsummen stimmten. |
| Vollständige Offline-Videos | Beide vorhandenen Filme wurden im Chrome-Browser ohne Serververbindung bis zu ihren jeweiligen `ended`-Ereignissen abgespielt. |
| Video-Teilabrufe | Im Browser wurden beide MP4-Dateien mit korrektem 206-Status und exakten Teilbytes gelesen. Zusätzliche automatische Tests decken offene Bereiche, Suffix-Bereiche und ungültige Bereiche ab. |
| Fehler- und Speichertests | Unvollständiger Transfer meldet keine Bereitschaft. Beschädigte Cache-Inhalte werden erkannt und nach Wiederverbindung repariert. Die Cache-Migration nach einer tatsächlichen Quota-Meldung hat im Browser bestanden. |
| Fotografien | Alle 38 Dateien decodiert und nicht leer; 38 unterschiedliche Ausstellungsplätze; 190 freie Geometrie-Sichtlinien. Keine Originaldatei ersetzt. |
| Bühne und Figuren | Getrennte Titel-/Porträt-Flächen, symmetrische Bereiche, keine schmale Anzeige davor; tatsächliche Augen-/Haar-Geometrie beider Sitzvorlagen zeigt zur Bühne; gültige Knochen-/Animationswerte. |
| Gesamte Geschichte | Automatisierte Zustands- und Geometrieprüfungen: Limousine, erster Film bei 20 Sekunden, Herzreaktion, Ankunft, Security, sechs Galerien, Wege/Treppen, Aufzug, Sitzplatz, drei Vorstellungen, Platz 3, Platz 2, Robina als Platz 1, E-Aufstehen, Krönung, automatische Nachricht, Schlussfilm, Schlüssel. |
| Refresh und laufende Sitzung | Fünf simulierte vollständige Starts mit alten Spielständen aus unterschiedlichen Kapiteln beginnen jeweils einmal am Anfang. Fokusverlust und Online-Ereignisse setzen nicht zurück. |
| Langsames Gerät | Simulierte langsame Frame-Zeiten prüfen, dass zuerst Effekte und erst danach die Renderauflösung reduziert werden. Keine Behauptung einer gemessenen GPU-Bildrate. |
| Build | JavaScript-Syntax, lokale Asset-Verweise, Prüfsummen, vollständiges Hosting-Archiv und eingebettete Einzeldatei geprüft. |

## Verbleibende technische Grenzen

Der bereitgestellte 3D-Testbrowser meldet weiterhin **„Error creating WebGL context“**. Ein vollständiger visuell gerenderter Spieldurchlauf und eine echte GPU-/FPS-Messung konnten deshalb hier nicht erfolgen. Die obigen Geometrie-, Zustands-, Cache- und nativen Videotests ersetzen diese Sichtprüfung nicht.

Edge und Safari standen hier nicht als separate Testbrowser zur Verfügung. Die Windows-/Pakistan-Hardware wurde nicht direkt getestet. Sound-Autoplay hängt von der Browserfreigabe ab. Für gesprochene Moderation werden bevorzugt installierte lokale englische Stimmen verwendet; deren Offline-Verfügbarkeit hängt vom Gerät ab. Die vollständigen Dialogtexte und vorhandenen Musik-/Tondateien sind mitgeliefert.

Die bestehende Online-Seite wurde unter derselben Adresse aktualisiert; ihre bisherigen privaten Zugriffsrechte bleiben unverändert. Das Hosting-ZIP ist für eine anschliessende Veröffentlichung auf eigenem HTTPS-Hosting vorbereitet.

Namensänderung: Browser-Titel, sichtbare Kopfzeile und Link-Metadaten heissen jetzt Gift 2. Geschichte und Medien wurden dafür nicht verändert.
