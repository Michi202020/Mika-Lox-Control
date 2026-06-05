# Mika Lox Control

Diese Anleitung beschreibt den kompletten Ablauf von der Firmware-Installation bis zur Freischaltung Schritt für Schritt.

## Installation und Erststart

Bevor eine Freischaltung möglich ist, muss die passende FULL-Binärdatei auf das richtige Gerät geflasht werden.

Verwende dafür am einfachsten diese Seite:

https://esptool.spacehuhn.com/

Wichtig: Die FULL-Datei muss auf die Adresse 0x0000 geflasht werden.

![ESPWebTool Uploadseite](https://github.com/user-attachments/assets/f56b4d3d-19e2-4320-bff9-ff60b8b84607)

### 1. Die richtige Firmware herunterladen

Lade aus dem Release die zu deinem Gerät passende FULL-Datei herunter:

- Mika-Lox-Control-4848S040CIY1-FULL.bin
- Mika-Lox-Control-4848S040CIY3-FULL.bin

Nutze nur die Datei, die zu deinem Gerät passt.

### 2. Was du vor dem Flashen brauchst

Vor dem Start bitte kurz prüfen:

- Ein USB-Datenkabel. Ein reines Ladekabel funktioniert nicht.
- Einen PC oder Laptop mit Google Chrome oder Microsoft Edge.
- Die passende heruntergeladene FULL-Datei.
- Das Gerät muss per USB angeschlossen sein.
- Falls ein anderes Programm schon auf den USB-Port zugreift, dieses vorher schließen.

### 3. Upload-Seite öffnen

1. Öffne https://esptool.spacehuhn.com/ in Chrome oder Edge.
2. Auf der Seite siehst du den Button Connect.
3. Klicke auf Connect.

### 4. USB-Gerät auswählen

Nach dem Klick auf Connect öffnet dein Browser ein Fenster zur USB- bzw. seriellen Port-Auswahl.

Gehe dabei genau so vor:

1. Suche in der Liste den Eintrag für dein angeschlossenes ESP32-Gerät.
2. Je nach System kann der Eintrag zum Beispiel so aussehen:
   - USB JTAG/serial debug unit
   - CP210x USB to UART Bridge
   - CH340
   - Silicon Labs CP210x
   - USB Serial
   - unter Linux manchmal ein Eintrag zu ttyUSB oder ttyACM
3. Wenn mehrere Einträge angezeigt werden und du unsicher bist:
   - Trenne das Gerät kurz vom USB.
   - Öffne die Auswahl erneut.
   - Schließe das Gerät wieder an.
   - Wähle den neu erschienenen Eintrag.
4. Markiere den richtigen Eintrag.
5. Klicke im Browserfenster auf Verbinden oder Connect.

Wenn gar kein Gerät angezeigt wird, prüfe zuerst ein anderes USB-Kabel oder einen anderen USB-Port.

### 5. FULL-Datei eintragen und Flash-Adresse setzen

Nach erfolgreicher Verbindung fügst du die Firmware-Datei in ESPWebTool ein.

1. Füge die heruntergeladene FULL-Datei hinzu.
2. Achte darauf, dass die Flash-Adresse auf 0x0000 steht.
3. Falls dort ein anderer Wert eingetragen ist, ändere ihn manuell auf 0x0000.
4. Prüfe noch einmal, dass wirklich die richtige FULL-Datei ausgewählt wurde.
5. Klicke danach auf Program.

Wichtig: Nicht auf eine andere Adresse flashen. Für die FULL-Datei muss 0x0000 verwendet werden.

### 6. Warten bis der Flash-Vorgang fertig ist

1. Warte, bis der Upload komplett abgeschlossen ist.
2. Trenne währenddessen nicht das USB-Kabel.
3. Schließe den Browser nicht.
4. Nach erfolgreichem Flashen startet das Gerät in der Regel automatisch neu.
5. Falls kein automatischer Neustart erfolgt, trenne das Gerät kurz vom Strom und schließe es erneut an.

### 7. Anzeige nach dem ersten Start

Nach dem ersten Start zeigt das Display zwei wichtige Werte an:

- Chip-ID, zum Beispiel AA:BB:CC:DD:EE:FF
- Freigabecode, zum Beispiel 1234

Diese beiden Werte musst du exakt so übernehmen, wie sie auf dem Display stehen.

Für die spätere Freischaltung müssen beide Werte in genau diesem Format übermittelt werden:

AA:BB:CC:DD:EE:FF 1234

Wichtig:

- Zwischen Chip-ID und Freigabecode steht genau ein Leerzeichen.
- Die Doppelpunkte in der Chip-ID müssen erhalten bleiben.
- Bitte nichts dazuschreiben und nichts weglassen.

## Freischaltung und Spendenhinweis

Die erweiterten Funktionen dieser Software werden über einen individuellen Zugangscode freigeschaltet.

Zur Unterstützung des Projekts ist eine freiwillige Spende von 20 € vorgesehen.

### So gehst du vor

1. Öffne den PayPal-Link:

   https://www.paypal.com/ncp/payment/VSKA88HTE4ZZY

2. Trage im Nachrichtenfeld unbedingt deine Zeichenfolge in diesem Format ein:

   AA:BB:CC:DD:EE:FF 1234

3. Nur mit dieser Angabe kann dein persönlicher Zugangscode erzeugt werden.
4. Nach Eingang der Nachricht wird dein Zugangscode per E-Mail geschickt.
5. Die Zusendung kann bis zu 3 Stunden dauern.

Wenn der PayPal-Link nicht funktioniert, kannst du auch direkt per PayPal an diese Adresse senden:

MikaLoxControl@gmail.com

Auch dann muss die Zeichenfolge mit Chip-ID und Freigabecode unbedingt in die Nachricht geschrieben werden.

### Zugangscode eingeben

Sobald du deinen persönlichen Zugangscode erhalten hast:

1. Gib den Zugangscode am Gerät ein.
2. Achte auf eine korrekte Eingabe.
3. Bei korrekter Eingabe wird das Gerät dauerhaft freigeschaltet.

Hinweis: Nach jeder dritten falschen Eingabe wird die Eingabe zeitweise gesperrt. Deshalb den zugesandten Code bitte genau übernehmen.

## Hinweis

Es handelt sich nicht um einen Kaufvertrag.

Die Spende dient der Unterstützung des Projekts. Der persönliche Zugangscode wird als Dankeschön bereitgestellt.

## Hilfe bei Verbindungsproblemen

Wenn auf der Upload-Seite keine Verbindung möglich ist, prüfe diese Punkte der Reihe nach:

1. Nur Chrome oder Edge verwenden.
2. Ein anderes USB-Kabel testen.
3. Einen anderen USB-Port am PC verwenden.
4. Alle anderen Programme schließen, die den seriellen Port belegen könnten.
5. Das Gerät kurz abziehen und wieder anschließen.
6. Die Upload-Seite neu laden und erneut auf Connect klicken.
7. Falls nötig den passenden USB-Seriell-Treiber für dein System installieren.

## Danke

Mit deiner Unterstützung hilfst du, Mika Lox Control weiterzuentwickeln.
