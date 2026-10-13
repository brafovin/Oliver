# Oliver.io

Ein Slither.io-ähnliches Browserspiel in einer einzigen Datei (`index.html`) – ohne Abhängigkeiten.
Einfach `index.html` im Browser öffnen.

**Steuerung:** Maus lenkt, Leertaste / Linksklick = Turbo (kostet Länge). Pfeiltasten bzw. A/D lenken ebenfalls. Touch: Finger ziehen + Turbo-Button.

**Regeln:** Friss Futter, um zu wachsen. Berührst du den Körper einer anderen Schlange oder den Arenarand, explodierst du und wirst zu Futter. 22 KI-Gegner sind unterwegs.

## Oliver Strike (`strike.html`)

Taktischer 3D-Ego-Shooter im Browser (three.js per CDN, sonst eine einzelne Datei). Rundenbasiert gegen KI-Gegner, mit Kaufmenü, Radar und sechs Waffen (u. a. AK-47 und M4A1).

**Steuerung:** WASD, Maus, Linksklick schießen, Rechtsklick Zoom (Sniper), Shift schleichen, C ducken, Leertaste springen, R nachladen, 1/2/Q Waffe, B Kaufmenü.

**Waffengenauigkeit:** Streuung hängt von Laufen, Springen, Ducken und Dauerfeuer ab. Jede Waffe hat ein festes Rückstoßmuster (Spray-Pattern), das man mit der Maus ausgleicht. Das dynamische Fadenkreuz zeigt die aktuelle Streuung.

## Oliver Craft (`craft.html`)

Multiplayer-Sandbox im Blockstil: Eine prozedural erzeugte Insel, die man gemeinsam abbauen und bebauen kann. Eine einzelne Datei, three.js und PeerJS kommen per CDN – ein eigener Server ist nicht nötig.

**Mehrspieler:** Einer klickt auf „Neue Welt erstellen“ und bekommt einen 5-stelligen **Raumcode** (oder kopiert den Einladungslink). Freunde öffnen dieselbe Seite und treten mit dem Code bei. Die Verbindung läuft direkt zwischen den Browsern (WebRTC über PeerJS). Der Host verwaltet die Welt. Verlässt er das Spiel, endet die Runde für alle. Bis zu 10 Spieler pro Raum.

**Steuerung:** WASD laufen, Maus umsehen, Leertaste springen (2× tippen oder F = fliegen), Shift sprinten bzw. im Flug sinken, Linksklick abbauen, Rechtsklick bauen, Mittelklick Block übernehmen, 1–9 / Mausrad Slot wählen, E Blockauswahl, T Chat, Tab Spielerliste, F3 Koordinaten.

**Chat-Befehle:** `/hilfe`, `/spawn`, `/tp <Name>`, `/seed`, `/code`, `/tag` und `/nacht` (nur Host).

**Speichern:** Die Welt des Hosts wird automatisch im Browser gespeichert und kann mit „Gespeicherte Welt fortsetzen“ weitergespielt werden – meist sogar mit demselben Raumcode.

**Für Entwickler:** `?local` verbindet Tabs im selben Browser ohne Internet (zum Testen), `?signal=host:port` nutzt einen eigenen PeerJS-Server statt des öffentlichen, `?nolock` spielt ohne Mauszeiger-Fang.
