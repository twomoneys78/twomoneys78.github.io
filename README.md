# twomoneys78.github.io
# Audio Synthesizer mit GPU.js und Web Audio API

## Übersicht
Dieses Projekt implementiert ein Audio-Synthesizer-Tool, das GPU.js für die Berechnung von Audio-Wellenformen und die Web Audio API für die Audioausgabe nutzt. Es bietet Funktionen zur Erzeugung von Melodien, Skalen und benutzerdefinierten Instrumenten, die auf zufälligen Parametern basieren.

## Hauptfunktionen
- **Instrumentenerstellung**: Klassenbasiertes Design für Instrumente mit Unterstützung für Wellenformen und Stereokanäle.
- **GPU-beschleunigte Audioverarbeitung**: Nutzung von GPU.js zur Berechnung von komplexen Audio-Wellenformen.
- **Dynamische Melodien**: Algorithmisch erzeugte Melodien basierend auf zufälligen Skalen und Parametern.
- **Visualisierung**: Skalen und Wellenformen werden visuell auf Canvas-Elementen dargestellt.
- **Echtzeit-Steuerung**: Konfigurierbare Parameter wie Dauer (in Sekunden) und Interaktion durch Buttons.

## Voraussetzungen
- Browser mit Unterstützung für Web Audio API und WebGL.
- Eine lokale Kopie von `gpu-browser.min.js`.

## Dateistruktur
- **index.html**: Hauptdatei, die den Code, UI-Elemente und Logik enthält.
- **gpu-browser.min.js**: GPU.js-Skript für die GPU-beschleunigte Verarbeitung.

## Verwendung
1. Öffnen Sie die `index.html`-Datei in einem unterstützten Browser.
2. Klicken Sie auf den Button "Sound", um den Synthesizer zu starten.
3. Passen Sie die Parameter wie "Seconds" an, um die Dauer des generierten Audios zu ändern.
4. Nutzen Sie den Button "Next please", um die aktuelle Wiedergabe zu stoppen und eine neue Session zu starten.

## Highlights des Codes
- **Instrument-Klasse**: Definiert die Eigenschaften und das Verhalten eines Instruments.
- **Melody-Klasse**: Generiert Melodien basierend auf den bereitgestellten Skalen.
- **waveGPU-Funktion**: GPU.js-basierte Funktion zur Berechnung von Audio-Wellenformen mit Obertönen und Vibrato.
- **Bongo- und Wave-Funktionen**: Spezialisierte Funktionen zur Synthese verschiedener Klangcharakteristiken.

## Anpassung
- **Skalen**: Passen Sie die `sc`-Variable an, um unterschiedliche musikalische Skalen zu verwenden.
- **Wellenformen**: Modifizieren Sie die `waveGPU`- und `bongoGPU`-Funktionen, um neue Wellenformen zu erstellen.
- **Benutzeroberfläche**: Fügen Sie zusätzliche Steuerungselemente für Parameter wie Lautstärke, BPM oder Instrumenteneigenschaften hinzu.

## Lizenz
Dieses Projekt steht unter der [MIT-Lizenz](LICENSE).

## Autoren
- **Ihr Name**
