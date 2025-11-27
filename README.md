---
funzione:
  descrizione: Guida completa per gli Enti Creditori sull'integrazione con il Nodo
    dei Pagamenti-SPC della Piattaforma pagoPA, illustrando i passaggi e le primitive
    necessarie.
  diataxis:
    primary_audience:
    - Sviluppatori
    - Integratori
    secondary_audience:
    - Architetti Software
    - Product Manager Tecnici
    tipo: how-to
  prodotto: Piattaforma pagoPA
  seo:
    canonical: https://docs.pagopa.it/piattaforma-pagopa/v3.6/guida-integrazione
    description: Scopri come integrare il tuo sistema con il Nodo dei Pagamenti-SPC
      di pagoPA. Guida passo-passo per Enti Creditori con dettagli sulle primitive
      e i requisiti.
    json-ld:
      '@context': https://schema.org
      '@type': HowTo
      about:
        '@type': SoftwareApplication
        applicationCategory: Finance
        name: Piattaforma pagoPA
        operatingSystem: Platform Independent
        softwareVersion: v3.6
      audience:
        '@type': Audience
        audienceType: Sviluppatori
        description: Enti Creditori che devono integrare i loro sistemi con la Piattaforma
          pagoPA.
      description: Una guida che descrive i passaggi necessari per un Ente Creditore
        per integrarsi con la Piattaforma pagoPA attraverso il Nodo dei Pagamenti-SPC.
      isPartOf:
        '@type': WebSite
        name: Documentazione Piattaforma pagoPA
        url: https://docs.pagopa.it
      name: Guida all'integrazione con il Nodo dei Pagamenti-SPC
      provider:
        '@type': Organization
        logo:
          '@type': ImageObject
          url: https://docs.pagopa.it/assets/logo-pagopa.svg
        name: PagoPA S.p.A.
      step:
      - '@type': HowToStep
        name: Comprensione dell'Architettura
        text: Comprendere il ruolo del Nodo dei Pagamenti-SPC come componente centrale
          della Piattaforma pagoPA per la gestione dei flussi di pagamento e consultare
          il Glossario per la terminologia.
        url: https://docs.pagopa.it/piattaforma-pagopa/glossario
      - '@type': HowToStep
        name: Consultazione della Documentazione SANP
        text: Analizzare in dettaglio il documento SANP (Standard di Attuazione del
          Nodo dei Pagamenti) che definisce le specifiche tecniche, i tracciati e
          le regole di comunicazione.
        url: https://docs.pagopa.it/piattaforma-pagopa/sanp
      - '@type': HowToStep
        name: Implementazione delle Primitive SOAP
        text: Implementare le chiamate SOAP verso il Nodo utilizzando le primitive
          necessarie, come 'nodoInviaCarrelloRPT' per richieste con carrello e 'nodoInviaRPT'
          per richieste singole, basandosi sui WSDL forniti.
        url: https://docs.pagopa.it/piattaforma-pagopa/api/soap/weds
      - '@type': HowToStep
        name: Gestione degli Avvisi di Pagamento
        text: Integrare la logica per la creazione e la gestione degli Avvisi di Pagamento,
          che rappresentano lo strumento di base per avviare una transazione sulla
          piattaforma.
        url: https://docs.pagopa.it/piattaforma-pagopa/avvisi-di-pagamento
      tool:
      - '@type': HowToTool
        description: Un client in grado di effettuare chiamate SOAP per comunicare
          con gli endpoint del Nodo dei Pagamenti-SPC.
        name: SOAP Client
      - '@type': HowToTool
        description: File WSDL forniti da PagoPA per la definizione dei servizi web.
        name: WSDL
      totalTime: PT8H
    keywords:
    - integrazione
    - Nodo dei Pagamenti-SPC
    - Ente Creditore
    - RPT
    - nodoInviaCarrelloRPT
    - nodoInviaRPT
    - API
    - SOAP
    - pagoPA
    title: Guida all'integrazione con Nodo dei Pagamenti | Piattaforma pagoPA
  titolo: Guida all'integrazione
  versione: v3.6
---

# gpl-open-source
GPLv3 Open Source Project