   <h2>CSS Flexbox – kompakte Übersicht</h2>
    <p>
      Flexbox (offiziell: <strong>CSS Flexible Box Layout Module</strong>) ist ein modernes Layout-Modell
      in CSS. Es löst viele alte Probleme beim Erstellen von Layouts: z.&nbsp;B. vertikale Zentrierung,
      gleich hohe Spalten oder flexible Spaltenbreiten.
    </p>
    <p>
      Statt komplizierter Hacks mit Tabellen, <code>float</code>, <code>inline-block</code> oder
      „magischen“ Abständen bekommst du mit Flexbox ein klares System mit eigenen Achsen und Regeln.
    </p>
  <h2>Warum Flexbox?</h2>
  <ol>
    <li>Elemente können sehr leicht flexibel („gummimäßig“) werden: Sie wachsen oder schrumpfen nach Regeln
      und füllen den verfügbaren Platz.</li>
    <li>Vertikale und horizontale Ausrichtung – auch an der <em>baseline</em> des Textes – ist sehr einfach.</li>
    <li>Die Reihenfolge im HTML ist nicht mehr entscheidend. Du kannst die Reihenfolge der Elemente in CSS
      ändern (praktisch für Responsive Design).</li>
    <li>Elemente können automatisch in mehrere Reihen oder Spalten umbrechen und dabei den Platz ausnutzen.</li>
    <li>Flexbox ist für Sprachen mit Schreibrichtung von rechts nach links (RTL) optimiert. Es arbeitet mit
      „Anfang“ und „Ende“ statt nur mit „links“ und „rechts“ – die Reihenfolge passt sich automatisch an.</li>
    <li>Der CSS-Syntax ist relativ einfach und schnell zu lernen.</li>
  </ol>

  <h2>Grundbegriffe: Flex-Container und Flex-Items</h2>
  <p>
    Flexbox definiert CSS-Eigenschaften für:
  </p>
  <ul>
    <li>den <strong>Flex-Container</strong> (das Elternelement)</li>
    <li>die <strong>Flex-Items</strong> (die direkten Kindelemente)</li>
  </ul>
  <p>
    Um Flexbox zu aktivieren, setzt du am Container:
  </p>

  <h3>HTML</h3>
  <pre><code>&lt;div class="my-flex-container"&gt;
  &lt;div class="my-flex-item"&gt;item 1&lt;/div&gt;
  &lt;div class="my-flex-item"&gt;item 2&lt;/div&gt;
  &lt;div class="my-flex-item"&gt;item 3&lt;/div&gt;
&lt;/div&gt;</code></pre>

  <h3>CSS</h3>
  <pre><code>.my-flex-container {
  display: flex;       /* oder inline-flex */
}</code></pre>

  <h2>Hauptachse und Querachse</h2>
  <p>
    In Flexbox gibt es zwei wichtige Richtungen:
  </p>
  <ul>
    <li><strong>Hauptachse (main axis)</strong> – entlang dieser Achse werden die Flex-Items
      angeordnet.</li>
    <li><strong>Querachse (cross axis)</strong> – verläuft senkrecht zur Hauptachse.</li>
  </ul>
  <p>
    Standardmäßig (in LTR-Sprachen) verläuft die Hauptachse von links nach rechts,
    die Querachse von oben nach unten.
  </p>

  <figure>
    <img
      src="https://web.archive.org/web/20210718095533im_/http://html5.by/wp-content/uploads/2014/02/flexbox-main-row-300x300.png"
      alt="Flexbox Hauptachse in Zeilenrichtung (row)">
  </figure>

  <h3><code>flex-direction</code> – Richtung der Hauptachse</h3>
  <p>
    Mit <code>flex-direction</code> legst du fest, in welche Richtung die Flex-Items angeordnet werden.
  </p>
  <ul>
    <li><code>row</code> (Standard): von links nach rechts (in RTL von rechts nach links)</li>
    <li><code>row-reverse</code>: von rechts nach links (in RTL von links nach rechts)</li>
    <li><code>column</code>: von oben nach unten</li>
    <li><code>column-reverse</code>: von unten nach oben</li>
  </ul>

  <pre><code>.my-flex-container {
  display: flex;
  flex-direction: row;
}</code></pre>

  <h3><code>justify-content</code> – Ausrichtung auf der Hauptachse</h3>
  <p>
    <code>justify-content</code> steuert, wie die Flex-Items entlang der <strong>Hauptachse</strong>
    verteilt werden.
  </p>
  <ul>
    <li><code>flex-start</code> (Standard): Items kleben am Anfang der Hauptachse.</li>
    <li><code>flex-end</code>: Items kleben am Ende der Hauptachse.</li>
    <li><code>center</code>: Items werden in der Mitte der Hauptachse zentriert.</li>
    <li><code>space-between</code>: erstes Item am Anfang, letztes am Ende, der Rest gleichmäßig dazwischen.</li>
    <li><code>space-around</code>: alle Items haben gleichmäßige Abstände, auch zum Rand.</li>
  </ul>

  <figure>
    <img
      src="https://web.archive.org/web/20210718095533im_/http://html5.by/wp-content/uploads/2014/01/flex-justify-content-300x200.png"
      alt="Illustration justify-content in Flexbox">
  </figure>

  <h3><code>align-items</code> – Ausrichtung auf der Querachse</h3>
  <p>
    <code>align-items</code> steuert, wie die Flex-Items entlang der <strong>Querachse</strong>
    ausgerichtet werden.
  </p>
  <ul>
    <li><code>flex-start</code>: Items kleben am Anfang der Querachse.</li>
    <li><code>flex-end</code>: Items kleben am Ende der Querachse.</li>
    <li><code>center</code>: Items werden in der Mitte der Querachse zentriert.</li>
    <li><code>baseline</code>: Items werden an der Text-Baseline ausgerichtet.</li>
    <li><code>stretch</code> (Standard): Items werden in der Höhe/Breite gestreckt, um den freien Platz
      entlang der Querachse zu füllen (unter Beachtung von <code>min-</code>/<code>max-</code>-Werten).</li>
  </ul>

  <figure>
    <img
      src="https://web.archive.org/web/20210718095533im_/http://html5.by/wp-content/uploads/2014/01/flex-align-items-300x300.png"
      alt="Illustration align-items in Flexbox">
  </figure>

  <p>
    <strong>Wichtig:</strong> <code>flex-direction</code>, <code>justify-content</code> und
    <code>align-items</code> werden immer auf den <strong>Flex-Container</strong> angewendet,
    nicht auf die einzelnen Items.
  </p>

  <h2>Mehrere Zeilen oder Spalten: <code>flex-wrap</code></h2>
  <p>
    Standardmäßig versucht ein Flex-Container, alle Items in <strong>eine</strong> Zeile/Spalte zu packen.
    Mit <code>flex-wrap</code> kannst du mehrzeilige oder mehrspaltige Layouts aktivieren.
  </p>
  <ul>
    <li><code>nowrap</code> (Standard): alles in einer Zeile (bzw. Spalte).</li>
    <li><code>wrap</code>: Items umbrechen in mehrere Zeilen (oder Spalten), falls kein Platz mehr da ist.</li>
    <li><code>wrap-reverse</code>: wie <code>wrap</code>, aber in umgekehrter Richtung.</li>
  </ul>

  <pre><code>.my-flex-container {
  display: flex;
  flex-wrap: wrap;
}</code></pre>

  <h3><code>flex-flow</code> – Kurzform für Richtung + Umbruch</h3>
  <p>
    <code>flex-flow</code> kombiniert <code>flex-direction</code> und <code>flex-wrap</code>
    in einer Eigenschaft.
  </p>

  <pre><code>.my-flex-container {
  flex-direction: column;
  flex-wrap: wrap;
}

/* ist das gleiche wie: */

.my-flex-container {
  flex-flow: column wrap;
}</code></pre>

  <h3><code>align-content</code> – Ausrichtung mehrerer Reihen</h3>
  <p>
    Wenn der Container mehrere Reihen/Spalten von Items hat (also bei
    <code>flex-wrap: wrap</code> oder <code>wrap-reverse</code>), bestimmt
    <code>align-content</code>, wie diese Reihen entlang der Querachse verteilt werden.
  </p>
  <p><strong>Wichtig:</strong> <code>align-content</code> wirkt nur, wenn es wirklich
    mehrere Reihen/Spalten gibt.</p>
  <ul>
    <li><code>flex-start</code>: alle Reihen am Anfang des Containers.</li>
    <li><code>flex-end</code>: alle Reihen am Ende des Containers.</li>
    <li><code>center</code>: Reihen im Zentrum des Containers.</li>
    <li><code>space-between</code>: erste Reihe am Anfang, letzte am Ende, Rest gleichmäßig dazwischen.</li>
    <li><code>space-around</code>: Reihen sind mit gleichmäßigen Abständen bis zu den Rändern verteilt.</li>
    <li><code>stretch</code> (Standard): Reihen werden gestreckt, um den gesamten freien Platz zu füllen.</li>
  </ul>

  <figure>
    <img
      src="https://web.archive.org/web/20210718095533im_/http://html5.by/wp-content/uploads/2014/01/flex-align-content-e1390778353494.png"
      alt="Illustration align-content in Flexbox">
  </figure>

  <p>
    Auch <code>flex-wrap</code> und <code>align-content</code> gehören zum
    <strong>Flex-Container</strong>, nicht zu den Items.
  </p>

  <h2>Eigenschaften der Flex-Items</h2>

  <h3><code>flex-basis</code> – Basisgröße eines Items</h3>
  <p>
    <code>flex-basis</code> legt die <strong>Ausgangsgröße</strong> eines Flex-Items entlang
    der Hauptachse fest, bevor andere Faktoren (z.&nbsp;B. <code>flex-grow</code>) wirken.
  </p>
  <ul>
    <li>Kann in Längeneinheiten angegeben werden, z.&nbsp;B. <code>px</code>, <code>em</code>, <code>%</code> …</li>
    <li>Standardwert: <code>auto</code> – dann wird die Größe aus <code>width</code>/<code>height</code>
      (oder aus dem Inhalt) abgeleitet.</li>
  </ul>

  <h3><code>flex-grow</code> – „Wachstumsfaktor“ eines Items</h3>
  <p>
    <code>flex-grow</code> bestimmt, wie stark ein Item wächst, wenn überschüssiger Platz im Container
    vorhanden ist. Der Wert ist eine <strong>verhältnismäßige Zahl</strong> (kein Pixelwert).
  </p>

  <p><strong>Beispiele:</strong></p>
  <ul>
    <li>Wenn alle Items <code>flex-grow: 1</code> haben, sind sie gleich groß.</li>
    <li>Wenn ein Item <code>flex-grow: 2</code> hat und alle anderen <code>1</code>,
      ist dieses Item doppelt so breit/hoch wie die anderen.</li>
  </ul>

  <p>Ein weiteres Beispiel:</p>
  <ul>
    <li>Alle Items: <code>flex-grow: 3</code></li>
    <li>Ein Item: <code>flex-grow: 12</code></li>
  </ul>
  <p>Dann ist dieses Item viermal so „gierig“ wie die anderen (12 / 3 = 4) und bekommt entsprechend mehr Platz.</p>

  <h3><code>flex-shrink</code> – „Schrumpffaktor“ eines Items</h3>
  <p>
    <code>flex-shrink</code> steuert, wie stark ein Item schrumpfen darf, wenn nicht genug Platz da ist.
    Standardwert ist <code>1</code>. Ein höherer Wert bedeutet: dieses Item gibt schneller Platz ab
    als andere.
  </p>

  <h3><code>flex</code> – Kurzform für drei Eigenschaften</h3>
  <p>
    Die Eigenschaft <code>flex</code> ist eine Kurzschreibweise für:
  </p>
  <p><code>flex-grow flex-shrink flex-basis</code></p>

  <pre><code>.my-flex-item {
  flex-grow: 12;
  flex-shrink: 3;
  flex-basis: 30em;
}

/* ist das gleiche wie: */

.my-flex-item {
  flex: 12 3 30em;
}</code></pre>

  <h3><code>align-self</code> – Ausrichtung eines einzelnen Items</h3>
  <p>
    Mit <code>align-self</code> kannst du für ein einzelnes Flex-Item die allgemeine Einstellung
    <code>align-items</code> des Containers überschreiben.
  </p>
  <p>Erlaubte Werte (wie bei <code>align-items</code>):</p>
  <ul>
    <li><code>flex-start</code></li>
    <li><code>flex-end</code></li>
    <li><code>center</code></li>
    <li><code>baseline</code></li>
    <li><code>stretch</code> (Standard)</li>
  </ul>

  <h3><code>order</code> – Reihenfolge der Items</h3>
  <p>
    Standardmäßig erscheinen die Elemente in der Reihenfolge des HTML-Codes. Mit <code>order</code>
    kannst du diese Reihenfolge innerhalb eines Flex-Containers ändern.
  </p>
  <ul>
    <li>Standardwert: <code>0</code></li>
    <li>Es können positive und negative ganze Zahlen verwendet werden.</li>
  </ul>
  <p>
    <code>order</code> legt nicht die absolute Position fest, sondern eine <strong>Gewichtung</strong>:
    Items mit kleinerem <code>order</code> kommen zuerst.
  </p>

  <h4>HTML-Beispiel</h4>
  <pre><code>&lt;div class="my-flex-container"&gt;
  &lt;div class="my-flex-item" style="order: 5"&gt;item 1&lt;/div&gt;
  &lt;div class="my-flex-item" style="order: 10"&gt;item 2&lt;/div&gt;
  &lt;div class="my-flex-item" style="order: 5"&gt;item 3&lt;/div&gt;
  &lt;div class="my-flex-item" style="order: 5"&gt;item 4&lt;/div&gt;
  &lt;div class="my-flex-item" style="order: 0"&gt;item 5&lt;/div&gt;
&lt;/div&gt;</code></pre>

  <p>
    In diesem Beispiel ist die Reihenfolge entlang der Hauptachse:
    <code>item 5</code>, dann <code>item 1</code>, <code>item 3</code>, <code>item 4</code>, zuletzt
    <code>item 2</code>.
  </p>

  <h3><code>margin: auto</code> – endlich auch vertikal</h3>
  <p>
    In einem Flex-Container funktioniert <code>margin: auto</code> nicht nur horizontal,
    sondern auch vertikal. Damit kannst du ein Element sehr einfach in beide Richtungen zentrieren.
  </p>

  <pre><code>.my-flex-container {
  display: flex;
  height: 300px; /* beliebig */
}

.my-flex-item {
  width: 100px;
  height: 100px;
  margin: auto;  /* zentriert das Item horizontal und vertikal */
}</code></pre>

  <h2>Dinge, die du dir merken solltest</h2>
  <ol>
    <li>Nutze Flexbox nur dort, wo es wirklich nötig ist. Für ganz einfache Fälle reicht oft
      normales Block-Layout oder <code>display: inline-block</code>.</li>
    <li>Die Struktur des HTML bleibt wichtig. Überlege dir gut, wann du die Reihenfolge nur per CSS
      änderst.</li>
    <li>Lerne die Grundlagen von Flexbox (Achsen, Ausrichtung, Wachstum/Shrink). Dann erreichst du
      das gewünschte Layout viel schneller.</li>
    <li><code>margin</code>-Werte werden bei der Ausrichtung in Flexbox berücksichtigt. Margins
      „kollabieren“ hier nicht wie im normalen Dokumentenfluss.</li>
    <li><code>float</code> hat auf Flex-Items keinen Effekt. Das kann man für „graceful degradation“
      verwenden, wenn ältere Browser unterstützt werden müssen.</li>
    <li>Flexbox ist ideal für einzelne Komponenten und Bereiche einer Seite (z.&nbsp;B. Navigation,
      Karten, Teaser). Für große Seiten-Layouts (Header, Footer, Sidebar, Content) wird meistens
      eher <code>CSS Grid</code> empfohlen.</li>
  </ol>

  <h2>Fazit</h2>
  <p>
    Flexbox wird andere Layout-Techniken nicht komplett ersetzen, aber es ist ein sehr wichtiges
    Werkzeug im modernen CSS. Es löst viele typische Layout-Probleme elegant und mit wenig Code.
  </p>
  <p>
    Wenn du Flexbox einmal verstanden hast, kannst du schnell responsive und flexible Layouts
    bauen – ohne komplizierte Hacks.
  </p>