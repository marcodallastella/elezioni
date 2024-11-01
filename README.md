# Elezioni API Scraper

## Descrizione
Questo codice utilizza un'API non documentata del sito dell'Interno italiano contenente i dati sulle elezioni. È attualmente impostato per estrarre i codici identificativi dei comuni nella regione Liguria e per ricostruire gli URL contenenti i dati scorporati per comune.

## Funzionalità
- Estrae i codici dei comuni in Liguria.
- Costruisce URL specifici per ogni comune per recuperare i dati elettorali.
- Recupera e salva i dati delle elezioni in un file CSV.

## Requisiti
- Python 3.x
- Pandas
- Requests

### Installazione delle dipendenze
Puoi installare le dipendenze richieste usando pip:

```bash
pip install pandas requests
