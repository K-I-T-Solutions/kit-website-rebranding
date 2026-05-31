# K.I.T. Solutions Website Rebranding

Zwischenstand fuer den Rebrand des oeffentlichen Webauftritts von K.I.T. Solutions.

Das Repository enthaelt aktuell eine statische Landingpage fuer die Uebergangsphase sowie die zugehoerigen Docker- und Proxy-Konfigurationen fuer lokalen Betrieb und Produktivbetrieb.

## Status

- `Live-Zwischenstand`: Under-Construction-Seite
- `Naechster Schritt`: vollstaendiger Relaunch des neuen Markenauftritts

## Inhalt

| Pfad | Zweck |
| :--- | :--- |
| `public/index.html` | Startseite der Uebergangsseite |
| `public/kontakt.html` | Kontaktseite |
| `public/impressum.html` | Impressum |
| `public/logo.svg` | Vektorlogo |
| `docker-compose.yml` | Lokaler Start auf Port `3010` |
| `docker-compose.prod.yml` | Produktivbetrieb mit Caddy |
| `Caddyfile` | Reverse-Proxy- und TLS-Konfiguration |

## Lokale Entwicklung

```bash
docker compose up --build
```

Danach ist die Seite unter `http://localhost:3010` erreichbar.

## Produktivbetrieb

```bash
docker compose -f docker-compose.prod.yml up --build -d
```

Der Produktiv-Stack besteht aus:

- statischem Webcontainer
- `Caddy` fuer HTTPS und Routing

## Tech-Stack

- Statisches HTML
- `nginx:alpine`
- Docker Compose
- Caddy

## Branding

- Logo: `public/logo.svg`
- Orange: `#FF6B35`
- Cyan: `#06B6D4`
- Blau: `#3B82F6`
- Navy: `#0F1629`

## Ziel des Repositories

Dieses Repository dient nicht als finaler Website-Stack, sondern als sauberer Zwischenstand fuer den Rebrand-Prozess. Es soll die Aussenwirkung von K.I.T. Solutions waehrend des Relaunchs konsistent halten, bis die vollstaendige neue Website produktiv uebernommen wird.
