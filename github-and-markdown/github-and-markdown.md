<h2>⭐ Git Branches and Pull Requests (PRs)</h2>

<p>Branches und Pull Requests sind essenzielle Werkzeuge für die Zusammenarbeit im Team und für saubere Code-Strukturen.</p>

<h3>🔹 Was ist ein Branch?</h3>
<p>Ein <strong>Branch</strong> ist eine unabhängige Entwicklungsumgebung innerhalb eines Git-Repositories.  
Er ermöglicht es, neue Features oder Bugfixes zu entwickeln, ohne den Hauptcode (main/master) zu beeinflussen.</p>

<h4>Wichtige Befehle:</h4>

<table>
  <tr>
    <th>Befehl</th>
    <th>Bedeutung</th>
  </tr>
  <tr><td><code>git branch</code></td><td>zeigt alle lokalen Branches</td></tr>
  <tr><td><code>git branch &lt;name&gt;</code></td><td>erstellt einen neuen Branch</td></tr>
  <tr><td><code>git checkout &lt;name&gt;</code></td><td>wechselt zu einem Branch</td></tr>
  <tr><td><code>git checkout -b &lt;name&gt;</code></td><td>erstellt und wechselt zu einem neuen Branch</td></tr>
  <tr><td><code>git merge &lt;name&gt;</code></td><td>führt einen Branch in den aktuellen Branch zusammen</td></tr>
</table>

<h3>🔹 Warum Branches benutzen?</h3>
<ul>
  <li>Gleichzeitige Arbeit mehrerer Entwickler ohne Konflikte</li>
  <li>Saubere Trennung von Features</li>
  <li>Verhindert Fehler im Hauptbranch</li>
  <li>Erlaubt Experimente ohne Risiko</li>
</ul>

<hr />

<h3>⭐ Was ist ein Pull Request (PR)?</h3>
<p>Ein <strong>Pull Request</strong> ist eine Anfrage, um Änderungen aus einem Branch in einen anderen (meist <code>main</code>) zu übernehmen.</p>

<p>PRs werden meist auf GitHub, GitLab oder Bitbucket erstellt.</p>

<h4>Ein PR wird verwendet, um:</h4>
<ul>
  <li>Code-Änderungen zu vergleichen</li>
  <li>Code Reviews im Team zu ermöglichen</li>
  <li>Tests automatisch auszuführen</li>
  <li>Konflikte zu erkennen, bevor gemergt wird</li>
</ul>

<h4>Typischer Ablauf eines Pull Requests:</h4>
<ol>
  <li>Neuen Branch erstellen: <code>git checkout -b feature-login</code></li>
  <li>Änderungen machen und committen</li>
  <li>Branch hochladen: <code>git push -u origin feature-login</code></li>
  <li>Auf GitHub einen Pull Request erstellen</li>
  <li>Review durch andere Entwickler</li>
  <li>Merge in <code>main</code></li>
</ol>

<p><strong>Vorteile von PRs:</strong></p>
<ul>
  <li>Bessere Codequalität dank Reviews</li>
  <li>Dokumentation der Änderungen</li>
  <li>Transparenz im Team</li>
  <li>Saubere Versionskontrolle</li>
</ul>

<hr />