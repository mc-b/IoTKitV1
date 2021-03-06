HTTP (Hypertext Transfer Protocol)
----------------------------------

**Anfrage:**

	GET /infotext.html HTTP/1.1
	Host: www.example.net

**Antwort:**

	HTTP/1.1 200 OK
	Server: Apache/1.3.29 (Unix) PHP/4.3.4
	Content-Length: 123456 (Größe von infotext.html in Byte)
	Content-Language: de (nach RFC 3282 sowie RFC 1766)
	Connection: close
	Content-Type: text/html
	
	<Nachrichtenrumpf>

<p style="font-size: 0.5em">Beispiel HTTP Kommunikation</p>

- - - 

Das Hypertext Transfer Protocol (HTTP, englisch für Hypertext-Übertragungsprotokoll) ist ein **Protokoll zur Übertragung von Nachrichten und Daten**. Es wird hauptsächlich eingesetzt, um Webseiten (Hypertext-Dokumente) aus dem World Wide Web (WWW) in einen Webbrowser zu laden. Es ist jedoch nicht prinzipiell darauf beschränkt und auch als allgemeines Dateiübertragungsprotokoll sehr verbreitet.

Jede Nachricht besteht dabei aus zwei Teilen, dem [Nachrichtenkopf (englisch Message Header, kurz: Header oder auch HTTP-Header genannt)](http://de.wikipedia.org/wiki/Liste_der_HTTP-Headerfelder) und dem Nachrichtenrumpf (englisch Message Body, kurz: Body). Der Nachrichtenkopf enthält die **Anfragemethode** und Informationen über den Nachrichtenrumpf wie etwa verwendete Kodierungen oder den Inhaltstyp. Der Nachrichtenrumpf enthält die Nutzdaten (siehe HTML unten).

Von den Nachrichten gibt es zwei unterschiedliche Arten: die Anfrage (englisch Request) vom **Client an den Server** und die Antwort (englisch Response) als Reaktion darauf vom **Server zum Client**. Die mbed Board&#039;s können als HTTP Client oder als HTTP Server Eingesetzt werden.

#### HTTP-Anfragemethoden (nicht abschliessend) 

*   **GET**: ist die gebräuchlichste Methode. Mit ihr wird eine Ressource (zum Beispiel eine HTML Datei) vom Server angefordert.
*   **POST**: schickt Daten zur weiteren Verarbeitung zum Server.
*   **PUT**: dient dazu eine Ressource (zum Beispiel eine Datei) auf einen Webserver hochzuladen.
*   **DELETE**: löscht die angegebene Ressource auf dem Server.

Heute ist **PUT**, ebenso wie **DELETE**, kaum implementiert. Beides erlangt jedoch mit dem [REST Programmierparadigma](http://de.wikipedia.org/wiki/Representational_State_Transfer) neue Bedeutung.

### Anwendungen 

*   Holen, Schreiben und Löschen von Daten und Dateien auf HTTP Servern.

### HTML (Nachrichtenrumpf)

Die Hypertext Markup Language (engl. für Hypertext-Auszeichnungssprache), abgekürzt HTML, ist eine textbasierte [maschinenlesbare Sprache (markup language)](http://de.wikipedia.org/wiki/Auszeichnungssprache) zur Strukturierung digitaler Dokumente wie Texte mit Hyperlinks, Bildern und anderen Inhalten.

HTML-Dokumente sind die Grundlage des World Wide Web und werden von Webbrowsern dargestellt.

### Beispiel HTML Dokument {#beispiel-html-dokument}

	<!DOCTYPE html>
	<html>
	<head>
	<meta charset="UTF-8">
	<title>Simple Web-App</title>
	</head>
	<body>
	<form>
	    <h3>Klassik Web-App</h3>
	       <input type="submit" formmethod="get" formaction="http://192.168.178.63/rpc/led1/write 1" value="LED1 On">
	       <input type="submit" formmethod="get" formaction="http://192.168.178.63/rpc/led1/write 0" value="LED1 Off"><br>
	       <input type="submit" formmethod="get" formaction="http://192.168.178.63/rpc/led2/write 1" value="LED2 On">
	       <input type="submit" formmethod="get" formaction="http://192.168.178.63/rpc/led2/write 0" value="LED2 Off">
	</form>
	</body>
	</html>    
   