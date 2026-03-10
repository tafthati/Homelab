# 🚀 OpenSpeedTest

OpenSpeedTest è uno strumento self-hosted per testare la velocità
della rete locale direttamente dal browser senza dipendere da
server esterni come Speedtest.net o Fast.com.

---

## Perché OpenSpeedTest

Testare la velocità verso server esterni misura la connessione
internet, non la rete locale. OpenSpeedTest misura la velocità
reale tra i dispositivi e il server ed è molto utile per verificare
le performance del Wi-Fi, della rete cablata e del NAS Samba.

---

## Configurazione

| Parametro | Valore |
|---|---|
| **Immagine** | `openspeedtest/latest:latest` |
| **Interfaccia** | HTTP, LAN only |
| **Restart policy** | `unless-stopped` |
| **Rete** | `openspeedtest_default` (bridge isolata) |

---

## Funzionalità

- Test di velocità in download e upload sulla rete locale
- Nessuna dipendenza da server esterni; tutto gira in LAN
- Interfaccia web moderna e responsive
- Risultati in tempo reale con grafico della velocità
- Compatibile con qualsiasi browser senza plugin

---

## File

| File | Descrizione |
|---|---|
| `docker-compose.yml` | Definizione del servizio |
| `.env.example` | Variabili d'ambiente necessarie (copiare in `.env`) |

---

## Note

- Per risultati accurati eseguire il test da dispositivi collegati
  via cavo; il Wi-Fi introduce variabili indipendenti dalla rete
- Utile in combinazione con iperf3 per una diagnosi completa
  delle performance di rete
