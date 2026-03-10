# 📸 Immich

Immich è una soluzione self-hosted per il backup automatico e la
gestione delle foto un'alternativa completa a Google Photos che
gira interamente sul proprio server, con pieno controllo sui dati.

---

## Perché Immich

Le foto sono tra i dati più personali e preziosi che esistano.
Affidarle a servizi cloud esterni significa perdere il controllo
su privacy, conservazione e accesso. Immich offre le stesse
funzionalità di Google Photos, backup automatico da mobile,
riconoscimento facciale, ricerca per luogo e data, album condivisi
— ma tutto rimane sul proprio hardware.

---

## Componenti

| Container | Immagine | Ruolo |
|---|---|---|
| `immich_server` | `ghcr.io/immich-app/immich-server:release` | Backend principale e API |
| `immich_machine_learning` | `ghcr.io/immich-app/immich-machine-learning:release` | Riconoscimento facciale e classificazione |
| `immich_postgres` | `ghcr.io/immich-app/postgres` | Database con estensioni vettoriali |
| `immich_redis` | `valkey/valkey:9` | Cache e gestione code |

---

## Configurazione

| Parametro | Valore |
|---|---|
| **Interfaccia** | HTTP, LAN only |
| **Restart policy** | `unless-stopped` |
| **Rete** | `immich_default` (bridge isolata) |

---

## Funzionalità

- Backup automatico da app mobile (iOS e Android)
- Riconoscimento facciale e raggruppamento per persona
- Ricerca per luogo, data, oggetti e scene tramite ML
- Album condivisi con altri utenti
- Timeline cronologica delle foto
- Supporto RAW e video

---

## File

| File | Descrizione |
|---|---|
| `docker-compose.yml` | Definizione di tutti e 4 i container dello stack |
| `.env.example` | Variabili d'ambiente necessarie (copiare in `.env`) |

---

## Note

- Il machine learning è il container più pesante — richiede tempo al primo avvio
- Le foto sono persistite in un volume dedicato: fare backup regolari
- L'app mobile va configurata con l'IP del server e la porta dedicata
- Aggiornare sempre tutti e 4 i container insieme — versioni miste causano problemi
