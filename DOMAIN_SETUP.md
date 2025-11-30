# Domain Setup für loot-goblin.xyz

## Schritt 1: DNS-Einträge bei Cloudflare setzen

1. Gehe zu Cloudflare Dashboard: https://dash.cloudflare.com
2. Wähle deine Domain `loot-goblin.xyz`
3. Gehe zu **DNS** → **Records**
4. Füge folgende Einträge hinzu:

### Option A: CNAME (Empfohlen - Einfacher)
- **Type**: CNAME
- **Name**: @ (oder loot-goblin.xyz)
- **Target**: `teddyflo95-boop.github.io`
- **Proxy status**: DNS only (graue Wolke)
- **TTL**: Auto

### Option B: A Records (Alternative)
Falls CNAME nicht funktioniert, verwende diese A Records:
- **Type**: A
- **Name**: @
- **IPv4 address**: `185.199.108.153`
- **Proxy status**: DNS only
- **TTL**: Auto

- **Type**: A
- **Name**: @
- **IPv4 address**: `185.199.109.153`
- **Proxy status**: DNS only
- **TTL**: Auto

- **Type**: A
- **Name**: @
- **IPv4 address**: `185.199.110.153`
- **Proxy status**: DNS only
- **TTL**: Auto

- **Type**: A
- **Name**: @
- **IPv4 address**: `185.199.111.153`
- **Proxy status**: DNS only
- **TTL**: Auto

## Schritt 2: GitHub Pages konfigurieren

1. Gehe zu: https://github.com/teddyflo95-boop/lootgoblin-website
2. Gehe zu **Settings** → **Pages**
3. Unter **Custom domain** trage ein: `loot-goblin.xyz`
4. Aktiviere **Enforce HTTPS** (wird nach DNS-Propagation verfügbar)
5. Warte 5-10 Minuten

## Schritt 3: Warte auf DNS-Propagation

- DNS-Änderungen können 5 Minuten bis 24 Stunden dauern
- Normalerweise: 10-30 Minuten
- Prüfe Status: https://dash.cloudflare.com → DNS

## Schritt 4: Testen

Öffne: https://loot-goblin.xyz

Falls es nicht funktioniert:
- Warte weitere 10 Minuten
- Prüfe DNS-Propagation: https://dnschecker.org/#A/loot-goblin.xyz
- Prüfe GitHub Pages Settings

## Wichtig bei Cloudflare:

- **Proxy status muss auf "DNS only" (graue Wolke)** sein!
- Nicht auf "Proxied" (orange Wolke) setzen für GitHub Pages
- Sonst funktioniert es nicht!

