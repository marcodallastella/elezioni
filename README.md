# Scraper per i Dati di Affluenza Elettorale

Questo repository contiene uno script Python che estrae i dati dall'API non documentata del *Ministero dell'Interno* per le elezioni regionali in Emilia-Romagna e Umbria. In particolare, lo script scarica i dati relativi all'affluenza degli elettori nelle elezioni regionali, li elabora e memorizza i risultati in un DataFrame di pandas.

## Panoramica
Lo script elabora i dati elettorali per ciascun comune nelle regioni Emilia-Romagna e Umbria, estraendo e organizzando le seguenti informazioni chiave:

Numero totale di elettori
Elettori maschi e femmine
Percentuale di affluenza
Percentuale di sezioni scrutinate
Percentuale affluenza elezione precedente
Timestamp degli aggiornamenti dei dati

## Flusso di Lavoro dello Script

### Preparazione dei Dati:

Lo script inizia preparando una lista di "enti" (amministrazioni locali) a partire dai dati forniti dall'API. Questo include informazioni come:

- Codice dell'ente (cod)
- Descrizione dell'ente (desc)
- Tipo dell'ente (tipo)
- Tipo di comune (tipo_comune)
- Timestamp dell'ultimo aggiornamento (dt_agg)
- Codice dell'elezione (cod_ele)
- I dati vengono strutturati in un DataFrame di pandas (enti_df).

### Estrazione degli URL:

Lo script estrae gli URL dai DataFrame df_er e df_um, che vengono utilizzati per recuperare i dati sull'affluenza elettorale per ogni comune.

### Recupero e Elaborazione dei Dati:

Lo script cicla su ciascun URL, inviando una richiesta all'API del Ministero.
Per ogni risposta, lo script elabora gli aggiornamenti disponibili per i dati sull'affluenza e memorizza le informazioni chiave come:
- Numero totale di elettori (sia maschi che femmine)
- Percentuale di affluenza complessiva
- Percentuale di sezioni scrutinate
- Timestamp dell'aggiornamento
I dati vengono aggiunti a una lista di dizionari, che viene successivamente convertita in un DataFrame di pandas (df_data) e salvato in `output/affluenze_er.csv` e `output/affluenze_um.csv`.

Infine viene identificato l'ultimo aggiornamento disponibile e salvato in `output/viz`

#### Conversione dei Dati:

Le colonne delle percentuali vengono convertite da stringa a float per consentire un'analisi più approfondita.

#### Risultato:

Il DataFrame finale contiene i dati sull'affluenza per ciascun comune delle regioni specificate, pronto per essere analizzato o esportato.