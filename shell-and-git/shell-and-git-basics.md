🐚 Shell and Git Basics — Meine Notizen

⭐ Was ist die Shell?

Die Shell ist ein textbasiertes Interface, mit dem man direkt mit dem Betriebssystem arbeitet.
Man gibt Befehle ein, um:
- Dateien und Ordner anzulegen
- im Dateisystem zu navigieren
- Programme auszuführen
- Prozesse zu steuern

Wichtige Shell-Befehle:

Befehl Bedeutung
- ls              zeigt den Inhalt des aktuellen Ordners
- ls -la          zeigt alle Dateien inkl. versteckter Dateien
- cd <Ordner>     in einen Ordner wechseln
- cd ..           eine Ebene zurück
- cd ~            ins Home-Verzeichnis
- pwd             zeigt den aktuellen Pfad
- mkdir <name>    erstellt einen neuen Ordner
- touch <datei>   erstellt eine neue Datei
- rm <datei>      löscht eine Datei (oder -rf dazu "rm -rf" dann kann mann ganze ordener löschen)
- mv <alt> <neu>  verschiebt oder umbenennt Dateien/Ordner

⸻

⭐ Was ist Git?

Git ist ein Versionskontrollsystem.
Damit kann man:
• Änderungen speichern
• frühere Versionen wiederherstellen
• Code online teilen (z. B. über GitHub)
• in Teams zusammenarbeiten

⸻

⭐ Wichtige Git-Befehle

🔹 Repository erstellen

git init

🔹 Status prüfen

git status

🔹 Dateien zum Commit vormerken

git add <datei oder ordner>
git add .

🔹 Commit erstellen

git commit -m "Beschreibung"

🔹 Remote-Repository hinzufügen

git remote add origin <SSH-Link>

🔹 Code zum Server pushen

git push -u origin main
git push

🔹 Änderungen vom Server holen

git pull

⸻

⭐ Wie man ein Remote-Repository erstellt (Schritte) 1. Lokalen Ordner öffnen 2. Mit git init ein Repository erstellen 3. Dateien hinzufügen: git add . 4. Commit machen: git commit -m "initial commit" 5. Auf GitHub ein neues, leeres Repository anlegen 6. SSH-Link kopieren 7. Mit git remote add origin <link> verbinden 8. Mit git push -u origin main hochladen

⸻

⭐ Meine Learnings
• Die Shell spart viel Zeit beim Arbeiten
• Git speichert meinen Fortschritt und schützt mich vor Fehlern
• Ich kann jetzt Projekte hochladen und online verwalten
• Push, Pull, Commit und Add gehören zu den wichtigsten Git-Befehlen
