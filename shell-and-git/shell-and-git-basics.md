
<h1>🐚 Shell and Git Basics — Meine Notizen</h1>

<h2>⭐ Was ist die Shell?</h2>
<p>Die Shell ist ein textbasiertes Interface, mit dem man direkt mit dem Betriebssystem arbeitet.  
Mit der Shell kann man:</p>

<ul>
  <li>Dateien und Ordner anlegen</li>
  <li>im Dateisystem navigieren</li>
  <li>Programme starten</li>
  <li>Prozesse steuern</li>
</ul>

<h3>Wichtige Shell-Befehle</h3>

<table>
  <tr>
    <th>Befehl</th>
    <th>Bedeutung</th>
  </tr>
  <tr><td><code>ls</code></td><td>zeigt den Inhalt des aktuellen Ordners</td></tr>
  <tr><td><code>ls -la</code></td><td>zeigt alle Dateien inkl. versteckter Dateien</td></tr>
  <tr><td><code>cd &lt;Ordner&gt;</code></td><td>in einen Ordner wechseln</td></tr>
  <tr><td><code>cd ..</code></td><td>eine Ebene zurück</td></tr>
  <tr><td><code>cd ~</code></td><td>ins Home-Verzeichnis</td></tr>
  <tr><td><code>pwd</code></td><td>zeigt den aktuellen Pfad</td></tr>
  <tr><td><code>mkdir &lt;name&gt;</code></td><td>erstellt einen neuen Ordner</td></tr>
  <tr><td><code>touch &lt;datei&gt;</code></td><td>erstellt eine neue Datei</td></tr>
  <tr><td><code>rm &lt;datei&gt;</code></td><td>löscht eine Datei</td></tr>
  <tr><td><code>mv &lt;alt&gt; &lt;neu&gt;</code></td><td>verschiebt oder umbenennt Dateien/Ordner</td></tr>
</table>

<hr />

<h2>⭐ Was ist Git?</h2>
<p>Git ist ein Versionskontrollsystem. Damit kann man:</p>

<ul>
  <li>Änderungen speichern</li>
  <li>frühere Versionen wiederherstellen</li>
  <li>Code online teilen (z. B. über GitHub)</li>
  <li>in Teams zusammenarbeiten</li>
</ul>

<h3>Wichtige Git-Befehle</h3>

<table>
  <tr>
    <th>Befehl</th>
    <th>Bedeutung</th>
  </tr>
  <tr><td><code>git init</code></td><td>erstellt ein neues Repository</td></tr>
  <tr><td><code>git status</code></td><td>zeigt den aktuellen Status</td></tr>
  <tr><td><code>git add .</code></td><td>alle Änderungen zum Commit vormerken</td></tr>
  <tr><td><code>git add &lt;Datei&gt;</code></td><td>eine bestimmte Datei vormerken</td></tr>
  <tr><td><code>git commit -m "Nachricht"</code></td><td>einen Commit erstellen</td></tr>
  <tr><td><code>git remote add origin &lt;SSH-Link&gt;</code></td><td>Remote-Repository verbinden</td></tr>
  <tr><td><code>git push -u origin main</code></td><td>erster Push zum Remote-Repo</td></tr>
  <tr><td><code>git push</code></td><td>weitere Änderungen hochladen</td></tr>
  <tr><td><code>git pull</code></td><td>Änderungen vom Server holen</td></tr>
</table>

<hr />

<h2>⭐ Wie erstelle ich ein Remote Repository?</h2>

<ol>
  <li>Projektordner öffnen</li>
  <li><code>git init</code> ausführen</li>
  <li>Dateien hinzufügen: <code>git add .</code></li>
  <li>Commit machen: <code>git commit -m "initial commit"</code></li>
  <li>Auf GitHub ein neues Repository erstellen</li>
  <li>SSH-Link kopieren</li>
  <li>Verbinden: <code>git remote add origin &lt;link&gt;</code></li>
  <li>Hochladen: <code>git push -u origin main</code></li>
</ol>

<hr />

<h2>⭐ Meine Learnings</h2>

<ul>
  <li>Die Shell spart Zeit und ist sehr flexibel.</li>
  <li>Git schützt meinen Fortschritt und sichert meine Projekte.</li>
  <li>Die wichtigsten Befehle sind: <code>add</code>, <code>commit</code>, <code>push</code>.</li>
  <li>Ich kann jetzt eigene Repositories erstellen und online teilen.</li>
</ul>
