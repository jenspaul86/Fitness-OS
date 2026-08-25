# Fitness OS – Projektregeln für Claude Code

Dieses Repo enthält `index.html` (Version 0.9.10), eine Single-File Web-App (reines HTML/CSS/JS, kein Framework). Die vollständige Projektübergabe (Datenstruktur, Regressionshistorie, Screens/UI-Ideen, Exportformate) liegt in `HANDOFF.md` im selben Repo – bei tieferen Fragen dort nachschlagen.

## Harte Entwicklungsregeln (unbedingt einhalten)

1. **Funktionierende Features sind eingefroren.** Nicht ändern, wenn sie nicht Teil der aktuellen Aufgabe sind.
2. Technische Abhängigkeiten vorher benennen und regressionstesten.
3. Nach jeder Änderung den Kerncheck durchgehen (siehe unten).
4. Keine großen Funktionsblöcke ersetzen, wenn nur ein kleiner Teil geändert werden soll.
5. Kritische UI-Aktionen möglichst direkt binden.
6. CSS-Grid/Flex-Höhen bei UI-Blöcken gemeinsam prüfen.
7. iPhone-Safari: nicht nur `min-height` verwenden; Inputs mindestens 16px (gegen Auto-Zoom).
8. Web-Audio auf iOS ist nur Best-Effort – keine Verlässlichkeit versprechen.
9. Zielplattform ist ausschließlich iPad und iPhone (kein Mac/Android/Desktop-Web).
10. **Bei jeder echten (nicht rein kosmetischen Test-)Änderung wird die Versionsnummer hochgezählt** – im Code (`APP_VERSION`-Konstante in `index.html`) und in der sichtbaren Anzeige (Badge, Startseiten-Footer, Trainingsscreen-Header, Export-Payloads), damit jederzeit eindeutig erkennbar ist, ob die laufende App auf dem neuesten Stand ist.

## Kerncheck nach jeder Änderung

Nicht jedes Mal alles, aber je nach betroffenem Bereich kurz durchklicken:

- App startet
- Training startet
- Satz bestätigbar
- Timer startet
- Timer läuft negativ weiter
- Übungswechsel
- Swipe
- Auto-Weiter
- Übersicht
- Training beenden
- Abschlussbewertung
- Summary
- Daten gespeichert
- Backup
- Coach-Export

## Vorgehen bei jeder Aufgabe

1. Code lesen
2. Betroffene Funktionen isolieren
3. Änderungen minimal halten
4. Kerncheck durchführen
5. Erst dann committen

## Kontext, der wichtig ist

- Persönliches Coaching-Umfeld: Bevel (Recovery + Strength-Builder-Test), Alpha Progression (RIR-Referenz), YAZIO (Ernährung), Apple Health (Datendrehscheibe) laufen parallel weiter und werden schrittweise abgelöst, nicht sofort ersetzt.
- Geplante Architektur-Richtung: Capacitor (nicht React Native), um die bestehende `index.html` zu wrappen statt neu zu schreiben – für echten HealthKit-, Hintergrund-Audio- und Hintergrundbetrieb-Zugriff.
- Vorgehen bewusst in kleinen Etappen, nicht alles auf einmal.
