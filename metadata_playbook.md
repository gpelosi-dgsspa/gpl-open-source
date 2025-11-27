---
funzione:
  descrizione: 'Guida passo-passo per integrare le API della Piattaforma Notifiche:
    prerequisiti, autenticazione JWT e uso degli endpoint principali.'
  diataxis: how-to
  json-ld: "{\n  \"@context\": \"https://schema.org\",\n  \"@graph\": [\n    {\n      \"@type\":
    \"Organization\",\n      \"@id\": \"https://www.pagopa.it/#organization\",\n      \"name\":
    \"PagoPA S.p.A.\",\n      \"url\": \"https://www.pagopa.it/\",\n      \"logo\":
    {\n        \"@type\": \"ImageObject\",\n        \"url\": \"https://www.pagopa.it/static/logo-pagopa-spa-652f1b8c47a064883307b22a10672722.svg\"\n
    \     }\n    },\n    {\n      \"@type\": \"HowTo\",\n      \"name\": \"Come Integrare
    l'API della Piattaforma Notifiche di PagoPA\",\n      \"description\": \"Guida
    passo-passo per integrare le API della Piattaforma Notifiche: prerequisiti, autenticazione
    JWT e uso degli endpoint principali.\",\n      \"author\": {\n        \"@id\":
    \"https://www.pagopa.it/#organization\"\n      },\n      \"publisher\": {\n        \"@id\":
    \"https://www.pagopa.it/#organization\"\n      },\n      \"datePublished\": \"2023-10-26\",\n
    \     \"dateModified\": \"2023-10-27\",\n      \"about\": {\n        \"@type\":
    \"SoftwareApplication\",\n        \"name\": \"Piattaforma Notifiche\",\n        \"softwareVersion\":
    \"v2.10\",\n        \"applicationCategory\": \"FinTech\",\n        \"operatingSystem\":
    \"Web Platform\",\n        \"url\": \"https://www.pagopa.it/it/prodotti-e-servizi/piattaforma-notifiche/\",\n
    \       \"publisher\": {\n          \"@id\": \"https://www.pagopa.it/#organization\"\n
    \       }\n      },\n      \"proficiencyLevel\": \"Intermediate\",\n      \"tool\":
    [\n        {\n          \"@type\": \"HowToTool\",\n          \"name\": \"API Key
    di Piattaforma Notifiche\"\n        },\n        {\n          \"@type\": \"HowToTool\",\n
    \         \"name\": \"Client HTTP (es. cURL, Postman)\"\n        }\n      ],\n
    \     \"step\": [\n        {\n          \"@type\": \"HowToStep\",\n          \"name\":
    \"Verifica dei Prerequisiti\",\n          \"text\": \"Assicurati di possedere
    una API key valida fornita da PagoPA e di aver configurato l'ambiente di sandbox.\",\n
    \         \"position\": 1,\n          \"url\": \"#prerequisiti\"\n        },\n
    \       {\n          \"@type\": \"HowToStep\",\n          \"name\": \"Ottenimento
    del Token di Autenticazione\",\n          \"text\": \"Esegui una richiesta POST
    all'endpoint di autenticazione per ottenere un token JWT. Il token deve essere
    incluso nell'header 'Authorization' di tutte le richieste successive e ha una
    validità di 60 minuti.\",\n          \"position\": 2,\n          \"url\": \"#autenticazione\",\n
    \         \"itemListElement\": [\n            {\n              \"@type\": \"HowToDirection\",\n
    \             \"text\": \"Invia una richiesta POST a https://api.sandbox.notifichedigitali.pagopa.it/v1/auth/token
    con il tuo client_id e api_key.\"\n            }\n          ]\n        },\n        {\n
    \         \"@type\": \"HowToStep\",\n          \"name\": \"Utilizzo degli Endpoint
    Principali\",\n          \"text\": \"Usa gli endpoint dell'API per inviare e recuperare
    lo stato delle notifiche, includendo sempre il token JWT nell'header 'Authorization'.\",\n
    \         \"position\": 3,\n          \"url\": \"#endpoint-principali\",\n          \"itemListElement\":
    [\n            {\n              \"@type\": \"HowToDirection\",\n              \"text\":
    \"Per inviare una notifica, usa l'endpoint POST /v1/notifications.\"\n            },\n
    \           {\n              \"@type\": \"HowToDirection\",\n              \"text\":
    \"Per recuperare lo stato di una notifica, usa l'endpoint GET /v1/notifications/{notificationId}.\"\n
    \           }\n          ]\n        }\n      ]\n    }\n  ]\n}"
  livello: Intermedio
  prodotto: Piattaforma Notifiche
  stato: pubblicato
  titolo: Guida all'Integrazione dell'API di Notifica
  ultima_modifica: '2023-10-27'
  versione: v2.10
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