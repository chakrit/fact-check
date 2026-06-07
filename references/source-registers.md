# Quick-Start Source Registers (by claim type)

Once a claim's beat is identified (see `SKILL.md` §1), this gives a curated entry point:
the primary publishers to reach first, plus the one easy-to-forget cross-check. These are
*starting points, not a canonical or complete list* — confirm each is current and that
you're at the original publisher, not an aggregator restating it.

Sources are named **explicitly** on purpose: this skill must work on models that don't
already know them, so the named source is the payload and an anti-hallucination anchor —
do not thin the list down to the "obvious" ones. Source *institutions* are stable enough
to name; this directs *where* to retrieve, it never substitutes a recalled fact for
retrieval.

Apply the independence test and the proxy cross-checks from "Calibrate to evidence"
(`SKILL.md`) and `references/data-sources.md` throughout — a captured official source is a
claim, not data.

## Markets & macro
- **Primaries** — FRED (St. Louis Fed); the IMF data portal (now `data.imf.org`, migrated
  2024–25); BIS (`data.bis.org`); World Bank Open Data (also `data360.worldbank.org`);
  exchange data direct from the venue; SEC EDGAR and national securities regulators.
- **Cross-check** — mirror trade statistics (IMF DOTS / UN Comtrade); for a suspect
  national figure, satellite nightlights.
- **Integrity gauge** — IMF SDDS / Data Quality Assessment Framework (which countries meet
  disclosure standards).
- **Note** — confirm the migrated IMF/BIS portals; older hosts are deprecated.

## Energy, commodities & power
- **Primaries** — EIA (weekly petroleum status, API); IEA (Oil Market Report); JODI (oil &
  gas); OPEC (Monthly Oil Market Report); ENTSO-E Transparency Platform (European
  electricity); Baker Hughes rig count.
- **Cross-check** — Ember (independent power-sector data).
- **Note** — prefer physical-flow, inventory, and refinery-run reports over price
  commentary.

## Shipping, trade & supply chains
- **Primaries** — UN Comtrade; WTO trade statistics; national customs (USA Trade Online /
  Census, Eurostat Comext); UNCTAD Review of Maritime Transport; IMO GISIS (vessel /
  registry); WCO (Harmonized System authority).
- **Cross-check** — mirror statistics (exporter's figures vs partners' reported imports);
  Global Financial Integrity for trade misinvoicing.
- **Supply-chain stress** — NY Fed Global Supply Chain Pressure Index (GSCPI).
- **Note** — most AIS vessel trackers (MarineTraffic etc.) are commercial; EMSA is a more
  authoritative European baseline. A global authoritative AIS baseline still needs
  verifying.

## Corporate & financial filings
- **Primaries** — SEC EDGAR (full-text search); UK Companies House (API); EU BRIS
  (Business Registers Interconnection, the e-justice portal); GLEIF LEI registry (the
  un-fakeable legal-entity identifier); Japan EDINET (FSA); regulator enforcement (SEC
  litigation releases, FINRA BrokerCheck).
- **Cross-check / index** — OpenCorporates: an aggregator (transparent, with provenance) —
  useful as an index, not as a primary.
- **Note** — trace to the filed instrument, not the press release about it.

## Official statistics & demographics
- **Primaries** — national statistical offices; UN Statistics Division (SDG database);
  World Bank Open Data (WDI, API); OECD Data Explorer (SDMX API); Eurostat; US Census
  (`data.census.gov`, ACS API); IMF.
- **Cross-check** — mirror trade statistics; Human Mortality Database (independent
  excess-mortality / demographic cross-check).
- **Note** — apply the independence test; a captured national statistics office produces
  claims, not data.

## Politics, elections & government records
- **Primaries (cross-national)** — IPU Parline (parliaments); International IDEA Voter
  Turnout Database; ACE Electoral Knowledge Network / IFES Election Guide.
- **Primaries (national exemplars)** — US FEC (campaign finance, API); UK Hansard; US
  Congress.gov / GovInfo; EU EUR-Lex (the Official Journal gazette).
- **Cross-check** — V-Dem (Varieties of Democracy) for democratic-quality claims.
- **Note** — favor cross-national aggregators of primary records for arbitrary
  jurisdictions; the national portals are exemplars — find the equivalent body for the
  country in question.

## Law, courts & crime/justice
- **Primaries** — FBI Crime Data Explorer (UCR/NIBRS, `cde.ucr.cjis.gov`); Bureau of
  Justice Statistics (`bjs.ojp.gov` — NCVS + corrections); PACER (US federal court system
  of record, paywalled) with CourtListener/RECAP as the free mirror/index; UNODC
  (`dataunodc.un.org`, cross-national homicide & justice); Eurostat crime (EU/EFTA).
- **Cross-check** — FBI UCR (crimes reported to police) vs BJS NCVS (victimization
  survey): separate agencies, separate methods, bounding the truth from both sides — a
  "crime wave" visible in one but not the other is suspect. Cross-nationally, UNODC
  homicide is the most comparable metric (bodies are hard to hide).
- **Note** — legacy `ucr.fbi.gov` and `bjs.gov` are deprecated; CourtListener is an
  aggregator (confirm a contested filing against PACER itself). US-centric — elsewhere use
  the national statistics office / justice ministry, with UNODC as the cross-national
  layer.

## Migration & humanitarian
- **Primaries** — UNHCR Refugee Data Finder (forced displacement; free keyless API); IOM
  DTM (internal displacement & flows) and IOM Missing Migrants Project (migrant deaths);
  UN OCHA HDX/HAPI (curated datasets — aggregator, trace to source), FTS (humanitarian
  funding), ReliefWeb (situation reports); national/EU asylum statistics (Eurostat, US DHS
  OHSS, UK Home Office).
- **Cross-check** — IDMC Global Internal Displacement Database (NRC-affiliated,
  methodologically separate from IOM and UNHCR).
- **Note** — IOM DTM and Missing Migrants return 403 to bots but are live in a real
  browser — don't mark them dead. For a destination-country claim, go to that country's
  own authority.

## Health, medicine & nutrition
- **Primaries** — WHO `data.who.int` (Global Health Observatory); US CDC WONDER +
  `data.cdc.gov`; FDA (openFDA — Drugs@FDA, FAERS, MAUDE, recalls); EMA (EU
  authorizations/EPARs); ECDC (EU disease surveillance); ClinicalTrials.gov (NIH, API v2)
  and WHO ICTRP (registry meta-search); Cochrane CDSR (systematic reviews); PubMed/PMC
  (literature index).
- **Cross-check** — Our World in Data (Health) — transparent re-publication of
  WHO/CDC/IHME, every chart linked to its primary source.
- **Meta** — Health Feedback (Science Feedback) for viral health-claim review.
- **Note** — ClinicalTrials.gov classic site + legacy API retired Jun 2024 (use the
  modernized site + API v2); WHO consolidated onto `data.who.int` (old GHO OData
  deprecating late 2025); Cochrane full text is mostly paywalled.

## Science & research integrity
- **Primaries** — Crossref REST API (canonical DOI/metadata); Retraction Watch Database
  (now in Crossref; free CSV); PubMed/NCBI (PMC); arXiv; bioRxiv/medRxiv (preprints — flag
  that a preprint is not yet peer-reviewed).
- **Cross-check** — ClinicalTrials.gov pre-registration: compare the pre-registered
  primary outcomes against the published paper to catch outcome-switching.
- **Meta** — PubPeer (post-publication peer review; image-duplication and integrity
  flags).
- **Note** — Retraction Watch data moved into the production Crossref REST API (Jan 2025);
  the old Crossref *Labs* annotation endpoint is deprecating — use the production API or
  the GitLab CSV.

## Climate & environment
- **Primaries** — IPCC Assessment Reports (consensus synthesis); the independent
  surface-temperature records — NASA GISTEMP, NOAA NCEI/NOAAGlobalTemp, UK Met Office/CRU
  HadCRUT5; Copernicus C3S/ECMWF Climate Data Store (ERA5); Global Carbon Project (Global
  Carbon Budget).
- **Cross-check** — Berkeley Earth: an independent non-profit temperature record with open
  methodology — agreement across the four independent series is the strongest signal.
- **Meta** — Carbon Brief (sourced explainers, IPCC-process tracking); Climate Feedback
  (scientist claim review).
- **Note** — 2025 US disruption: NOAA Climate.gov was shut down/redirected and the
  Billion-Dollar Disasters product retired under Executive Order 14303 — a
  political-interference flag on some US-government climate products; lean on the
  multi-record consensus.

## Conflict, war & geopolitics
- **Primaries** — ACLED (event-level political violence; free myACLED account) and UCDP
  (Uppsala, academic gold-standard); Copernicus Browser (free Sentinel satellite imagery);
  ADS-B Exchange (unfiltered flight tracking incl. military); MarineTraffic / VesselFinder
  (AIS); GDELT (aggregator — flag).
- **Cross-check** — UCDP (conservative, slower) vs ACLED (faster, higher) on fatality
  counts — they bound each other; Bellingcat's Online Investigation Toolkit for OSINT
  verification.
- **Note** — ACLED migrated to a new Access Portal in 2025; legacy API keys were
  deprecated 2025-09-15. AIS can be spoofed or disabled; treat satellite/flight/ship
  signals as corroboration and fold image/video through `references/media-provenance.md`.

## Disasters, weather & public safety
- **Primaries** — USGS Earthquake Hazards / ANSS ComCat (global quakes, real-time API);
  NOAA/NWS (`api.weather.gov`, US only) with the WMO Severe Weather Information Centre
  (global aggregator routing to each national met service); Copernicus Emergency
  Management Service (satellite damage maps); EM-DAT (CRED, historical disaster catalog).
- **Cross-check** — EMSC (European-Mediterranean Seismological Centre): operationally
  independent of USGS — agreement between them confirms an earthquake's parameters.
- **Note** — no dedicated disaster claim-checker exists; convergence across official
  sources is the check. GDACS was renamed Nov 2025 (same `gdacs.org`); NOAA/NWS API is
  US-only — use WMO SWIC elsewhere.

## Technology, cybersecurity & platforms
- **Primaries** — CVE Program (`cve.org`, identifier registry); NIST NVD (CVSS/CWE
  enrichment); CISA KEV catalog (confirmed in-the-wild exploitation); Have I Been Pwned
  (breach exposure); vendor PSIRT advisories (the originating source for a product flaw);
  national CERTs/CSIRTs.
- **Cross-check** — ENISA EU Vulnerability Database (EUVD, launched 2025): vendor- and
  US-government-independent.
- **Note** — major currency flag: from 15 Apr 2026 NIST NVD stopped enriching most CVEs
  (large backlog), prioritizing only KEV / federal / critical software — don't assume an
  NVD entry is enriched; cross-check CVE + KEV + EUVD + the vendor advisory.

## Fact-check orgs & claim databases
- **Primaries** — IFCN Code of Principles verified signatories (the vetted-org allowlist);
  Google Fact Check Explorer / ClaimReview (cross-publisher search — aggregator); and
  established signatories: Snopes, PolitiFact (US), Full Fact (UK), AFP Fact Check
  (global).
- **Cross-check** — EFCSN (European Fact-Checking Standards Network) signatories — an
  independent cross-check on the IFCN list.
- **Meta** — EDMO repository + Duke Reporters' Lab database (index fact-checks across
  orgs).
- **Note** — use the IFCN/EFCSN allowlist to vet an unfamiliar "fact-checker" (a
  self-label is zero evidence). Meta ended its US third-party fact-checking program Jan
  2025 (→ Community Notes) — never rely on a single org.

## Quotes & misattributions
- **Primaries** — Quote Investigator (deeply sourced quotation tracing); HathiTrust
  full-text search (~18M digitized books — trace a phrase to its earliest dated print);
  The American Presidency Project + Miller Center (US presidential transcripts); The New
  Yale Book of Quotations (scholarly; paywalled).
- **Cross-check** — full-text search of dated digitized print (HathiTrust + Google Books)
  with date filters: find the earliest real appearance; no appearance before the
  attributed date refutes the attribution.
- **Meta** — Library of Congress "Quotations and Misquotations" research guide (method).
- **Note** — these are records and corpora, not self-styled authorities; trust derives
  from the checkable citation, not the source's name.

## Public figures & viral hoaxes
- **Primaries** — Google Fact Check Explorer + the IFCN/EFCSN signatory registries (vetted
  checkers); SEC EDGAR for US public-company executives; VIAF + Wikidata authority files
  (identity reconciliation).
- **Cross-check** — reverse image search across Google Lens + TinEye + Yandex (run all
  three): trace a viral image to its earliest appearance — the decisive check for death
  hoaxes and miscaptioned photos.
- **Meta** — Snopes death-hoax / viral-claim database.
- **Note** — no single "public-figure status" registry exists; resolve identity/role
  claims against official filings + authority files, and route image-based claims through
  `references/media-provenance.md`.
