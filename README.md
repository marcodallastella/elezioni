# Scraper per Eligendo

Questo repository contiene i notebooks usate per estrarre ed elaborare dati di elezioni da [Eligendo](https://dait.interno.gov.it/elezioni), il portale del Ministero dell'Interno contenente i dati delle elezioni politiche ed europee.

Per farlo utilizziamo l'API non documentata del sito. (🙏 Grazie [Leon Yin](https://inspectelement.org/apis.html)).

## Notebooks

- **0_scraper_codici** : notebook utilizzato per estrarre i codici identificativi di ogni entità (regioni, circoscrizioni, province, comuni). Serviranno per ricostruire le nostre richieste all'API.
- **1_affluenza_ER** : notebook utilizzato per scaricare i dati sull'affluenza in Emilia Romagna
- **1_affluenza_UM** : notebook utilizzato per scaricare i dati sull'affluenza in Umbria
- **2_scraper_risultati_ER** : notebook utilizzato per scaricare i risultati in Emilia Romagna (solo Presidente, non sono presenti i dati per singola lista)
- **2_scraper_risultati_UM** : notebook utilizzato per scaricare i risultati in Umbria (solo Presidente, non sono presenti i dati per singola lista)

## Outputs
- [Codici identificativi Emilia Romagna e Umbria](output/codici_umbria_er.csv)
- [Affluenze Emilia Romagna](output/affluenze_er.csv)
- [Affluenze Umbria](output/affluenze_um.csv)
- [Risultati Emilia Romagna](output/risultati_er.csv)
- [Risultati Umbria](output/risultati_um.csv)

## Grafici

#### Risultati presidente (confronto centrodestra-centrosinistra)
- [Liguria](https://www.datawrapper.de/_/zC8EU)
- [Emilia Romagna](https://www.datawrapper.de/_/9yIHu)
- [Umbria](https://www.datawrapper.de/_/ervq2)

#### Affluenza
- [Liguria](https://www.datawrapper.de/_/TPPvf/)
- [Emilia Romagna](https://www.datawrapper.de/_/pWRZG/)
- [Umbria](https://www.datawrapper.de/_/YElha/)

#### Affluenza - confronto con elezioni regionali precedenti
- [Umbria](https://www.datawrapper.de/_/Znz4J)
- [Emilia Romagna](https://www.datawrapper.de/_/wS5a8/?v=11)
- [Liguria](https://www.datawrapper.de/_/DM7Nf)

### Contatti

Marco Dalla Stella
[m.dallastella@proton.me](mailto:m.dallastella@proton.me)
[BlueSky](https://bsky.app/profile/mdallastella.bsky.social)
