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
Das Internet Message Access Protocol (IMAP) ist ein Netzwerkprotokoll, welcher sich um die Online-Verwaltung von E-Mails auf Servern kümmert. Es erlaubt die Synchronisation des lokalen Clients mit dem Postfach vom Server. Mit dem Protokoll IMAP stehen Client und Server ständig in Verbindung. Solange auf dem Server die Mails nicht gelöscht werden, kann auf diese zugegriffen werden während einer IMAP-Sitzung. Durch das können auch Endgeräte mit schlechtem Internet  auf den Server zugreifen.

#### Funktion
1. Zuerst wird die Verbindung zwischen Client und Server hergestellt über TCP.
2. Da der Client bei IMAP keine Antwort auf Kommandos abwartet, kann er mehrere Befehle hintereinander senden.
3. Damit der Client dann später bei einer Rückmeldung weiss, dass es vom diesem Server kommt, schickt der Client eine Kennung mit, die der Server dann in seiner Antwort zurück schickt.
4. Wenn der Server in der Antwort ein Zeichen am Anfang der Zeile sendet, heisst das, dass der Server noch auf mehr Infos vom Befehl des Clients wartet.
5. Schlussendlich ist dann in der Antwort entweder ein «OK», «NO» oder «BAD» gekennzeichnet, welches informiert ob die Mission ein Erfolg war oder nicht oder ob es einen Syntax-fehler gibt.

#### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/IMAP.jpg" width="500" height="300">


### Unterschiede zwischen POP3 und IMAP

IMAP ist das modernere Protokoll. Bei IMAP wird der komplette Inhalt des Emailkontos stets mit dem Mailprogramm auf dem Computer synchronisiert. Bei POP3 findet nur der simple Download statt.  

### SMTP Testfall

Zuerst startet man eine telnet Verbindung auf einen Server:

<img src="https://github.com/lauradubach/M239/blob/main/1%20SMTP.png" width="500" height="300">


Wenn dieser sich verbindet kann man nun eine folgende Zeile sehen und dort Sachen eingeben:

<img src="https://github.com/lauradubach/M239/blob/main/2%20SMTP.png" width="500" height="300">


Wenn man dann auf Wireshark geht kann man auf SMTP filtern und der Verkehr wird angezeigt:

<img src="https://github.com/lauradubach/M239/blob/main/3%20SMTP.png" width="600" height="250">


Man kann diesen auch folgen und sieht dann was man alles eingegeben hat:

<img src="https://github.com/lauradubach/M239/blob/main/4%20SMTP.png" width="500" height="300">

### Wie kann man seinen Mailserver herausfinden?
Wenn man zum Beispiel im Mobile Phone auf sein E-Mail geht, kann man oben rechts auf die drei Punkte klicken und dann auf die Einstellungen:

<img src="https://github.com/lauradubach/M239/blob/main/1%20Mail.png" width="350" height="500">

Unter den Einstellungen kann man nun sein gewünschtes Mailkonto auswählen und dann findet man ganz unten die Erweiterten Einstellungen:

<img src="https://github.com/lauradubach/M239/blob/main/2%20Mail.png" width="350" height="700">

Hier sieht man nun alle Infos zum Ein- und Ausgang des Mailservers.

Eingang:

<img src="https://github.com/lauradubach/M239/blob/main/3%20Mail.png" width="350" height="700">

Ausgang:

<img src="https://github.com/lauradubach/M239/blob/main/4%20Mail.png" width="350" height="700">


### Definition Base64

Dies ist eine Kodier- und Dekodiertechnik. Sie wird verwendet um binäre Daten in ein ASCII-Textformat umzuwandeln und umgehkehrt. Es wird im Allgemeinen dazu verwendet, um inhaltbasierte Nachrichten über das Internet zu übertragen.

#### Funktion

1. Zuerst unterteilt es alle drei Bits der binären Daten in sechs Bit-Einheiten.
2. Die neuen Daten werden als 64-Radix-Zahlensystem und als Sieben-Bit-ASCII-Text dargestellt.
3. Diese Daten sind nicht für Menschen lesbar.

#### Detailierter Ablauf

<img src="https://github.com/lauradubach/M239/blob/main/Base64.jpg" width="450" height="300">
