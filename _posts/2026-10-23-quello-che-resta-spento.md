---
layout: post
title: "Attivare un’integrazione con controlli e verifiche"
date: 2026-10-23
lang: it
locale: it_IT
permalink: /it/blog/quello-che-resta-spento/
alt: /en/blog/what-stays-off/
description: "Anteprima, sola lettura e opzioni da configurare prima di collegare Nesso ai sistemi aziendali."
image: /assets/images/blog/ch4-switches-off.webp
image_sm: /assets/images/blog/ch4-switches-off-640.webp
image_alt: "Quattro interruttori spenti accanto a un foglio ancora da leggere."
series: giro
series_order: 4
author: Nesso
---

La prima importazione è solo una parte del lavoro. Prima di automatizzare un flusso occorre verificare i dati, decidere quali modifiche consentire e sapere come fermare le scritture.

## Esamina le modifiche previste

L’anteprima mostra l’impatto dell’elaborazione: record da creare, aggiornare o chiudere, errori e differenze da controllare. La prova a secco consente di verificare un campione senza scrivere su EspoCRM.

La modalità di sola lettura blocca le scritture della singola integrazione. È disponibile anche un blocco generale delle scritture verso il CRM.

## Procedi per attivazioni successive

Il piano di attivazione permette di introdurre i flussi progressivamente dopo averne verificato le anteprime. È utile quando un’integrazione dipende dai dati di un’altra, per esempio quando i contatti devono essere associati alle aziende già importate.

## Valuta le opzioni separatamente

La scrittura di ritorno al database esterno richiede un’attivazione esplicita ed è limitata alle colonne indicate. La coda dei nuovi tentativi e il filtro per team sono altre opzioni da configurare in base al processo.

La protezione delle credenziali salvate richiede la variabile NESSO_SECRET_KEY. La demo non la imposta: le credenziali nel volume locale restano quindi in chiaro. Questo requisito va affrontato prima di usare credenziali aziendali.

## Monitora dopo l’avvio

La schermata Attività raccoglie gli esiti e le righe scartate. Puoi impostare soglie di inattività e orari entro cui attendere i file. Gli avvisi sono visibili nell’applicazione; il motore non invia attualmente notifiche email.

La demo con dati fittizi permette di esplorare questi controlli. Per l’adozione, verifica requisiti e limiti nel manuale e prepara configurazione e backup del tuo ambiente.

Consulta [Controlli e verifiche](/it/rischio/) per una panoramica delle funzioni.
