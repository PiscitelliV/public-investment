

<h1 align="center">
  <img src="docs/img/hero.svg" alt="Ontologia del dominio degli Investimenti Pubblici — PublicInvestment · prefisso pi · Codice Unico di Progetto (CUP) · OpenCUP" width="100%">
</h1>

<p align="center">
  <a href="https://w3id.org/italia/PublicInvestment"><img src="https://img.shields.io/badge/URI%20persistente-w3id.org%2Fitalia%2FPublicInvestment-0066cc" alt="w3id URI"></a>
  <a href="https://schema.gov.it"><img src="https://img.shields.io/badge/Catalogo-schema.gov.it-003366" alt="schema.gov.it"></a>
  <img src="https://img.shields.io/badge/versione-v1.0-089994" alt="versione">
  <a href="LICENSE"><img src="https://img.shields.io/badge/licenza-CC--BY%204.0-5c6f82" alt="licenza CC-BY 4.0"></a>
  <img src="https://img.shields.io/badge/OGP-Impegno%20C6%20(2024–2026)-008758" alt="OGP C6">
</p>

---

## Descrizione

Questo repository ospita i **semantic assets** del dominio degli **investimenti pubblici** della Pubblica Amministrazione italiana: l'ontologia **PublicInvestment**, i relativi **vocabolari controllati** e gli **identificatori persistenti** dei progetti CUP.

L'ontologia è il prodotto dell'analisi semantica del **Codice Unico di Progetto (CUP)** e del patrimonio informativo del portale **[OpenCUP](https://www.opencup.gov.it)**. È sviluppata dal **Dipartimento per la programmazione e il coordinamento della politica economica (DIPE)** della Presidenza del Consiglio dei Ministri, con la *semantic stewardship* dell'**ISTAT** e in coordinamento con il **Dipartimento per la Trasformazione Digitale (DTD)**, nell'ambito dell'**Impegno C6 del 6° Piano d'Azione Nazionale per il Governo Aperto (OGP) 2024–2026**.

Il namespace persistente `w3id.org/italia/PublicInvestment` è registrato secondo il modello *domain-contributor* del namespace nazionale `w3id.org/italia`. L'ontologia riusa ontologie CORE: CLV, COV, TI e SKOS della rete semantica del **Catalogo Nazionale dei dati semantici ([schema.gov.it](https://schema.gov.it))**.

## URI persistenti

| Risorsa | URI |
|---|---|
| Ontologia | `https://w3id.org/italia/PublicInvestment/onto/PublicInvestment` |
| Vocabolari controllati | `https://w3id.org/italia/PublicInvestment/controlled-vocabulary/{nome}` |
| Progetti (per codice CUP) | `https://w3id.org/italia/PublicInvestment/data/CUP/{CODICE_CUP}` |

> [!IMPORTANT]
> Gli URI sotto `data/CUP/` sono gli **identificatori ufficiali e persistenti** dei progetti d'investimento nei Linked Open Data e risolvono alla scheda pubblica del progetto su OpenCUP.

Gli URI supportano la *content negotiation*: per l'ontologia, le richieste con `Accept` RDF (`text/turtle`, `application/rdf+xml`, `application/n-triples`) risolvono alle serializzazioni pubblicate in questo repository; per i vocabolari controllati sono negoziabili Turtle (`text/turtle`) e CSV (`text/csv`). Le richieste HTML rinviano alla documentazione sul Catalogo Nazionale dei dati semantici, disponibile a valle dell'indicizzazione.

## Il modello

<p align="center">
  <img src="docs/diagrammi/PublicInvestment-overview.png" alt="Vista d'insieme semplificata dell'ontologia PublicInvestment" width="80%">
</p>
<p align="center"><sub>Vista d'insieme semplificata, derivata dalla serializzazione pubblicata (v1.0). Il sorgente vettoriale è disponibile in <code>docs/diagrammi/</code>.</sub></p>

Diagrammi di dettaglio per singolo modulo (progetto, CUP, intervento, natura, soggetto, atto, relazioni, tipizzazione delle data property) e la vista completa sono pubblicati accanto alle serializzazioni, in [`assets/ontologies/public-investment/latest/`](assets/ontologies/public-investment/latest/).

L'ontologia modella le entità centrali del sistema CUP: il **progetto** d'investimento, il **codice unico di progetto** e la sua storia, gli **interventi** con i relativi **schemi di classificazione** (natura, settore, sottosettore, tipologia, categoria), i **soggetti** (titolari, attuatori, accreditati), gli **atti di finanziamento**, la **localizzazione** e gli elementi **PNRR** (tematiche, sub-investimenti, target).

## Vocabolari controllati

| Vocabolario | URI | Formati |
|---|---|---|
| Natura di intervento | `…/controlled-vocabulary/natura_intervento` | TTL · CSV · XLSX |
| Tipologia di intervento | `…/controlled-vocabulary/tipologia_intervento` | TTL · CSV · XLSX |
| Classificazione di intervento | `…/controlled-vocabulary/classificazione_intervento` | TTL · CSV · XLSX |

Gli URI completi seguono il pattern `https://w3id.org/italia/PublicInvestment/controlled-vocabulary/{nome}`. Ciascun vocabolario è modellato come `skos:ConceptScheme` e pubblicato in `assets/controlled-vocabularies/{nome}/` nelle versioni `latest` e `v1.0`.

## Struttura del repository

```
public-investment/
├── README.md
├── LICENSE                              ← CC-BY 4.0
├── assets/
│   ├── ontologies/
│   │   └── public-investment/
│   │       ├── latest/                  ← public-investment.{ttl,rdf,json-ld,graphol}
│   │       │                              + diagrammi PNG per modulo
│   │       └── v1.0/                    ← copia immutabile della versione rilasciata
│   └── controlled-vocabularies/
│       ├── classificazione_intervento/  ← {latest,v1.0}/*.{ttl,csv,xlsx}
│       ├── natura_intervento/
│       └── tipologia_intervento/
└── docs/
    ├── diagrammi/                       ← vista d'insieme (PNG/SVG)
    └── img/                             ← loghi e immagini del README
```

## Serializzazioni

| Formato | File | Uso |
|---|---|---|
| Turtle | `public-investment.ttl` | formato di riferimento |
| RDF/XML | `public-investment.rdf` | interoperabilità, import in tool (es. Protégé) |
| JSON-LD | `public-investment.json-ld` | integrazione in applicazioni web |
| Graphol | `public-investment.graphol` | sorgente del modello (Eddy/Graphol) |

## Come citare

> DIPE — Dipartimento per la programmazione e il coordinamento della politica economica (Presidenza del Consiglio dei Ministri). *Ontologia del dominio degli Investimenti Pubblici (PublicInvestment)*, v1.0 (2026). URI: https://w3id.org/italia/PublicInvestment — Licenza CC-BY 4.0.

## Manutentori e contatti

- **Handle GitHub (manutentore):** [@PCM-DIPE](https://github.com/PCM-DIPE)
- Help Desk DIPE — open.cup@governo.it

- *Semantic stewardship:* ISTAT

## Licenza

Distribuito con licenza **[Creative Commons Attribution 4.0 International (CC-BY 4.0)](LICENSE)**.

## Ringraziamenti

Lavoro svolto nell'ambito dell'**Impegno C6 del 6° Piano d'Azione Nazionale OGP (2024–2026)** — [Open Government Partnership](https://www.opengovpartnership.org) / [open.gov.it](https://open.gov.it) — con la *semantic stewardship* di **ISTAT** e in coordinamento con il **Dipartimento per la Trasformazione Digitale**, a partire dal patrimonio informativo di [OpenCUP](https://www.opencup.gov.it).

<p align="center">
  <img src="docs/img/logo-istat.png" alt="ISTAT" height="44">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="docs/img/logo-dtd.png" alt="Dipartimento per la Trasformazione Digitale" height="44">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="docs/img/logo-ogp.png" alt="Open Government Partnership" height="44">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="docs/img/logo-opencup.png" alt="OpenCUP" height="44">
</p>
