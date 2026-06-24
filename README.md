<!--
  README istituzionale per il repository  PCM-DIPE/public-investment
  (deliverable Fase B — repository dei semantic assets del dominio investimenti pubblici).
  NON è il README della PR w3id, che resta minimale.

  LOGHI/IMMAGINI:
  - Carica i file logo in  docs/img/  (vedi segnaposto sotto) e lascia i percorsi relativi.
  - Usa i loghi ufficiali di cui hai i diritti (DiPE.png, ISTAT, DTD, ecc.).
  - I diagrammi Graphol dell'ontologia vanno in  docs/diagrammi/  (PNG/JPG).
-->

<p align="center">
  <!-- Sostituisci i src con i file reali in docs/img/ . Rimuovi le righe dei loghi che non userai. -->
  <img src="docs/img/logo-pcm-dipe.png" alt="DIPE — Presidenza del Consiglio dei Ministri" height="72">
  &nbsp;&nbsp;&nbsp;
  <img src="docs/img/logo-istat.png" alt="ISTAT" height="72">
  &nbsp;&nbsp;&nbsp;
  <img src="docs/img/logo-dtd.png" alt="Dipartimento per la Trasformazione Digitale" height="72">
</p>

<h1 align="center">Ontologia del dominio degli Investimenti Pubblici</h1>
<p align="center"><strong>PublicInvestment</strong> &nbsp;·&nbsp; prefisso <code>pi</code> &nbsp;·&nbsp; basata sul <em>Codice Unico di Progetto (CUP)</em> e su OpenCUP</p>

<p align="center">
  <a href="https://w3id.org/italia/PublicInvestment"><img src="https://img.shields.io/badge/URI%20persistente-w3id.org%2Fitalia%2FPublicInvestment-1a5fb4" alt="w3id URI"></a>
  <a href="https://schema.gov.it"><img src="https://img.shields.io/badge/Catalogo-schema.gov.it-17324d" alt="schema.gov.it"></a>
  <img src="https://img.shields.io/badge/versione-v0.1-informational" alt="versione">
  <a href="LICENSE"><img src="https://img.shields.io/badge/licenza-CC--BY%204.0-blue" alt="licenza CC-BY 4.0"></a>
  <img src="https://img.shields.io/badge/OGP-Impegno%20C6%20(2024–2026)-2e7d32" alt="OGP C6">
</p>

---

## Descrizione

Questo repository ospita i **semantic assets** del dominio degli **investimenti pubblici** della Pubblica Amministrazione italiana: l'ontologia **PublicInvestment**, i relativi **vocabolari controllati** e gli **identificatori persistenti** dei progetti CUP.

L'ontologia è il prodotto dell'analisi semantica del **Codice Unico di Progetto (CUP)** e del patrimonio informativo del portale **[OpenCUP](https://www.opencup.gov.it)**. È sviluppata dal **Dipartimento per la programmazione e il coordinamento della politica economica (DIPE)** della Presidenza del Consiglio dei Ministri, con la *semantic stewardship* dell'**ISTAT** e in coordinamento con il **Dipartimento per la Trasformazione Digitale (DTD)**, nell'ambito dell'**Impegno C6 del 6° Piano d'Azione Nazionale per il Governo Aperto (OGP) 2024–2026**. È allineata alla rete **OntoPiA** ed è pubblicata nel **Catalogo Nazionale dei dati semantici (schema.gov.it)**.

## URI persistenti

| Risorsa | URI |
|---|---|
| Ontologia | `https://w3id.org/italia/PublicInvestment/onto/PublicInvestment` |
| Vocabolari controllati | `https://w3id.org/italia/PublicInvestment/controlled-vocabulary/{nome}` |
| Progetti (per codice CUP) | `https://w3id.org/italia/PublicInvestment/data/CUP/{CODICE_CUP}` |

> Gli URI sotto `data/CUP/` sono gli **identificatori ufficiali e persistenti** dei progetti d'investimento nei Linked Open Data e risolvono alla scheda pubblica del progetto su OpenCUP.

## Il modello

<p align="center">
  <!-- Diagramma Graphol esportato in PNG/JPG. Sostituisci con il file reale. -->
  <img src="docs/diagrammi/PublicInvestment-overview.png" alt="Diagramma dell'ontologia PublicInvestment" width="80%">
</p>

L'ontologia modella le entità centrali del sistema CUP: il **progetto** d'investimento, i **soggetti** (titolari e attuatori), i **dati finanziari**, la **localizzazione geografica** e gli **schemi di classificazione** (natura, settore, sottosettore, tipologia, categoria).

## Struttura del repository

```
public-investment/
├── README.md
├── LICENSE                      ← CC-BY 4.0
├── CHANGELOG.md
├── assets/
│   ├── ontologies/
│   │   └── PublicInvestment/
│   │       ├── latest/          ← PublicInvestment.{ttl,rdf,n3} + -metadata.ttl
│   │       └── v0.1/            ← copia immutabile della versione rilasciata
│   └── controlled-vocabularies/
│       └── {nome_vocabolario}/
│           └── latest/
├── src/                         ← sorgente Graphol
├── doc/                         ← Documento di Analisi (PDF) e note
│   └── diagrammi/               ← PNG/JPG dei diagrammi ontologici
└── docs/
    └── img/                     ← loghi e immagini del README
```

## Serializzazioni

| Formato | File | Uso |
|---|---|---|
| Turtle | `PublicInvestment.ttl` | formato di riferimento (OntoPiA) |
| RDF/XML | `PublicInvestment.rdf` | interoperabilità, import tool (es. Protégé) |
| N-Triples | `PublicInvestment.n3` | triple grezze, triplestore/SPARQL |
| Metadati | `PublicInvestment-metadata.ttl` | scheda ADMS-AP_IT |

## Come citare

> DIPE — Dipartimento per la programmazione e il coordinamento della politica economica (Presidenza del Consiglio dei Ministri). *Ontologia del dominio degli Investimenti Pubblici (PublicInvestment)*, v0.1. URI: https://w3id.org/italia/PublicInvestment — Licenza CC-BY 4.0.

## Manutentori e contatti

- **Handle GitHub (manutentore):** [@PCM-DIPE](https://github.com/PCM-DIPE)
- Francesco De Stefanis (DIPE) — f.destefanis@governo.it
- Leonardo Salvatori (DIPE) — leo.salvatori@governo.it
- *Semantic stewardship:* ISTAT

## Licenza

Distribuito con licenza **[Creative Commons Attribution 4.0 International (CC-BY 4.0)](LICENSE)**, la licenza standard delle ontologie della rete OntoPiA.

## Ringraziamenti

Lavoro svolto nell'ambito dell'**Impegno C6 del 6° Piano d'Azione Nazionale OGP (2024–2026)**, con il contributo di ISTAT e del Dipartimento per la Trasformazione Digitale.

<p align="center">
  <img src="docs/img/logo-ogp.png" alt="Open Government Partnership" height="48">
  &nbsp;&nbsp;&nbsp;
  <img src="docs/img/logo-opencup.png" alt="OpenCUP" height="48">
</p>
