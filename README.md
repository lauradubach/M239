# Dokumentation Mail-Protokolle

### Inhalt
* Definitionen
* Ablauf
* Unterschiede
* Mailserver
* Base64

### Definition SMTP
Simple Mail Transfer Protocol

Das Protokoll SMTP ist für den Austausch der E-Mails zuständig. Dieses Protokoll basiert auf dem Port 25. Er regelt nur das senden und weiterleiten von Emails vom Absender zum Empfänger.

##### Funktion

1. Wenn man eine Mail sendet, ist der Computer ein SMTP Client.
2.	Der SMTP Server hingegen ist der Ausgangsserver des Mailanbieters, zunächst wird diese Mail auf den Server hochgeladen.
3.	Nun kontaktiert der Server den DNS Server, der vermittelt nun einen Ziel SMTP Server.
4.	Auf dem Ziel SMTP Server wird die Nachricht dann gespeichert und kann vom Empfänger IMAP oder POP3 heruntergeladen werden.

##### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/Ablauf%20SMTP.png" width="500" height="350">

### Definition POP3

### Definition IMAP

### Ablauf SMTP

### Ablauf POP3

### Ablauf IMAP

### Unterschiede zwischen POP3 und IMAP

### Mailserver

### Base64
