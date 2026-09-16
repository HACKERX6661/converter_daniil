# converter_daniil
converter für alle formate
# Universal Client-Side Converter Engine

Eine vollständig client-seitige Webanwendung zur Konvertierung von Quellcode, Medienformaten und Archivdateien. Das Projekt demonstriert den Einsatz von WebAssembly (WASM), abstrakter Syntaxanalyse (AST Transpilation) und In-Memory-Binärverarbeitung im Browser – ohne externe Backend-Server.

---

## Technical Features & Architektur

### 1. Code & Script Transpilation (AST Parser Engine)
* **Regelbasierte Übersetzungen:** Wandelt Windows Batch-Skripte (`.bat`) in äquivalenten Python- (`.py`) oder C-Code (`.c`) um.
* **JSON Syntax Parsing:** Parst JSON-Strukturen dynamisch und generiert typisierte Datenstrukturen für **C (`struct`)**, **Java (`class`)** und **C++ (`class`)**.

### 2. Audio & Video Transcoding (WebAssembly / FFmpeg)
* **WASM Core Integration:** Nutzt `@ffmpeg/ffmpeg`, um die C-Bibliothek FFmpeg direkt im virtuellen Speicher der V8 JavaScript-Engine auszuführen.
* **Client-side Processing:** Medienkonvertierungen (MP4, MP3, WAV, M4A) finden vollständig auf der Hardware des Nutzers statt.

### 3. Archive Processing & In-Memory Extraction
* **Binärdatenverarbeitung:** Liest und entpackt ZIP-Archive und Binärdaten mittels `JSZip` und JavaScript `ArrayBuffer` / `Blob` APIs direkt im RAM.

---

## Security & Privacy Advantage
Da alle Berechnungen, Parsings und Medien-Encodings ausschließlich lokal über die Client-Ressourcen des Webbrowsers ausgeführt werden, werden **keine Dateien auf externe Server übertragen**. Dies sorgt für maximale Privatsphäre und minimale Latenz.

---

## Tech Stack
* **Frontend:** HTML5, CSS3 (CSS Variables, Flexbox/Grid)
* **Core Logic:** Vanilla JavaScript (ES6+), Regular Expressions (RegEx)
* **High-Performance Runtimes:** WebAssembly (WASM), FFmpeg C-Core
* **Libraries:** JSZip (Buffer/Zip Processing), FFmpeg.wasm

---

## Installation / Lokale Ausführung
1. Repository klonen oder ZIP herunterladen.
2. Die Datei `index.html` direkt in einem modernen Browser (Chrome, Firefox, Edge) öffnen.
3. Keinen lokalen Webserver nötig (ausser für CoOP/COEP Header bei erweiterten WASM-Features).
