Готово, Сергей!
Вот идеально оформленный markdown-файл (.md) — полностью совместимый с GitHub, со списками, таблицами и кодовыми блоками.
Можно копировать как есть в html-and-the-web.md.

⸻

🌐 HTML and the Web — Meine Notizen

⭐ Wie funktioniert das Web?

Das Web besteht aus vielen Computern, die über das Internet miteinander kommunizieren.
Wenn man eine Website öffnet, passiert Folgendes:
	1.	Der Browser bekommt eine URL.
	2.	DNS übersetzt den Domainnamen in eine IP-Adresse.
	3.	Der Browser verbindet sich über TCP/HTTPS mit dem Server.
	4.	Der Browser sendet eine HTTP-GET-Anfrage.
	5.	Der Server antwortet mit HTML, CSS, Bildern und weiteren Dateien.
	6.	Der Browser rendert die Seite und zeigt sie an.
	7.	Falls nötig, lädt der Browser später zusätzliche Daten (GET/POST).

⸻

⭐ Wichtige Begriffe

Begriff	Bedeutung
Client	Gerät, das eine Website anfragt (Laptop, Handy).
Server	Computer, der Anfragen beantwortet und Daten liefert.
DNS	System, das Domainnamen in IP-Adressen umwandelt.
HTTP / HTTPS	Protokolle zur Kommunikation zwischen Browser und Server.
URL	Adresse einer Website.
IP-Adresse	Technische Adresse eines Servers im Netzwerk.


⸻

⭐ HTML Basics

HTML (HyperText Markup Language) dient zur Strukturierung von Webseiten.

Ein typisches HTML-Element besteht aus:
	•	öffnendem Tag
	•	Inhalt
	•	schließendem Tag

Beispiel:

<h1>Hello World</h1>


⸻

⭐ Wichtige HTML-Elemente

Element	Bedeutung
<h1>	Hauptüberschrift (nur einmal pro Seite).
<h2>	Unterüberschrift.
<p>	Absatz.
<a>	Link.
<img>	Bild (selbstschließend).
<ul> / <ol>	Listen.
<li>	Listenelement.
<form>	Formular.
<input>	Eingabefeld.
<button>	Button.


⸻

⭐ Semantisches HTML

Semantische Tags beschreiben die Bedeutung des Inhalts.
Sie verbessern:
	•	Lesbarkeit für Entwickler
	•	SEO
	•	Barrierefreiheit (Screenreader)

Wichtige semantische Elemente

Element	Bedeutung
<header>	Kopfbereich einer Seite oder eines Abschnitts.
<nav>	Navigation / Menü.
<main>	Hauptinhalt.
<section>	Abschnitt.
<article>	eigenständiger Artikel (z. B. Blogpost).
<aside>	Zusatzinfos / Sidebar.
<footer>	Fußbereich.


⸻

⭐ Aufbau einer HTML-Datei

<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Meine Website</title>
  </head>
  <body>
    <h1>Hallo Welt</h1>
  </body>
</html>

	•	head → Meta-Informationen, CSS, Titel
	•	body → Inhalt der Seite

⸻

⭐ Wie Browser HTML rendern
	1.	HTML wird geladen → DOM entsteht
	2.	CSS wird geladen → Render Tree entsteht
	3.	Layout: Browser positioniert Elemente
	4.	Paint: Browser zeichnet die Seite
	5.	JavaScript macht die Seite interaktiv

⸻

⭐ Meine Learnings
	•	Ich verstehe jetzt die Client–Server-Kommunikation.
	•	Ich weiß, wie DNS, HTTP und IP-Adressen funktionieren.
	•	Ich kann HTML-Strukturen erstellen und lesen.
	•	Ich kenne semantische HTML-Elemente und ihren Nutzen.
	•	Der Aufbau einer Webseite mit <head> und <body> ist klar.
	•	Ich weiß, wie der Browser HTML rendert.
