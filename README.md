# SSH für Docker

## Benutzer und Schlüssel hinterlegen

Im Verzeichnis ``/run/secrets`` müssen die Keys für jeden Benutzer in jeweils einer Datei hinterlegt werden. Der
Dateiname muss benutzername.pub für Public Keys und benutzername.password für Passwörter lauten. Der Dateiname
(ohne Dateierweiterung) wird als Benutzername verwendet und beim Starten des Containers automatisch angelegt.

In den Dateien *.pub sind mehrere ``Public Keys`` möglich, das Format entspricht den authorized_keys die sich sonst im
Benutzerverzeichnis befinden.

Der Pfad ``/run/secrets`` kann ein Volume sein, falls nicht die ``Rancher Secrets``  verwendet werden.

### Beispiel

Für den Benutzer ``foobar.pub`` werden die Public-Keys in der Datei ``/run/secrets/foobar.pub`` hinterlegt.


## Credits

Die Idee für dieses Image stammt von https://github.com/panubo/docker-sshd. 
