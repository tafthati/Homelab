# 📝 Memos

Memos è un'applicazione self-hosted per le note rapide in stile
microblog leggera, veloce e minimalista. Perfetta per catturare
pensieri, appunti tecnici e promemoria senza la complessità
di un sistema di note completo.

---

## Perché Memos

A volte serve uno spazio semplice dove buttare giù un'idea,
un comando da ricordare o una nota veloce senza aprire BookStack
e creare una pagina strutturata. Memos riempie questo spazio:
è sempre aperto in un tab del browser, pronto in un second damn.

---

## Configurazione

| Parametro | Valore |
|---|---|
| **Immagine** | `neosmemo/memos:stable` |
| **Interfaccia** | HTTP, LAN only |
| **Restart policy** | `unless-stopped` |
| **Rete** | `memos_default` (bridge isolata) |

---

## Funzionalità

- Note rapide in Markdown con anteprima live
- Tag per organizzare e filtrare i contenuti
- Ricerca full-text su tutte le note
- Fissaggio delle note importanti in cima
- Visualizzazione a calendario e a timeline
- API REST per integrazioni esterne
- Supporto multi-utente

---

## File

| File | Descrizione |
|---|---|
| `docker-compose.yml` | Definizione del servizio |
| `.env.example` | Variabili d'ambiente necessarie (copiare in `.env`) |

---

## Note

- I dati sono persistiti in un volume Docker dedicato con database SQLite
- Memos è volutamente minimalista, non è un sostituto di BookStack
  ma un complemento per note veloci e informali
- Il tag `stable` garantisce versioni testate e affidabili
