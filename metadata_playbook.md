---
args:
  autori:
  - Team Documentazione Tecnica
  - Dipartimento Sviluppo Piattaforma
  data_creazione: '2023-11-20'
  data_modifica: '2024-05-10'
  descrizione: Una guida tecnica dettagliata su come creare, aggiornare e annullare
    gli avvisi di pagamento utilizzando le API della Piattaforma Notifiche di PagoPA.
  diataxis_type: how-to
  json_ld: "{\n  \"@context\": \"https://schema.org\",\n  \"@graph\": [\n    {\n      \"@type\":
    \"HowTo\",\n      \"@id\": \"https://docs.pagopa.it/piattaforma-notifiche/v2.4/how-to/gestire-avvisi-pagamento\",\n
    \     \"name\": \"Come gestire gli avvisi di pagamento con le API della Piattaforma
    Notifiche\",\n      \"description\": \"Una guida tecnica dettagliata su come creare,
    aggiornare e annullare gli avvisi di pagamento utilizzando le API della Piattaforma
    Notifiche di PagoPA.\",\n      \"datePublished\": \"2023-11-20\",\n      \"dateModified\":
    \"2024-05-10\",\n      \"inLanguage\": \"it-IT\",\n      \"publisher\": {\n        \"@type\":
    \"Organization\",\n        \"name\": \"PagoPA S.p.A.\",\n        \"url\": \"https://www.pagopa.it\",\n
    \       \"logo\": {\n          \"@type\": \"ImageObject\",\n          \"url\":
    \"https://docs.pagopa.it/assets/logo-pagopa.svg\"\n        }\n      },\n      \"author\":
    {\n        \"@type\": \"Organization\",\n        \"name\": \"PagoPA S.p.A.\"\n
    \     },\n      \"about\": {\n        \"@type\": \"SoftwareApplication\",\n        \"name\":
    \"Piattaforma Notifiche\",\n        \"softwareVersion\": \"v2.4\"\n      },\n
    \     \"totalTime\": \"PT20M\",\n      \"step\": [\n        {\n          \"@type\":
    \"HowToStep\",\n          \"name\": \"Step 1: Autenticazione e Setup dell'ambiente\",\n
    \         \"text\": \"Prima di poter interagire con le API, è necessario ottenere
    un token di autenticazione valido. Configura l'header 'Authorization' con il Bearer
    Token e imposta l'API Key corretta per l'ambiente (sandbox o produzione).\",\n
    \         \"url\": \"https://docs.pagopa.it/piattaforma-notifiche/v2.4/how-to/gestire-avvisi-pagamento#step-1-autenticazione\"\n
    \       },\n        {\n          \"@type\": \"HowToStep\",\n          \"name\":
    \"Step 2: Creazione di un nuovo avviso di pagamento\",\n          \"text\": \"Effettua
    una richiesta POST all'endpoint `/v1/payment-notices`. Il body della richiesta
    deve contenere i dati dell'avviso, come l'importo, la causale e i dati del debitore,
    in formato JSON.\",\n          \"itemListElement\": [\n            {\n              \"@type\":
    \"HowToDirection\",\n              \"text\": \"Esempio di payload per la creazione:
    `{ \\\"amount\\\": 150.50, \\\"recipient\\\": { ... }, \\\"reason\\\": \\\"Pagamento
    TARI 2024\\\" }`\"\n            },\n            {\n              \"@type\": \"HowToTip\",\n
    \             \"text\": \"Conserva l'ID dell'avviso restituito dalla API per le
    operazioni successive.\"\n            }\n          ],\n          \"url\": \"https://docs.pagopa.it/piattaforma-notifiche/v2.4/how-to/gestire-avvisi-pagamento#step-2-creazione\"\n
    \       },\n        {\n          \"@type\": \"HowToStep\",\n          \"name\":
    \"Step 3: Aggiornamento di un avviso esistente\",\n          \"text\": \"Per modificare
    un avviso, invia una richiesta PUT all'endpoint `/v1/payment-notices/{noticeId}`.
    È possibile aggiornare solo avvisi in stato 'PENDING'.\",\n          \"url\":
    \"https://docs.pagopa.it/piattaforma-notifiche/v2.4/how-to/gestire-avvisi-pagamento#step-3-aggiornamento\"\n
    \       }\n      ]\n    },\n    {\n      \"@type\": \"BreadcrumbList\",\n      \"itemListElement\":
    [\n        {\n          \"@type\": \"ListItem\",\n          \"position\": 1,\n
    \         \"name\": \"Documentazione\",\n          \"item\": \"https://docs.pagopa.it/\"\n
    \       },\n        {\n          \"@type\": \"ListItem\",\n          \"position\":
    2,\n          \"name\": \"Piattaforma Notifiche\",\n          \"item\": \"https://docs.pagopa.it/piattaforma-notifiche/\"\n
    \       },\n        {\n          \"@type\": \"ListItem\",\n          \"position\":
    3,\n          \"name\": \"v2.4\",\n          \"item\": \"https://docs.pagopa.it/piattaforma-notifiche/v2.4/\"\n
    \       },\n        {\n          \"@type\": \"ListItem\",\n          \"position\":
    4,\n          \"name\": \"Guide\",\n          \"item\": \"https://docs.pagopa.it/piattaforma-notifiche/v2.4/how-to/\"\n
    \       },\n        {\n          \"@type\": \"ListItem\",\n          \"position\":
    5,\n          \"name\": \"Come gestire gli avvisi di pagamento\",\n          \"item\":
    \"https://docs.pagopa.it/piattaforma-notifiche/v2.4/how-to/gestire-avvisi-pagamento\"\n
    \       }\n      ]\n    },\n    {\n      \"@type\": \"FAQPage\",\n      \"mainEntity\":
    [\n        {\n          \"@type\": \"Question\",\n          \"name\": \"Quali
    sono gli stati possibili di un avviso di pagamento?\",\n          \"acceptedAnswer\":
    {\n            \"@type\": \"Answer\",\n            \"text\": \"Gli stati principali
    sono: PENDING (in attesa di pagamento), PAID (pagato), EXPIRED (scaduto), e CANCELED
    (annullato). Ogni stato determina le operazioni che è possibile eseguire sull'avviso.\"\n
    \         }\n        },\n        {\n          \"@type\": \"Question\",\n          \"name\":
    \"Cosa succede se provo a modificare un avviso già pagato?\",\n          \"acceptedAnswer\":
    {\n            \"@type\": \"Answer\",\n            \"text\": \"L'API restituirà
    un errore con codice di stato `409 Conflict`, indicando che l'operazione non è
    permessa sullo stato attuale della risorsa.\"\n          }\n        }\n      ]\n
    \   }\n  ]\n}"
  prodotto: Piattaforma Notifiche
  search_boost: 1.3
  tags:
  - avvisi
  - pagamenti
  - api
  - crud
  - piattaforma notifiche
  titolo: Come gestire gli avvisi di pagamento
  versione: v2.4
audience:
  experienceLevel: intermediate
  primaryRole: Documentation Specialist
document:
  summary: Defines a neutral blueprint for generating YAML frontmatter and Schema.org
    JSON-LD to enrich technical documentation.
  title: Metadata playbook
  topics:
  - YAML
  - frontmatter
  - Schema.org
  - JSON-LD
  type: Playbook
funzione: genera_frontmatter_avanzato
metadata:
  keywords:
  - frontmatter
  - YAML
  - Schema.org
  - JSON-LD
  - metadata
schema:
  '@context': https://schema.org
  '@type': TechArticle
  audience:
    '@type': Audience
    audienceType: Documentation Specialist
  description: Defines a neutral blueprint for generating YAML frontmatter and Schema.org
    JSON-LD to enrich technical documentation.
  inLanguage: it
  keywords:
  - frontmatter
  - YAML
  - Schema.org
  - JSON-LD
  - metadata
  learningResourceType: Playbook
  name: Metadata playbook
  proficiencyLevel: intermediate
---

# Metadata playbook

This knowledge base defines a neutral blueprint for generating YAML frontmatter and Schema.org JSON-LD.

## Frontmatter blueprint
```yaml
frontmatter_blueprint:
  document:
    title: required
    summary: required
    type: required
    topics: optional_list
  audience:
    primaryRole: required
    additionalRoles: optional_list
    experienceLevel: optional
  lifecycle:
    status: optional
    lastUpdated: optional
  metadata:
    keywords: optional_list
    relatedResources: optional_list
```

- Treat `required` fields as mandatory. If a value cannot be inferred, provide the best concise description based on the Markdown source.
- `optional_list` indicates that the field should appear only when information is available; otherwise omit the key entirely.
- Use domain-specific vocabulary for `document.type` and `audience.primaryRole` derived from the document itself.
- Keep `summary` under 30 words when possible.

## Taxonomy guidance
- Prefer verbs or task-oriented nouns for `document.type` when the content describes procedures (e.g., `How-To`, `Tutorial`).
- Use technology names, platform components, or conceptual topics for `document.topics`.
- Choose `audience.experienceLevel` from `beginner`, `intermediate`, or `advanced` when the document implies a clear skill expectation.

## Schema hints
```yaml
schema_hints:
  preferred_types:
    - TechArticle
    - Article
    - HowTo
  common_properties:
    - name
    - description
    - inLanguage
    - keywords
    - learningResourceType
    - audience
  audience_template:
    "@type": "Audience"
    "audienceType": <role inferred from audience.primaryRole>
```

- Select the Schema.org `@type` that best matches the Markdown content while staying within the `preferred_types` list when applicable.
- Map `audience.primaryRole` into the `audience` property using the `audience_template`.
- Include additional properties only when explicitly supported by the retrieved Schema.org definitions.