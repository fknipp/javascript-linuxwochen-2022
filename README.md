# JavaScript Linuxwochen 2022

## Die ganze Welt im Browser

### Visual Studio Code – der (Lieblings-)Editor ist immer dabei

1. Ein Repository in Github öffnen
1. Punkte (.) eingeben

https://github.dev/

### StackbBlitz – Darf es ein bisschen mehr sein?

Die Entwicklung von Webapplikationen braucht Werkzeuge. Die meisten stehen als NPM-Pakete zur Verfügung. Mit StackbBlitz kann man diese im Browser nutzen.

1. [StackbBlitz](https://stackblitz.com/) öffnen
1. Beispielprojekt Express unter Backend öffnen
1. Import von **express** in *package.json* zeigen
1. *index.js* anpassen
1. Im Terminal Applikation mit `npm start` neu starten

https://stackblitz.com/

Die Webcontainer von StackBlitz erlauben die Ausführung von Node.js im Browser.

https://blog.stackblitz.com/posts/introducing-webcontainers/

### Gitpod – Und jetzt auch im Container

Wenn es mehr als NPMs, sondern diverse Binaries braucht, führt uns der Weg zu Container. Diese Methode ist älter als die Webcontainer bei StackBlitz, aber auch dort erfreut sich Visual Studio Code als Editor steigender Beliebtheit.

1. 


## Der Sprung auf die Kommandozeile

### Deno

10 Jahre nach der Präsentation von Node.js hat dessen Erfinder eine neue JavaSript-Runtime erstellt. Diese setzt zwar auch wieder auf Googles V8 auf, soll aber [alle Fehler vermeiden](https://www.youtube.com/watch?v=M3BM9TB-8yA), die bei Node passiert sind.

1. Öffnen des Repositories https://github.com/gitpod-io/template-typescript-deno
1. Klick auf **Open in Gitpod**
1. Zeigen der Demo
1. Verwendung von `deno` auf der Kommandozeile
    1. `Math.random()`
    1. `await fetch('https://www.fh-burgenland.at')`

https://deno.land/

### Die "Rust"ifikation von JavaScript

Die JavaScript-Entwicklungswerkzeuge sind zumeist in JavaScript oder TypeScript erstellt:

- **Bundler**, die die Vielzahl von JavaScript-Dateien in eine überführen
- **Transpiler**, die JavaScript in JavaScript übersetzen, z. B. zur Unterstützung alternativer Syntaxen wie JSX oder Verwendung von in Entwicklung befindlichen JavaScript-Sprach-Features
- **Minifier**, die die erzeugten JavaScript-Dateien im Platzbedarf minimieren
- **Linter**, die den Quellcode analysieren und Verbesserungen vorschlagen
- **Formatierer**, die eine einheitliche Formatierung des Quellcodes sicherstellen

JavaScript ist dafür nicht die schnellste Technologie, gerade beim Bundling mit integriertem Tree-Shaking zum Entfernen nicht genutzter Funktionen, werden viele Schritte ausgeführt. 

Daher werden diese Tools zur Verarbeitung von JavaScript-Dateien in anderen Programmiersprachen umgesetzt, was Geschwindigkeitssteigerungen mit Faktoren von 10 bis 100 bringt.

- Rust in Deno
- Rust in der Bibliothek **swc**, die beispielsweise von Parcel, Next.js, Deno verwendet wird
- Go für **esbuild**

Rust kann übrigens auch nach WebAssembly (WASM) kompilieren.

### xz
TypeScript


## TypeScript: Was tut sich da?

Typisierung von JavaScript, ursprünglich 

https://github.com/tc39/proposal-type-annotations

