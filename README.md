---
audience:
  primaryRole: Developer
descrizione: Questa guida illustra i passaggi necessari per aggiornare in sicurezza
  il modulo di pagamento pagoPA sulla tua piattaforma e-commerce, garantendo la continuità
  del servizio.
document:
  summary: A description of a project licensed under the GPLv3 open source license.
  title: GPLv3 Open Source Project
  topics:
  - GPLv3
  - Open Source
  type: Overview
funzione: generazione_frontmatter
keywords:
- pagoPA
- modulo di pagamento
- aggiornamento
- e-commerce
- backup
- compatibilità
- script
- cache
last_update:
  author: Team Documentazione PagoPA
  date: '2023-10-26'
metadata:
  keywords:
  - GPLv3
  - Open Source
  - License
prodotto:
  nome: Piattaforma Notifiche
  versione: v1.0
quadrante: how-to
schema:
  '@context': https://schema.org
  '@type': TechArticle
  audience:
    '@type': Audience
    audienceType: Developer
  description: A description of a project licensed under the GPLv3 open source license.
  inLanguage: en
  keywords:
  - GPLv3
  - Open Source
  - License
  learningResourceType: Overview
  name: GPLv3 Open Source Project
seo:
  description: Segui la nostra guida dettagliata per aggiornare il modulo di pagamento
    pagoPA sul tuo e-commerce in modo sicuro. Passaggi chiari, dai prerequisiti alla
    verifica finale.
  json-ld: "{\n  \"@context\": \"https://schema.org\",\n  \"@type\": \"HowTo\",\n
    \ \"name\": \"Come aggiornare il modulo di pagamento pagoPA\",\n  \"description\":
    \"Guida passo-passo per aggiornare in sicurezza il modulo di pagamento pagoPA
    sul tuo e-commerce, dalla preparazione al test finale.\",\n  \"inLanguage\": \"it-IT\",\n
    \ \"learningResourceType\": \"how-to guide\",\n  \"provider\": {\n    \"@type\":
    \"Organization\",\n    \"name\": \"PagoPA S.p.A.\",\n    \"url\": \"https://www.pagopa.it/\"\n
    \ },\n  \"isPartOf\": {\n    \"@type\": \"Book\",\n    \"name\": \"Documentazione
    Piattaforma Notifiche\",\n    \"bookEdition\": \"v1.0\"\n  },\n  \"totalTime\":
    \"PT30M\",\n  \"estimatedCost\": {\n    \"@type\": \"MonetaryAmount\",\n    \"currency\":
    \"EUR\",\n    \"value\": \"0\"\n  },\n  \"step\": [\n    {\n      \"@type\": \"HowToSection\",\n
    \     \"name\": \"Prerequisiti\",\n      \"itemListElement\": [\n        {\n          \"@type\":
    \"HowToStep\",\n          \"position\": 1,\n          \"name\": \"Controllo Compatibilità\",\n
    \         \"text\": \"Controllare la compatibilità della nuova versione del modulo
    con la versione della tua piattaforma (es. PrestaShop, Magento, etc.) e con le
    versioni di PHP e MySQL in uso. Consulta il file README o la documentazione ufficiale.\"\n
    \       },\n        {\n          \"@type\": \"HowToStep\",\n          \"position\":
    2,\n          \"name\": \"Backup\",\n          \"text\": \"Fare un backup completo
    del sito e del database. Questo è un passaggio fondamentale per poter ripristinare
    la situazione precedente in caso di problemi.\"\n        }\n      ]\n    },\n
    \   {\n      \"@type\": \"HowToSection\",\n      \"name\": \"Procedura di Aggiornamento\",\n
    \     \"itemListElement\": [\n        {\n          \"@type\": \"HowToStep\",\n
    \         \"position\": 3,\n          \"name\": \"Download del Modulo\",\n          \"text\":
    \"Scaricare l'ultima versione del modulo di pagamento dal repository ufficiale
    o dal marketplace della tua piattaforma.\"\n        },\n        {\n          \"@type\":
    \"HowToStep\",\n          \"position\": 4,\n          \"name\": \"Modalità Manutenzione\",\n
    \         \"text\": \"Mettere il sito in modalità manutenzione per evitare che
    i clienti effettuino transazioni durante l'aggiornamento.\"\n        },\n        {\n
    \         \"@type\": \"HowToStep\",\n          \"position\": 5,\n          \"name\":
    \"Caricamento File\",\n          \"text\": \"Caricare i file del nuovo modulo
    via FTP o tramite il pannello di gestione del tuo e-commerce, sovrascrivendo i
    file esistenti.\"\n        },\n        {\n          \"@type\": \"HowToStep\",\n
    \         \"position\": 6,\n          \"name\": \"Esecuzione Script di Aggiornamento\",\n
    \         \"text\": \"Se previsto dalla documentazione del modulo, eseguire lo
    script di aggiornamento del database. Questo di solito avviene accedendo a una
    specifica URL o tramite un comando da shell.\",\n          \"tool\": {\n            \"@type\":
    \"HowToTool\",\n            \"name\": \"SSH o Pannello di Controllo Hosting\"\n
    \         }\n        }\n      ]\n    },\n    {\n      \"@type\": \"HowToSection\",\n
    \     \"name\": \"Verifica Finale\",\n      \"itemListElement\": [\n        {\n
    \         \"@type\": \"HowToStep\",\n          \"position\": 7,\n          \"name\":
    \"Svuotare la Cache\",\n          \"text\": \"Svuotare la cache della piattaforma
    e del browser per assicurarsi che vengano caricate le nuove versioni dei file.\"\n
    \       },\n        {\n          \"@type\": \"HowToStep\",\n          \"position\":
    8,\n          \"name\": \"Disattivare Manutenzione e Testare\",\n          \"text\":
    \"Disattivare la modalità manutenzione e verificare il corretto funzionamento
    del modulo effettuando una transazione di test in ambiente di collaudo o con un
    prodotto a basso costo.\"\n        }\n      ]\n    }\n  ]\n}"
  title: Come Aggiornare il Modulo di Pagamento pagoPA | Guida Sicura
titolo: Come aggiornare il modulo di pagamento pagoPA
---

# gpl-open-source
GPLv3 Open Source Project