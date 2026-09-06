# Mika Lox Control mit 3 Stunden Demo

Diese Anleitung beschreibt den kompletten Ablauf von der Firmware-Installation bis zur Freischaltung Schritt für Schritt.

Aktuell unterstützt das Dashboard diese Loxone-Typen: 
Switch, Dimmer, LightControllerV2, Jalousie, IRoomController, IRoomControllerV2, EFM, Meter, Pushbutton, Slider, InfoOnlyDigital, InfoOnlyAnalog, InfoOnlyText, TextState und TimedSwitch.


## Installation und Erststart

Bevor eine Freischaltung möglich ist, muss die passende Firmware auf das richtige Gerät geflasht werden. Das geht direkt über die Installer-Seite im Browser – ganz ohne manuellen Datei-Download und ohne Adresseingabe.

### 1. Was du vor dem Flashen brauchst

Vor dem Start bitte kurz prüfen:

* Ein USB-Datenkabel. Ein reines Ladekabel funktioniert nicht.
* Einen PC oder Laptop mit Google Chrome, Microsoft Edge oder Firefox (ab Version 151).
* Das Gerät muss per USB angeschlossen sein.
* Falls ein anderes Programm schon auf den USB-Port zugreift (z. B. Arduino IDE oder ein serieller Monitor), dieses vorher schließen.

### 2. Installer-Seite öffnen

1. Öffne [michi202020.github.io/Mika-Lox-Control](https://michi202020.github.io/Mika-Lox-Control/) in Chrome, Edge oder Firefox.
2. Wähle die Karte, die zu deinem Gerät passt:
   * 4848S040CIY1      
   * 4848S040CIY3      https://de.banggood.com/ESP32-S3-4_0-Inch-480+480-Smart-Display-for-Arduinos-LVGL-WiFi-Bluetooth-Development-Board-86-Box-Central-Control-Panel-LCD-TFT-Module-with-Shell-p-2029063.html?utm_source=googleshopping&utm_medium=cpc_organic&gmcCountry=DE&utm_content=minha&utm_campaign=aceng-pmax-deg-de-pc&currency=EUR&cur_warehouse=CN&createTmp=1&ID=6331253&utm_source=googleshopping&utm_medium=cpc_eu&utm_content=dcr&utm_campaign=aceng-pmax-deg-all-help-240411-copy2&ad_id=&gad_source=1&gad_campaignid=21176915915&gclid=EAIaIQobChMIpruekP_ZlgMV6ZWDBx1d0TJqEAQYBSABEgI2yPD_BwE
   * Waveshare ESP32-S3-LCD-4 (Rev4)
3. Klicke bei deinem Gerät auf **Installieren**.

Die passende Firmware wird automatisch geladen – welche Datei das ist und auf welche Adresse geflasht wird, ist bereits hinterlegt. Du musst dich um nichts davon kümmern.

### 3. USB-Gerät auswählen

Nach dem Klick auf Installieren öffnet dein Browser ein Fenster zur USB- bzw. seriellen Port-Auswahl.

1. Suche in der Liste den Eintrag für dein angeschlossenes ESP32-Gerät. Je nach System kann der Eintrag zum Beispiel so aussehen:
   * USB JTAG/serial debug unit
   * CP210x USB to UART Bridge
   * CH340
   * Silicon Labs CP210x
   * USB Serial
   * unter Linux manchmal ein Eintrag zu ttyUSB oder ttyACM
2. Wenn mehrere Einträge angezeigt werden und du unsicher bist:
   * Trenne das Gerät kurz vom USB.
   * Öffne die Auswahl erneut.
   * Schließe das Gerät wieder an.
   * Wähle den neu erschienenen Eintrag.
3. Markiere den richtigen Eintrag und klicke auf **Verbinden** bzw. **Connect**.
4. Bestätige im nächsten Schritt die Installation.

Wenn gar kein Gerät angezeigt wird, prüfe zuerst ein anderes USB-Kabel oder einen anderen USB-Port.

### 4. Warten, bis der Flash-Vorgang fertig ist

1. Warte, bis der Vorgang komplett abgeschlossen ist.
2. Trenne währenddessen nicht das USB-Kabel.
3. Schließe den Browser nicht.
4. Nach erfolgreichem Flashen startet das Gerät in der Regel automatisch neu.
5. Falls kein automatischer Neustart erfolgt, trenne das Gerät kurz vom Strom und schließe es erneut an.

### 5. Anzeige nach dem ersten Start

Nach dem ersten Start zeigt das Display zwei wichtige Werte an:

* Chip-ID, zum Beispiel `AA:BB:CC:DD:EE:FF`
* Freigabecode, zum Beispiel `1234`

Diese beiden Werte musst du exakt so übernehmen, wie sie auf dem Display stehen.

Für die spätere Freischaltung müssen beide Werte in genau diesem Format übermittelt werden:

```
AA:BB:CC:DD:EE:FF 1234
```

Wichtig:

* Zwischen Chip-ID und Freigabecode steht genau ein Leerzeichen.
* Die Doppelpunkte in der Chip-ID müssen erhalten bleiben.
* Bitte nichts dazuschreiben und nichts weglassen.

## Privates Projekt, Unterstützung und Freischaltung

Mika Lox Control ist ein privat entwickeltes DIY-/Hobbyprojekt. Es ist kein offizielles Produkt von Loxone, steht in keiner Verbindung zu Loxone und umfasst keinen offiziellen Loxone-Support. Hinter dem Projekt steht keine als Anbieter auftretende Firma. Die Entwicklung erfolgte über einen Zeitraum von etwa 1,5 Jahren und wird privat fortgeführt.

Du kannst frei entscheiden, ob du das Projekt unterstützen und eine Freischaltung anfordern möchtest. Wichtig: Für die Nutzung des Geräts ist ein individueller Zugangscode erforderlich. Dieser Zugangscode wird nach einer Zahlung von **20 €** bereitgestellt. Ohne diese Zahlung erhältst du keinen Zugangscode und das Gerät bleibt im Demo für 3h und anschließend nicht nutzbar. Die Zahlung ist daher Voraussetzung für die Freischaltung und wird hier nicht als bloße „Spende“ bezeichnet.

Diese Beschreibung soll den Ablauf transparent erklären. Sie trifft keine verbindliche Aussage darüber, wie das Projekt oder die Zahlung steuerlich, gewerblich oder rechtlich einzuordnen ist, und ersetzt keine Rechtsberatung.

### So gehst du vor

1. Öffne den PayPal-Link: [paypal.com/ncp/payment/VSKA88HTE4ZZY](https://www.paypal.com/ncp/payment/VSKA88HTE4ZZY)
2. Trage im Nachrichtenfeld unbedingt deine Zeichenfolge in diesem Format ein:

   ```
   AA:BB:CC:DD:EE:FF 1234
   ```

3. Nur mit dieser Angabe kann dein persönlicher Zugangscode erzeugt werden.
4. Nach Eingang der Zahlung und der erforderlichen Angaben wird dein Zugangscode per E-Mail geschickt.
5. Die Zusendung kann bis zu 3 Stunden dauern.

Wenn der PayPal-Link nicht funktioniert, kannst du auch direkt per PayPal an diese Adresse zahlen: [MikaLoxControl@gmail.com](mailto:MikaLoxControl@gmail.com)

Auch dann muss die Zeichenfolge mit Chip-ID und Freigabecode unbedingt in die Nachricht geschrieben werden.

### Zugangscode eingeben

Sobald du deinen persönlichen Zugangscode erhalten hast:

1. Gib den Zugangscode am Gerät ein.
2. Achte auf eine korrekte Eingabe.
3. Bei korrekter Eingabe wird das Gerät dauerhaft freigeschaltet.

Hinweis: Nach jeder dritten falschen Eingabe wird die Eingabe zeitweise gesperrt. Deshalb den zugesandten Code bitte genau übernehmen.

## Hilfe bei Verbindungsproblemen

Wenn auf der Installer-Seite keine Verbindung möglich ist, prüfe diese Punkte der Reihe nach:

1. Nur Chrome, Edge oder Firefox (ab Version 151) verwenden.
2. Ein anderes USB-Kabel testen.
3. Einen anderen USB-Port am PC verwenden.
4. Alle anderen Programme schließen, die den seriellen Port belegen könnten.
5. Das Gerät kurz abziehen und wieder anschließen.
6. Die Installer-Seite neu laden und erneut auf Installieren klicken.
7. Falls nötig den passenden USB-Seriell-Treiber für dein System installieren.

## Alternative: manueller Download

Falls die Installer-Seite bei dir aus irgendeinem Grund nicht funktioniert, findest du die Firmware-Dateien auch direkt in den [GitHub Releases](https://github.com/Michi202020/Mika-Lox-Control/releases/) zum manuellen Flashen mit einem eigenen Tool. Nutze dabei die zu deinem Gerät passende FULL-Datei und flashe sie auf Adresse `0x0000`:

* `Mika-Lox-Control-4848S040CIY1-FULL.bin`
* `Mika-Lox-Control-4848S040CIY3-FULL.bin`
* `Mika-Lox-Control-waveshare-s3-lcd40-rev4-FULL.bin`

## Videos

Kurze Videos zu den wichtigsten Themen – einfach das passende auswählen:

### Werbevideo

Ein kurzer Überblick über Mika Lox Control.

https://github.com/user-attachments/assets/3e19dfe8-a0e1-4b31-98ce-e44bf2a4b9de

### Ersteinrichtung

Zeigt Schritt für Schritt, wie du dein Gerät flashst und aktivierst.



https://github.com/user-attachments/assets/63472106-8f14-49d5-83aa-8facc78d70aa



### Bedienung

Zeigt, wie du Mika Lox Control im Alltag bedienst.

https://github.com/user-attachments/assets/4dc782e3-94d2-4d89-9e53-3214a69f453b

## Tutorial Material / Anwendungsvideos

1. Dashboard ändern und Kacheln belegen : https://youtu.be/upHhYXxaVIo
2. Firmware Update : https://youtu.be/nbM5DjN6LQg
3. Einstellung Setup Übersicht : https://youtu.be/3EHh_ZeNYxY
4. Lichtsteuerung : https://youtu.be/WQmvKWAQJFg


## Danke

Mit deiner Unterstützung hilfst du, Mika Lox Control weiterzuentwickeln.
