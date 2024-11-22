# Italian Regional Elections Data Tracker

A collection of tools to track and analyze Italian regional election data by accessing the Ministry of Interior's undocumented API. This project automates the collection of voter turnout and election results data from [Eligendo](https://dait.interno.gov.it/elezioni), the official election portal.

## Project Overview

The project consists of three main components that work together to collect and process election data in real-time:

1. **Location Code Extractor** (`0_codici.ipynb`)
   - Maps the hierarchical structure of electoral districts
   - Extracts unique identifiers for regions, provinces, and municipalities
   - Essential for constructing valid API requests

2. **Turnout Tracker** (`1_affluenza.ipynb`)
   - Monitors voter turnout in real-time
   - Tracks participation rates across different timeframes
   - Compares current turnout with historical data

3. **Results Processor** (`2_risultati.ipynb`)
   - Collects and processes vote counts as they come in
   - Handles both party-list and candidate-level results
   - Calculates electoral margins and shifts from previous elections

## Technical Details

The system works by:
- Reverse-engineering the Eligendo portal's internal API
- Constructing properly formatted API requests using official location codes
- Processing JSON responses into structured data
- Generating clean CSV files ready for analysis or visualization

### Key Features
- Real-time data collection
- Automated geocoding of results
- Historical comparison capabilities
- Multiple output formats for visualization

## Data Outputs

### Raw Data Files

- [Location Codes - Liguria](https://github.com/marcodallastella/elezioni/blob/main/output/codici_li.csv)
- [Location Codes - Emilia Romagna e Umbria](output/codici_umbria_er.csv)
- [Voter Turnout - Liguria](https://github.com/marcodallastella/elezioni/blob/main/output/affluenze_li.csv)
- [Voter Turnout - Emilia Romagna](output/affluenze_er.csv)
- [Voter Turnout - Umbria](output/affluenze_um.csv)
- [Election Results - Liguria](https://github.com/marcodallastella/elezioni/blob/main/output/risultati_LI.csv)
- [Election Results - Emilia Romagna](output/risultati_er.csv)
- [Election Results - Umbria](output/risultatium.csv)

### Visualizations
##### Risultati presidente (confronto centrodestra-centrosinistra)
- [Liguria](https://www.datawrapper.de//zC8EU)
- [Emilia Romagna](https://www.datawrapper.de/_/9yIHu)
- [Umbria](https://www.datawrapper.de/_/ervq2)
##### Affluenza
- [Liguria](https://www.datawrapper.de/_/TPPvf/)
- [Emilia Romagna](https://www.datawrapper.de/_/pWRZG/)
- [Umbria](https://www.datawrapper.de/_/YElha/)
#### Affluenza - confronto con elezioni regionali precedenti
- [Umbria](https://www.datawrapper.de/_/Znz4J)
- [Emilia Romagna](https://www.datawrapper.de/_/wS5a8/?v=11)
- [Liguria](https://www.datawrapper.de/_/DM7Nf)

## Usage

Each notebook is documented and contains step-by-step examples. The core workflow:

1. Run `0_codici_ER_UM.ipynb` to get location codes
2. Use `1_affluenza_ER.ipynb` to track turnout
3. Process results with `2_risultati_ER.ipynb`

## Contact

Marco Dalla Stella  
📧 [m.dallastella@proton.me](mailto:m.dallastella@proton.me)  
🦋 [BlueSky](https://bsky.app/profile/mdallastella.bsky.social)

---

*Note: For more information about working with undocumented APIs and web scraping techniques, check out this [resource guide](https://inspectelement.org/apis.html).*
