<h1>🌐 HTML and the Web — Meine Notizen</h1>

<h2>⭐ Wie funktioniert das Web?</h2>
<p>Das Web besteht aus vielen Computern, die über das Internet miteinander kommunizieren. Wenn man eine Website öffnet, passiert Folgendes:</p>

<ol>
  <li>Der Browser bekommt eine <strong>URL</strong>.</li>
  <li><strong>DNS</strong> übersetzt den Domainnamen in eine IP-Adresse.</li>
  <li>Der Browser verbindet sich über <strong>TCP/HTTPS</strong> mit dem Server.</li>
  <li>Der Browser sendet eine <strong>HTTP-GET-Anfrage</strong>.</li>
  <li>Der Server antwortet mit <strong>HTML</strong>, CSS, Bildern und weiteren Dateien.</li>
  <li>Der Browser rendert die Seite und zeigt sie an.</li>
  <li>Falls nötig, lädt der Browser später zusätzliche Daten (GET/POST).</li>
</ol>

<hr />

<h2>⭐ Wichtige Begriffe</h2>

<table>
  <tr>
    <th>Begriff</th>
    <th>Bedeutung</th>
  </tr>
  <tr>
    <td><strong>Client</strong></td>
    <td>Gerät, das eine Website anfragt (Laptop, Handy).</td>
  </tr>
  <tr>
    <td><strong>Server</strong></td>
    <td>Computer, der Anfragen beantwortet und Daten liefert.</td>
  </tr>
  <tr>
    <td><strong>DNS</strong></td>
    <td>System, das Domainnamen in IP-Adressen umwandelt.</td>
  </tr>
  <tr>
    <td><strong>HTTP / HTTPS</strong></td>
    <td>Protokolle zur Kommunikation zwischen Browser und Server.</td>
  </tr>
  <tr>
    <td><strong>URL</strong></td>
    <td>Adresse einer Website.</td>
  </tr>
  <tr>
    <td><strong>IP-Adresse</strong></td>
    <td>Technische Adresse eines Servers im Netzwerk.</td>
  </tr>
</table>

<hr />

<h2>⭐ HTML Basics</h2>

<p>HTML (Hypertext Markup Language) dient zur Strukturierung von Webseiten.</p>
<p>Ein typisches HTML-Element besteht aus:</p>

<ul>
  <li>öffnendem Tag</li>
  <li>Inhalt</li>
  <li>schließendem Tag</li>
</ul>

<p>Beispiel:</p>

<pre><code>&lt;h1&gt;Hello World&lt;/h1&gt;</code></pre>

<hr />

<h2>⭐ Wichtige HTML-Elemente</h2>

<table>
  <tr>
    <th>Element</th>
    <th>Bedeutung</th>
  </tr>
  <tr><td>&lt;h1&gt;</td><td>Hauptüberschrift (nur einmal pro Seite)</td></tr>
  <tr><td>&lt;h2&gt;</td><td>Unterüberschrift</td></tr>
  <tr><td>&lt;p&gt;</td><td>Absatz</td></tr>
  <tr><td>&lt;a&gt;</td><td>Link</td></tr>
  <tr><td>&lt;img&gt;</td><td>Bild (selbstschließend)</td></tr>
  <tr><td>&lt;ul&gt; / &lt;ol&gt;</td><td>Listen</td></tr>
  <tr><td>&lt;li&gt;</td><td>Listenelement</td></tr>
  <tr><td>&lt;form&gt;</td><td>Formular</td></tr>
  <tr><td>&lt;input&gt;</td><td>Eingabefeld</td></tr>
  <tr><td>&lt;button&gt;</td><td>Button</td></tr>
</table>

<hr />

<h2>⭐ Semantisches HTML</h2>

<p>Semantische Tags beschreiben die Bedeutung des Inhalts und verbessern:</p>

<ul>
  <li>Lesbarkeit für Entwickler</li>
  <li>SEO</li>
  <li>Barrierefreiheit (Screenreader)</li>
</ul>

<h3>Wichtige semantische Elemente</h3>

<table>
  <tr>
    <th>Element</th>
    <th>Bedeutung</th>
  </tr>
  <tr><td>&lt;header&gt;</td><td>Kopfbereich einer Seite oder eines Abschnitts</td></tr>
  <tr><td>&lt;nav&gt;</td><td>Navigation / Menü</td></tr>
  <tr><td>&lt;main&gt;</td><td>Hauptinhalt</td></tr>
  <tr><td>&lt;section&gt;</td><td>Abschnitt</td></tr>
  <tr><td>&lt;article&gt;</td><td>Eigenständiger Artikel</td></tr>
  <tr><td>&lt;aside&gt;</td><td>Sidebar / Zusatzinfos</td></tr>
  <tr><td>&lt;footer&gt;</td><td>Fußbereich</td></tr>
</table>

<hr />

<h2>⭐ Aufbau einer HTML-Datei</h2>

<pre><code>&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;meta charset="UTF-8" /&gt;
    &lt;title&gt;Meine Website&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Hallo Welt&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</code></pre>

<hr />

<h2>⭐ Wie Browser HTML rendern</h2>

<ol>
  <li>Browser lädt HTML → DOM entsteht</li>
  <li>Browser lädt CSS → Render Tree entsteht</li>
  <li>Layout: Elemente werden positioniert</li>
  <li>Paint: Seite wird gezeichnet</li>
  <li>JavaScript macht die Seite interaktiv</li>
</ol>

<hr />

<h2>⭐ Meine Learnings</h2>

<ul>
  <li>Ich verstehe Client–Server-Kommunikation.</li>
  <li>Ich weiß, wie DNS, HTTP und IP-Adressen funktionieren.</li>
  <li>Ich kann HTML-Strukturen erstellen und lesen.</li>
  <li>Ich kenne wichtige semantische HTML-Elemente.</li>
  <li>Ich verstehe den Aufbau einer typischen Webseite.</li>
  <li>Ich weiß, wie Browser HTML rendern.</li>
</ul>
