---
layout: post
title: "Collegare EspoCRM ai sistemi aziendali"
date: 2026-10-20
lang: it
locale: it_IT
permalink: /it/blog/espo-da-una-parte/
alt: /en/blog/espo-on-one-side/
description: "Come Nesso separa canali e regole per configurare il trasferimento dei dati tra EspoCRM e i sistemi esterni."
image: /assets/images/blog/ch1-two-sides.webp
image_sm: /assets/images/blog/ch1-two-sides-640.webp
image_alt: "Fogli da una parte, quattro quadrati in mezzo, un archivio scuro dall'altra."
series: giro
series_order: 1
author: Nesso
---

Quando clienti, contatti e richieste arrivano da fonti diverse, il primo problema è stabilire come portarli nel CRM e come mantenere gli aggiornamenti nel tempo. Nesso organizza questa configurazione in due elementi: il collegamento e l’integrazione.

## Il collegamento definisce il canale

Un sito web può inviare dati tramite webhook. Un gestionale può renderli disponibili in un database o in file CSV ed Excel. Un’applicazione esterna può ricevere aggiornamenti tramite HTTP. Il collegamento contiene le impostazioni necessarie per comunicare attraverso il canale scelto.

## L’integrazione definisce le regole

L’integrazione stabilisce quale scheda di EspoCRM aggiornare, quale codice identifica ciascun record e come associare le colonne ai campi. Comprende anche la frequenza delle esecuzioni e le regole di aggiornamento.

Uno stesso collegamento può servire più integrazioni. Per esempio, i dati ricevuti da un sito possono alimentare Lead e Contatti attraverso due configurazioni distinte.

## EspoCRM resta l’ambiente di lavoro

Nesso legge e scrive su EspoCRM attraverso le API HTTP. Le schede e i record restano nel CRM. Il motore conserva le configurazioni e le informazioni operative necessarie a riconoscere i dati già elaborati e registrare i risultati.

Anche le schede personalizzate possono essere incluse nei flussi, in base a ciò che è disponibile nella propria installazione.

## Dalla configurazione alla verifica

Prima di attivare il trasferimento, l’anteprima permette di esaminare le modifiche previste. La demo locale Gruppo Meridia offre un ambiente con dati fittizi per esplorare questo percorso.

Per iniziare, consulta [come funziona Nesso](/it/come-funziona/) e le istruzioni nel [repository del prodotto](https://github.com/nessocrm/nessocrm).
