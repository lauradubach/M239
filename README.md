# Dokumentation Mail-Protokolle

### Inhalt
* Definitionen
* Unterschiede
* Testfälle
* Mailserver
* Base64


### Definition SMTP
Simple Mail Transfer Protocol

Das Protokoll SMTP ist für den Austausch der E-Mails zuständig. Dieses Protokoll basiert auf dem Port 25. Er regelt nur das senden und weiterleiten von Emails vom Absender zum Empfänger.

#### Funktion

1. Wenn man eine Mail sendet, ist der Computer ein SMTP Client.
2. Der SMTP Server hingegen ist der Ausgangsserver des Mailanbieters, zunächst wird diese Mail auf den Server hochgeladen.
3. Nun kontaktiert der Server den DNS Server, der vermittelt nun einen Ziel SMTP Server.
4. Auf dem Ziel SMTP Server wird die Nachricht dann gespeichert und kann vom Empfänger IMAP oder POP3 heruntergeladen werden.

#### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/Ablauf%20SMTP.png" width="450" height="300">

### Definition POP3
Post Office Protocol

Über diesen Port werden Emails aus dem Ordner des Posteingangs vom Server heruntergeladen. Nur der Nutzer kann wählen, ob diese gelöscht werden sollten oder nicht. Wenn man sich an einem anderen Ort anmelden möchte, kann es sein, dass die Emails erneut heruntergeladen werden. Der Speicherplatz wird dadurch beansprucht. Das heisst POP3 dient nur zum simplen Download des Posteingangs. Es findet keine Synchronisierung statt zwischen dem Endgerät und Emailkonto.

#### Funktion

1. Über den Fernzugriff werden alle gespeicherten E-Mails abgerufen und auf dem lokalen Computer gespeichert.
2. Nun werden Online die E-Mails vom Posteingangserver vom E-Mail Client heruntergeladen.
3. Die eingegangenen E-Mails werden nun auf dem lokalen Computer des Benutzers ohne Verbindung bearbeitet.
4. Die Verbindung vom POP-Server und dem E-Mail-Client erfolgt über TCP auf dem Port 110.

#### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/pop3%20verfahren.png" width="450" height="300">


### Definition IMAP
Internet Message Access Protocol

#### Funktion

#### Detailierter Ablauf


### Unterschiede zwischen POP3 und IMAP

IMAP ist das modernere Protokoll. Bei IMAP wird der komplette Inhalt des Emailkontos stets mit dem Mailprogramm auf dem Computer synchronisiert. Bei POP3 findet nur der simple Download statt.  

### Testfälle

### Wie kann man seinen Mailserver herausfinden?
Wenn man zum Beispiel im Mobile Phone auf sein E-Mail geht, kann man oben rechts auf die drei Punkte klicken und dann auf die Einstellungen:

<img src="https://github.com/lauradubach/M239/blob/main/1%20Mail.png" width="350" height="500">

Unter den Einstellungen kann man nun sein gewünschtes Mailkonto auswählen und dann findet man ganz unten die Erweiterten Einstellungen:

<img src="https://github.com/lauradubach/M239/blob/main/2%20Mail.png" width="350" height="500">

Hier sieht man nun alle Infos zum Ein- und Ausgang des Mailservers.

Eingang:

<img src="https://github.com/lauradubach/M239/blob/main/3%20Mail.png" width="350" height="500">

Ausgang:

<img src="https://github.com/lauradubach/M239/blob/main/4%20Mail.png" width="350" height="500">


### Definition Base64

Dies ist eine Kodier- und Dekodiertechnik. Sie wird verwendet um binäre Daten in ein ASCII-Textformat umzuwandeln und umgehkehrt. Es wird im Allgemeinen dazu verwendet, um inhaltbasierte Nachrichten über das Internet zu übertragen.

#### Funktion

1. Zuerst unterteilt es alle drei Bits der binären Daten in sechs Bit-Einheiten.
2. Die neuen Daten werden als 64-Radix-Zahlensystem und als Sieben-Bit-ASCII-Text dargestellt.
3. Diese Daten sind nicht für Menschen lesbar.

#### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/Base64.jpg" width="450" height="300">
