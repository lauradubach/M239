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
2.	Der SMTP Server hingegen ist der Ausgangsserver des Mailanbieters, zunächst wird diese Mail auf den Server hochgeladen.
3.	Nun kontaktiert der Server den DNS Server, der vermittelt nun einen Ziel SMTP Server.
4.	Auf dem Ziel SMTP Server wird die Nachricht dann gespeichert und kann vom Empfänger IMAP oder POP3 heruntergeladen werden.

#### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/Ablauf%20SMTP.png" width="450" height="300">

### Definition POP3
Post Office Protocol

Über diesen Port werden Emails aus dem Ordner des Posteingangs vom Server heruntergeladen. Nur der Nutzer kann wählen, ob diese gelöscht werden sollten oder nicht. Wenn man sich an einem anderen Ort anmelden möchte, kann es sein, dass die Emails erneut heruntergeladen werden. Der Speicherplatz wird dadurch beansprucht. Das heisst POP3 dient nur zum simplen Download des Posteingangs. Es findet keine Synchronisierung statt zwischen dem Endgerät und Emailkonto.

#### Funktion

#### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/pop3%20verfahren.png" width="450" height="300">


### Definition IMAP
Internet Message Access Protocol

#### Funktion

#### Detailierter Ablauf


### Unterschiede zwischen POP3 und IMAP

IMAP ist das modernere Protokoll. Bei IMAP wird der komplette Inhalt des Emailkontos stets mit dem Mailprogramm auf dem Computer synchronisiert. Bei POP3 findet nur der simple Download statt.  


### Testfälle

### Mailserver

### Base64
