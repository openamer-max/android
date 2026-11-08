# OpenAmer — Android

Alle Versionen der Android-App **`ai.openamer.mobile`**.

## Neueste Version: 1.3.0

### ⬇ [openamer-latest.apk herunterladen](https://github.com/openamer-max/android/releases/latest/download/openamer-latest.apk)

Immer die aktuellste Version — der Link bleibt gleich.

## Alle Versionen

| Version | Größe | SHA-256 (Anfang) | Was drin ist | Download |
|---|---|---|---|---|
| **1.3.1** | 616 KB | `f3ffbda1…` | **Retrieval-Fixes** (Skill-Erkennung, Autor-Frage) — 85 % → 95 % im Eval | [openamer-latest.apk](https://github.com/openamer-max/android/releases/download/v1.3.1/openamer-latest.apk) |
| 1.3.0 | 616 KB | `3084601b…` | RAG-Wissensbasis eingebaut (43 Fakten + 165 Skills) | [openamer-latest-1.3.0.apk](https://github.com/openamer-max/android/releases/download/v1.3.0/openamer-latest.apk) |
| 1.2.0 | 604 KB | `d69fa36d…` | Original-Build | [OpenAmer-1.2.0-android.apk](https://github.com/openamer-max/android/releases/download/v1.2.0/OpenAmer-1.2.0-android.apk) |
| 1.1.0 | 595 KB | `c593dd25…` | Erster Build | [OpenAmer-1.1.0-android.apk](https://github.com/openamer-max/android/releases/download/v1.1.0/OpenAmer-1.1.0-android.apk) |

### Direkt-Links ohne Release-Seite

```
https://raw.githubusercontent.com/openamer-max/android/main/openamer-latest.apk
https://raw.githubusercontent.com/openamer-max/android/main/OpenAmer-1.2.0-android.apk
https://raw.githubusercontent.com/openamer-max/android/main/OpenAmer-1.1.0-android.apk
```

> Hinweis: `github.com/openamer-max/android/<datei>.apk` liefert **HTTP 404** —
> GitHub zeigt unter diesem Pfad keine Datei. Nur die Links oben funktionieren.

## ⚠️ Signatur — bitte lesen

| Version | Signaturzertifikat |
|---|---|
| 1.1.0, 1.2.0 | Original: `CN=OpenAmer, OU=Mobile Division, O=OpenAmer AGI/ASI, L=Stuttgart, C=DE` |
| **1.3.0** | Neu: `CN=OpenAmer, OU=OpenAmer-max, O=Amer Sacirovic, L=Glattal, C=CH` |

Der private Schlüssel der Original-Builds lag nicht vor, deshalb ist 1.3.0 mit
einem **neuen Schlüssel** signiert.

**Folge:** Wer 1.1.0 oder 1.2.0 installiert hat, muss diese **zuerst
deinstallieren**, bevor 1.3.0 installiert werden kann. Android verweigert
Updates über einen Schlüsselwechsel (Signatur-Konflikt).

## Installation

1. APK herunterladen
2. „Unbekannte Quellen installieren" für den Browser erlauben
3. APK öffnen und installieren

**Beim ersten Start** kann die App einmal beendet werden, während WebView noch
Komponenten lädt — einfach erneut öffnen.

## Was 1.3.0 bringt

**Eingebaute Wissensbasis (RAG)** — 43 kuratierte Fakten über OpenAmer und
165 Skills, per BM25 direkt in der App, offline und ohne Server. Vor jeder
Anfrage legt die App die passenden Fakten als Systemkontext dazu. Ergebnis:

| | Antwort auf „Was ist OpenAmer?" |
|---|---|
| Modell ohne RAG | „OpenAmer ist keine bekannte Bezeichnung oder Organisation…" |
| **App mit RAG** | „OpenAmer ist ein persönlicher KI-Assistent, der lokal auf deinem Rechner läuft… von **Amer Sacirovic in der Schweiz** entwickelt." |

Die Wissensbasis wiegt 30 KB JavaScript — deshalb bleibt die APK bei ~600 KB.
Ein Sprachmodell ist **nicht** enthalten; Modelle kommen weiterhin über Provider
(Ollama, OpenAI, Anthropic, Groq, DeepSeek, Mistral, Together, xAI, Cerebras,
MiniMax, Moonshot, Cloudflare, Z.ai).

## Verifikation

Alle Dateien wurden vor dem Upload geprüft: `apksigner verify` (v2/v3),
`aapt2 dump badging` (Package, versionCode, versionName) und SHA-256.

---
OpenAmer · Amer Sacirovic · Open Source · Apache-2.0
