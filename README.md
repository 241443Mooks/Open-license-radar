# Open Licence Opportunity Radar

A living, human-curated collection of **open-source foundations, open-licensed datasets, public-domain material and combinations worth building on**.

**Purpose:** find genuinely interesting, reusable starting points; prototype small ideas in 1–2 days; learn whether any should become useful tools or products. This is a research and experimentation radar, **not** a validated commercial-opportunity ranking.

## Explore the radar

| File | What's inside |
| --- | --- |
| [Opportunity register](data/opportunities.csv) | All **42** existing resource records, with unique IDs, building ideas, tiny experiments, licences, evidence links, user-adjustable scores and stages |
| [Experiment queue](data/experiments.csv) | **15** scoped prototype tests, with success evidence, estimated effort, stage, notes and result links |
| [Rights guide](data/rights-guide.csv) | Licence scope, reuse restrictions, dependencies and sources; **not legal clearance** |
| [Review log](data/review-log.csv) | History of existing additions, evidence and decisions |

The seed migration captures the **2 November 2026** refreshed workbook, including the original entries and notes. Original workbook remains a separate backup in ChatGPT Library.

## Build status and current direction

**OL-001 · Decision Canvas — Live (first playable, 2 November 2026).** [Open the deployed prototype](https://decision-canvas.corneliuslobster.workers.dev/) · [Source repository](https://github.com/241443Mooks/Decision-canvas-). The experience supports editable cards, labelled connections, browser-local persistence and JSON import/export. This records a working deployment, **not** completion of the experiment's user-validation test. Further development is paused until an actual use case emerges.

**OL-033 · Time-Layer Explorer — Live first playable (owner-confirmed 4 November 2026).** [Explore a place through time](https://time-layer.corneliuslobster.workers.dev/) · [Source repository](https://github.com/241443Mooks/Time-layer). Owner feedback: interesting but clunky. Code now provides four historical-period ranges from 4000 BCE through 2026 CE, with Roman/medieval jump years; verify Cloudflare has redeployed the latest commit. Site coverage is incomplete, the two embeds are not synchronised, and the experiment's five researched OHM features and two-minute user test are still pending. The v0.2 source adds a collapsible 'What do we know here?' evidence inspector, queried through an on-demand bounded OHM Overpass proxy, with nearby tagged records, source links and clickable recorded dates. The live API and panel markup were externally observed on 4 November 2026; the Manchester query returned the capped 150 records. A selected-year-only evidence filter is now committed, so future features and later events are hidden at earlier dates; unparseable/end-only records remain unresolved. Historical evidence retrieval now uses bounded 25-year Overpass windows, so the result cap is applied after a period filter. A Castlefield-only Historic England Scheduled Monuments lookup is now integrated behind a nested disclosure, with an independently verified live Roman fort wall record (NHLE 1001953). Legal scheduling dates still must not be treated as historical construction dates. [Layer plan](https://github.com/241443Mooks/Time-layer/blob/main/docs/evidence-layers.md). Version 0.3 now offers worldwide Wikidata coordinate-based place search, a place-first mobile-conscious layout, Wikipedia summaries and source-labelled nearby connections. The first curated Castlefield → Mamucium link preserves the year and breadcrumb trail; global OHM evidence lookup and place-detail API have returned live responses. Version 0.4 replaces the stacked map iframes with a single Past/Today flippable viewport (controls observed live and mocked interaction verified), makes the sourced Castlefield → Mamucium thread visible without opening the generic nearby list, and links to original-map archive viewers without asserting that scans are integrated. Tested the National Archives Discovery API for Castlefield (51 catalogue results), but this archive is a future connector, not yet in the app. [Discovery warren roadmap](https://github.com/241443Mooks/Time-layer/blob/main/docs/discovery-warren.md). An opt-in v0.5 **Keep views aligned · BETA** now uses one MapLibre map instance, an OHM date filter and a modern OSM raster overlay, so pan/zoom persist when flipping views. Mocked map-interaction tests passed; the original iframe version remains the fallback. A 5 November 2026 Android screenshot led to v0.6: collapsed place/year in a compact journey heading, a fold-away map window, shorter Wikipedia introductions, Commons-licensed hero and featured images, and a few illustrated nearby pathways with per-image creator/licence/source credits. The live Castlefield API returned verified media; further physical-device usability and historical attribution checks remain necessary. The 6 November v0.7 adds exact-year-aware Commons image gating (20-year pilot), a dated artwork search, a verified original London Bridge 1746 map-sheet permalink only for its historic bridge entity, and explicit distinction from modern railway station; no year-matched source means no illustration or map link. [Source quality and ranking rules](https://github.com/241443Mooks/Time-layer/blob/main/docs/source-matching.md). On 6 November v0.8 added an in-place time-hop strip (±25/100 years), optional named OHM date suggestions using the same bounded cache, discovery before the map, and compressed evidence lists; Commons images now preserve century/bounded intervals rather than assigning vague records to false point years. [Warren roadmap](https://github.com/241443Mooks/Time-layer/blob/main/docs/discovery-warren.md). Version 0.9 includes a live, narrowly curated Tower of London history with separate Roman-site and Norman-building evidence, seven sourced chapter jumps, and a genuinely unknown-dated anonymous house research route with four archive methods. It is a working prototype, not an automated multi-source history engine. [Adaptive history and Codex roadmap](https://github.com/241443Mooks/Time-layer/blob/main/docs/adaptive-history-codex-brief.md). Promising 1–2 day options already in the experiment register are **OL-033 Time-Layer Explorer** (OpenHistoricalMap + MapLibre), **OL-007 Hidden Britain** (Historic England + mapped heritage sites), **OL-017 Geology Beneath My Walk** (BGS + maps), and **OL-038 Wild Near Me** (GBIF + maps). Choose a single location and five-to-ten objects/records for the first prototype; check map tiles, feature-level rights and attribution first.

## First things to try

- **Decision Canvas** — [React Flow](https://reactflow.dev/): create, connect, save and reload ten visual nodes.
- **Hidden Britain** — [Historic England Open Data](https://historicengland.org.uk/listing/the-list/data-downloads/) + [OpenStreetMap](https://www.openstreetmap.org/): plot ten interesting places and invite someone to choose one to visit.
- **Rabbit Hole** — [Wikidata](https://www.wikidata.org/): follow surprising factual connections and make an interactive visual graph.
- **Art Detective** — [The Met Open Access](https://metmuseum.github.io/): make a tiny visual-detail quiz with suitably cleared objects.
- **Historical time-layer** — [OpenHistoricalMap](https://www.openhistoricalmap.org/) + [MapLibre](https://maplibre.org/): map five historic features and compare time periods; verify the rights of each source and map layer.

Ideas can stay in **Inbox** or **Explore** without becoming commitments. Use GitHub Issues for experiments you actually decide to develop—not one issue per interesting resource.

## How scoring works

The workbook's editable ratings (columns `Curiosity /5`, `Start /5`, `Potential /5`) determine the subjective `Fit /100` score:

`Fit /100 = ROUND(20 × (0.40 × Curiosity + 0.35 × Start + 0.25 × Potential), 0)`

The CSV stores current values, not live spreadsheet formulas. When changing ratings, recompute the score. Do not confuse a high score with evidence of user demand.

## Research and rights rules

1. Begin with the original publisher, source repository or official collection. Include a **resource URL** and a **licence/terms evidence URL** in every new row.
2. A public website, GitHub repository or API is **not automatically licensed for reuse**. Check software, data, images, fonts, models, map tiles, third-party assets and hosted/API terms separately.
3. Distinguish `Verified` (published licence for the specified scope) from `Scope check`, `Item check` and `API terms`. Even verified licences are not blanket clearance.
4. Assess attribution, share-alike, non-commercial rules, UK copyright status, API quotas, trademark restrictions and paid service costs before commercial use.
5. Keep a narrow, testable **1–2 day experiment** and an evidence/success test for any shortlisted candidate.
6. **Never overwrite personal notes, decisions, stages or existing entries** during a refresh. Use stable `OL-###` IDs, deduplicate by resource and canonical URL, and record meaningful edits in [the review log](data/review-log.csv).
7. Prioritise genuinely new and interesting opportunities. If none clear the bar, make no edits.

## Maintaining the repository

**Source of truth:** the four CSV files under `data/`. Changes are tracked through normal Git commits. Weekly research should preserve existing values and add only substantiated, source-backed opportunities, using the existing schema.

**Current snapshot:** 42 opportunities, 15 experiments; last source-workbook refresh: **2 November 2026**.

> **Licensing of this repository:** third-party links and descriptions retain their own rights, specified individually. The repository's public visibility does not itself grant a licence over original editorial content or code. Choose a repository licence deliberately before publishing reusable original materials.
