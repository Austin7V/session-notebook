
  <h1>CSS Grundlagen</h1>

  <!-- SECTION 1 -->
  <div class="section">
    <h2>1. Was ist CSS und wofür braucht man es?</h2>
    <p>
      <strong>CSS (Cascading Style Sheets)</strong> ist eine Stylesheet-Sprache, die das Aussehen
      und Layout einer Webseite bestimmt.  
      Während HTML für die Struktur der Inhalte verantwortlich ist, sorgt CSS dafür,
      wie diese Inhalte visuell dargestellt werden.
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

  <!-- SECTION 2 -->
  <div class="section">
    <h2>2. CSS Syntax</h2>
    <p>Die CSS-Syntax besteht aus einem Selektor, einer Eigenschaft und einem Wert.</p>

    <pre>
selektor {
  property: value;
}
    </pre>

    <p><strong>Beispiel:</strong></p>
    <pre>
p {
  color: red;
  font-size: 18px;
}
    </pre>

    <p>Dieses Beispiel verändert die Farbe und Größe aller &lt;p&gt;-Elemente.</p>
  </div>

  <!-- SECTION 3 -->
  <div class="section">
    <h2>3. Selektortypen</h2>

    <h3>Grundlegende Selektoren:</h3>
    <ul>
      <li><strong>Typselektor</strong> – wählt HTML-Tags  
        <code>p { color: blue; }</code></li>

      <li><strong>Klassenselektor</strong> – wählt Elemente mit einer Klasse  
        <code>.button { padding: 10px; }</code></li>

      <li><strong>ID-Selektor</strong> – wählt ein eindeutiges Element  
        <code>#header { background: black; }</code></li>

      <li><strong>Universalselektor *</strong> – wählt alle Elemente  
        <code>* { margin: 0; }</code></li>

      <li><strong>Attributselektor</strong>  
        <code>input[type="text"] { border: 1px solid gray; }</code></li>
    </ul>

    <h3>Kombinierte Selektoren:</h3>
    <ul>
      <li><strong>Nachfahre</strong>  
        <code>div p { color: green; }</code></li>

      <li><strong>Kindselektor</strong>  
        <code>ul &gt; li { margin: 5px; }</code></li>

      <li><strong>Adjacent Sibling</strong>  
        <code>h2 + p { font-style: italic; }</code></li>
    </ul>

  </div>

  <!-- SECTION 4 -->
  <div class="section">
    <h2>4. Spezifität</h2>

    <p>
      Die Spezifität bestimmt, welche CSS-Regel angewendet wird, wenn mehrere Regeln auf dasselbe Element zutreffen.
    </p>

    <h3>Priorität (von niedrig nach hoch):</h3>

    <ol>
      <li>Tag-Selektor (z. B. <code>div</code>)</li>
      <li>Klasse (<code>.container</code>)</li>
      <li>ID (<code>#main</code>)</li>
      <li>Inline-Style (<code>&lt;p style="color:red"&gt;</code>)</li>
      <li><strong>!important</strong> (höchste Priorität, aber schlecht für sauberen Code)</li>
    </ol>

    <h3>Beispiel:</h3>
    <pre>
p { color: black; }
.text { color: blue; }
#hero { color: red; }
    </pre>

    <p>Wenn das HTML-Element so aussieht:</p>

    <pre>
<p id="hero" class="text">Hallo</p>
    </pre>

    <p><strong>Die Farbe wird rot</strong>, da ID die höchste Spezifität besitzt.</p>
  </div>

  <!-- SECTION 5 -->
  <div class="section">
    <h2>5. Content-Box vs Border-Box</h2>

    <h3>Content-Box (Standardwert)</h3>
    <p>
      Die angegebene <code>width</code> umfasst nur den Inhalt.  
      <strong>Padding und Border werden nicht eingerechnet.</strong>
    </p>

    <pre>
.box {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  box-sizing: content-box;
}
    </pre>

    <p>Reale Breite = 200 + 20 + 20 + 5 + 5 = <strong>250px</strong></p>

    <hr>

    <h3>Border-Box</h3>
    <p>
      Die angegebene <code>width</code> beinhaltet Inhalt + Padding + Border.  
      <strong>Die Gesamtgröße bleibt exakt so, wie angegeben.</strong>
    </p>

    <pre>
.box {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  box-sizing: border-box;
}
    </pre>

    <p>Reale Breite bleibt <strong>200px</strong>.</p>

    <h3>Gewöhnliche Empfehlung:</h3>
    <pre>
* {
  box-sizing: border-box;
}
    </pre>

  </div>