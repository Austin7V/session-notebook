<h1>CSS Grundlagen</h1>

<div>
  <h2>1. Was ist CSS und wofür braucht man es?</h2>

  <p>
    <strong>CSS (Cascading Style Sheets)</strong> ist eine Stylesheet-Sprache, die das Aussehen und Layout einer Webseite bestimmt.
    Während HTML für die Struktur der Inhalte verantwortlich ist, sorgt CSS dafür, wie diese Inhalte visuell dargestellt werden.
  </p>

  <h3>Warum braucht man CSS?</h3>
  <ul>
    <li>Farben, Schriftgrößen und Typografie festlegen</li>
    <li>Abstände, Ränder und Layouts gestalten</li>
    <li>Elemente positionieren (z. B. Flexbox, Grid)</li>
    <li>Animationen und Übergänge erstellen</li>
    <li>Responsives Design für verschiedene Geräte</li>
  </ul>
</div>

<div>
  <h2>2. CSS Syntax</h2>

  <p>Die CSS-Syntax besteht aus einem Selektor, einer Eigenschaft und einem Wert.</p>

  <pre>
selektor {
  property: value;
}
  </pre>

  <h3>Beispiel:</h3>
  <pre>
p {
  color: red;
  font-size: 18px;
}
  </pre>

  <p>Dieses Beispiel verändert die Farbe und Schriftgröße aller <code>&lt;p&gt;</code>-Elemente.</p>
</div>

<div>
  <h2>3. Selektortypen</h2>

  <h3>Grundlegende Selektoren:</h3>
  <ul>
    <li>
      <strong>Typselektor</strong><br />
      <code>p { color: blue; }</code>
    </li>

    <li>
      <strong>Klassenselektor</strong><br />
      <code>.button { padding: 10px; }</code>
    </li>

    <li>
      <strong>ID-Selektor</strong><br />
      <code>#header { background: black; }</code>
    </li>

    <li>
      <strong>Universalselektor *</strong><br />
      <code>* { margin: 0; }</code>
    </li>

    <li>
      <strong>Attributselektor</strong><br />
      <code>input[type="text"] { border: 1px solid gray; }</code>
    </li>
  </ul>

  <h3>Kombinierte Selektoren:</h3>
  <ul>
    <li>
      <strong>Nachfahre (Descendant)</strong><br />
      <code>div p { color: green; }</code>
    </li>

    <li>
      <strong>Kindselektor</strong><br />
      <code>ul &gt; li { margin: 5px; }</code>
    </li>

    <li>
      <strong>Adjacent Sibling</strong><br />
      <code>h2 + p { font-style: italic; }</code>
    </li>
  </ul>
</div>

<div>
  <h2>4. Spezifität</h2>

  <p>
    Die Spezifität bestimmt, welche CSS-Regel angewendet wird, wenn mehrere Regeln auf dasselbe Element zutreffen.
  </p>

  <h3>Priorität (von niedrig nach hoch):</h3>
  <ol>
    <li>Tag-Selektor (z. B. <code>div</code>)</li>
    <li>Klassenselektor (z. B. <code>.container</code>)</li>
    <li>ID-Selektor (z. B. <code>#main</code>)</li>
    <li>Inline-Style (z. B. <code>&lt;p style="color:red"&gt;</code>)</li>
    <li><strong>!important</strong> (höchste Priorität – nur im Notfall)</li>
  </ol>

  <h3>Beispiel:</h3>
  <pre>
p { color: black; }
.text { color: blue; }
#hero { color: red; }
  </pre>

  <p>HTML:</p>
  <pre>
&lt;p id="hero" class="text"&gt;Hallo&lt;/p&gt;
  </pre>

  <p>Die Farbe wird <strong>rot</strong>, da der ID-Selektor die höchste Spezifität hat.</p>
</div>

<div>
  <h2>5. Content-Box vs Border-Box</h2>

  <h3>Content-Box (Standard)</h3>
  <p>Die angegebene <code>width</code> umfasst nur den Inhalt. Padding und Border werden nicht eingerechnet.</p>

  <pre>
.box {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  box-sizing: content-box;
}
  </pre>

  <p><strong>Reale Breite:</strong> 200 + 20 + 20 + 5 + 5 = <strong>250px</strong></p>

  <h3>Border-Box</h3>
  <p>Die angegebene <code>width</code> umfasst Inhalt + Padding + Border.</p>

  <pre>
.box {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  box-sizing: border-box;
}
  </pre>

  <p><strong>Reale Breite bleibt 200px.</strong></p>

  <h3>Empfehlung:</h3>
  <pre>
* {
  box-sizing: border-box;
}
  </pre>
</div>
