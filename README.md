# Selfhosting-Stack

Dieses Repository bietet eine modulare Selfhosting-Umgebung für verschiedene Dienste auf Basis von Docker Compose. Ziel ist es, die wichtigsten Anwendungen für den privaten Serverbetrieb einfach und sicher bereitzustellen.

## Enthaltene Komponenten
- **Reverse Proxy (Traefik):** Zentrale Verwaltung von HTTPS, Routing und Zertifikaten für alle Dienste
- **Vaultwarden:** Passwortmanager (Bitwarden-kompatibel)
- **Jellyfin:** Medienserver für Filme, Serien und Musik
- **Nextcloud:** Cloud-Speicher und Kollaborationsplattform

Jeder Dienst ist in einem eigenen Unterordner mit Beispiel-Konfiguration und separater `.env`-Datei organisiert.

## Architektur
```
selfhosting/
├── reverse-proxy/      # Traefik Reverse Proxy (docker-compose, traefik.yml, .env)
├── vaultwarden/        # Vaultwarden Setup (docker-compose, .env)
├── jellyfin/           # Jellyfin Setup (docker-compose, .env)
├── nextcloud/          # Nextcloud Setup (docker-compose, .env)
├── docs/               # Dokumentation, HowTos
├── .gitignore          # Sensitive Daten ausgeschlossen
└── README.md           # Diese Datei
```

## Hinweise zur Nutzung
- Sensible Daten wie Passwörter, Zertifikate und Backups werden durch `.gitignore` ausgeschlossen.
- Für jeden Dienst gibt es eine eigene `.env`-Datei (Beispiel liegt jeweils bei).
- Die Konfigurationen sind als Vorlage gedacht und müssen für den Produktivbetrieb angepasst werden (z.B. Passwörter, Domains, Zertifikate).

## Quickstart
1. Repository clonen
2. Eigene `.env`-Dateien in den jeweiligen Dienst-Ordnern anpassen
3. Docker Compose Dateien nach Bedarf editieren
4. Mit Portainer oder `docker compose up -d` starten

---

Weitere Hinweise und Anleitungen finden sich im Ordner `docs/`.
