# 📁 File Browser

File Browser è un gestore di file via interfaccia web che permette
di navigare, caricare, scaricare, modificare e condividere file
direttamente dal browser senza bisogno di client FTP o accesso SSH.

---

## Perché File Browser

Accedere ai file del server tramite terminale è potente ma scomodo
per operazioni quotidiane. File Browser offre un'interfaccia grafica
intuitiva per gestire i file da qualsiasi dispositivo in rete locale,
con supporto per upload drag-and-drop, anteprima di immagini e
condivisione tramite link temporanei.

---

## Configurazione

| Parametro | Valore |
|---|---|
| **Immagine** | `filebrowser/filebrowser:latest` |
| **Interfaccia** | HTTP, LAN only |
| **Restart policy** | `unless-stopped` |
| **Rete** | `file-browser_default` (bridge isolata) |

---

## Funzionalità

- Navigazione e gestione file via browser
- Upload drag-and-drop di file e cartelle
- Anteprima di immagini, video e documenti
- Editor di testo integrato per file di configurazione
- Condivisione tramite link temporanei con scadenza
- Gestione utenti con permessi personalizzabili per cartella
- Tema chiaro e scuro

---

## File

| File | Descrizione |
|---|---|
| `docker-compose.yml` | Definizione del servizio |
| `.env.example` | Variabili d'ambiente necessarie (copiare in `.env`) |


---

## Note

- Le credenziali di default al primo avvio sono `admin` / `admin` e vanno subito cambiate
- Le cartelle accessibili vanno montate come volumi nel `docker-compose.yml`
- I permessi utente sono configurabili granularmente per ogni cartella montata
