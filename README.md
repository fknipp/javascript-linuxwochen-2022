# JavaScript Linuxwochen 2022

## Die ganze Welt im Browser

### Visual Studio Code – der (Lieblings-)Editor ist immer dabei

1. Ein Repository in Github öffnen
1. Punkte (.) eingeben

https://github.dev/

### StackBlitz – Darf es ein bisschen mehr sein?

Die Entwicklung von Webapplikationen braucht Werkzeuge. Die meisten stehen als NPM-Pakete zur Verfügung. Mit StackBlitz kann man diese im Browser nutzen.

1. [StackBlitz](https://stackblitz.com/) öffnen
1. Beispielprojekt Express unter Backend öffnen
1. Import von **express** in *package.json* zeigen
1. *index.js* anpassen
1. Im Terminal Applikation mit `npm start` neu starten

https://stackblitz.com/

Die Webcontainer von StackBlitz erlauben die Ausführung von Node.js im Browser.

https://blog.stackblitz.com/posts/introducing-webcontainers/

### Gitpod – Und jetzt auch im Container

Wenn es mehr als NPMs, sondern diverse Binaries braucht, führt uns der Weg zu Container. Diese Methode ist älter als die Webcontainer bei StackBlitz, aber auch dort erfreut sich Visual Studio Code als Editor steigender Beliebtheit.

1. Öffnen des Repositories https://github.com/gitpod-io/template-typescript-deno
1. Klick auf **Open in Gitpod**
1. Zeigen von *.gitpod.yml* und *.gitpod.Dockerfile*

https://gitpod.io

## Der Sprung auf die Kommandozeile

### Deno – Node.js reloaded

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

### zx – die Verschmelzung von JavaScript und Bash

Die Bash ist sehr toll, aber irgendwann kommt man an ihre Grenzen, und der Wunsch nach einer leistungsfähigeren Programmiersprache wird laut. Google versucht diese Lücke mit zx zu schließen.

1. Workspace in Gitpod öffnen
1. Imstallation von zx
    ```
    npm i -g zx
    ```
1. Erzeugen einer neuen Datei *test-zx.mjs* mit dem Inhalt
    ```
    #!/usr/bin/env zx
    ```
1. Ausführungsrechte setzen
    ```
    chmod a+x test-zx.mjs
    ```
1. Ausführung der Datei mit
    ```
    ./test-zx.mjs
    ```

```javascript
#!/usr/bin/env zx

// Aufruf eines Befehls
await $`ls`;

// Verarbeitung der Ausgabe
const process = await quiet($`ls`);
console.log(process.stdout.split("\n"));

// Escaping der Parameter
const ugly_filename = "abc $USER &";
await $`touch ${ugly_filename}`;
```

https://github.com/google/zx

## TypeScript: Was tut sich da?

JavaScript ist eine schwach typisierte Sprache. Typisierung bringt aber Vorteile, z. B. die Typprüfung vor der Ausführung oder verbesserte Assistenten bei der Softwareentwicklung. TypeScript ist eine streng typisierte Sprache auf Basis von JavaScript. Es ist eine Übersetzung von TypeScript nach JavaScript erforderlich.

https://www.typescriptlang.org/

Jede JavaScript-Datei ist eine gültige TypeScript-Datei. Das erlaubt die Erweiterung von JavaSript um eine optionale Typisieren. Ein entsprechender Vorschlag liegt bereits auf Stage 1 vor.

https://github.com/tc39/proposal-type-annotations