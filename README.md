# esp32cam-easy
Optimierte ESP32CAM Firmware

Ich habe die optimierte Firmware von https://github.com/easytarget/esp32-cam-webserver mit dem WifiManager von https://github.com/tzapu/WiFiManager "verheiratet".

Installation der beiden Repos in Arduino:
Da in meiner Arduino-Bibliothek der WiFiManager von tzapu nicht auftaucht, habe ich die Zip-Datei aus seinem Repo gezogen https://github.com/tzapu/WiFiManager/archive/refs/heads/master.zip und manuell als ZIP-Datei zur Bibliothek hinzugefügt. Das war es schon.

Den optimierten ESP32CAM-Webserver habe ich ebenfalls als Zip Datei heruntergeladen. https://github.com/easytarget/esp32-cam-webserver/archive/refs/heads/master.zip Das entpackte Verzeichnis habe ich in den Arduino Sketchordner gepackt. Wichtig dabei, die Datei myconfig.sample.h in myconfig.h umzubenennen.

In der Arduino-IDE öffnen wir nun aus dem Verzeichnis "esp32-cam-webserver-master" direkt die esp32-cam-webserver.ino . So sollten alle Verknüpfungen zu den zusätzlichen Dateien nun funktionieren. Testweise kann man es mal kompilieren, ob es durchläuft. Wenn ja, den Inhalt der Datei durch meine modifizierte Version zu ersetzen. Sei es durch cut-n-paste im Editor oder einfach überschreiben. Meine Version hat zum einen dort die SSID-Geschichte rausgenommen weil es durch den WiFiManager übernommen wird. Das Rücksetzen auf Standardwerte und eigenen Accesspoint habe ich auch etwas verändert. Nun muss man einen Taster zwischen GPIO2 und Masse etwa 8-10 Sekunden direkt nach Anklemmen der Betriebsspannung drücken. So funktioniert es auch, wenn das Teil völlig verkonfiguriert ist.

Das war es schon. Da es sich nur um wenige Zeilen handelt, lohnt es sich für mich nicht, zu forken. Mein Dankeschön an easytarget und tzapu.

Infos zur Hard- und Softwareinstallation sowie Bedienung gibt es auf der Seite von easytarget: https://github.com/easytarget/esp32-cam-webserver
