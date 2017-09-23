# SSH für Docker

# Benutzer und Schlüssel hinterlegen

Im Verzeichnis ``/etc/authorized_keys`` müssen die Keys für jeden Benutzer in jeweils einer Datei hinterlegt werden.
Der Dateiname wird dabei als Benutzername verwendet und beim Starten des Containers automatisch angelegt. Der Pfad
``/etc/authorized_keys`` sollte in einen eigenen Docker-Volume legen.

## Beispiel

Für den Benutzer ``foobar`` werden die Public-Keys in der Datei ``/etc/authorized_keys/foobar`` hinterlegt.

# Credits

Die Idee für dieses Image ist beim Docker-Image von https://github.com/panubo/docker-sshd 
