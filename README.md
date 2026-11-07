# OpenAmer — Android

Offizielle Android-App von OpenAmer (`ai.openamer.mobile`).

## Download

**[⬇ openamer-latest.apk herunterladen](https://github.com/openamer-max/android/releases/latest/download/openamer-latest.apk)**

Direkt-Download (ohne Release-Seite):
`https://raw.githubusercontent.com/openamer-max/android/main/openamer-latest.apk`

## Was diese Version (1.3.0) bringt

- **Eingebaute Wissensbasis (RAG)** — 43 kuratierte Fakten über OpenAmer plus
  165 Skills, per BM25 direkt in der App. Die App legt die passenden Fakten
  automatisch als Systemkontext in jede Anfrage, sodass das Modell Fragen über
  OpenAmer korrekt beantwortet statt zu raten. Funktioniert offline, ohne Server,
  ohne zusätzliche Downloads.
- Weiterhin: alle Provider (Ollama, OpenAI, Anthropic, Groq, DeepSeek, Mistral,
  Together, xAI, Cerebras, MiniMax, Moonshot, Cloudflare, Z.ai)

## Installation

1. APK herunterladen
2. „Unbekannte Quellen installieren" für den Browser erlauben
3. APK öffnen und installieren

**Wichtig:** Diese Version ist mit einem **neuen Schlüssel** signiert. Wenn eine
ältere OpenAmer-App installiert ist, muss sie **zuerst deinstalliert** werden —
sonst verweigert Android das Update (Signatur-Konflikt).

## Technisch

- Basis: bestehende WebView-App (kein Modell in der APK — Modelle laufen über
  Ollama/Provider)
- RAG-Schicht: reines JavaScript in `assets/index.html`, ~30 KB
- Signatur: APK Signature Scheme v2 + v3

---
OpenAmer · Amer Sacirovic · Open Source
