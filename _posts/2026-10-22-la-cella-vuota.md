---
layout: post
title: "Aggiornare i dati senza sovrascrivere le note del team"
date: 2026-10-22
lang: it
locale: it_IT
permalink: /it/blog/la-cella-vuota/
alt: /en/blog/the-empty-cell/
description: "Come definire la priorità dei campi e gestire i valori vuoti nelle importazioni verso EspoCRM."
image: /assets/images/blog/ch3-empty-cell.webp
image_sm: /assets/images/blog/ch3-empty-cell-640.webp
image_alt: "Una cella di città vuota e una nota che resta sul record."
series: giro
series_order: 3
author: Nesso
---

Un file del gestionale e un record del CRM possono contenere informazioni diverse. La ragione sociale potrebbe essere aggiornata dal gestionale, mentre la nota commerciale viene curata direttamente dal team. Per automatizzare il trasferimento serve una regola per ciascun campo.

## Quando prevale il sistema esterno

Per impostazione predefinita, Nesso applica il valore ricevuto dalla sorgente. Questa regola comprende i valori vuoti: una cella vuota può svuotare il campo corrispondente in EspoCRM.

È un comportamento da verificare. Può essere corretto per un dato di cui il gestionale è il riferimento, ma non per un’informazione che deve essere conservata nel CRM.

## Quando prevale EspoCRM

Puoi assegnare a EspoCRM la priorità su un campo. Per i record esistenti, Nesso conserva il valore del CRM e raccoglie le differenze per la verifica.

Per esempio, se la nota commerciale è gestita in EspoCRM, un’importazione successiva non la sostituisce con la nota diversa o vuota del file. Alla creazione di un nuovo record, il valore iniziale può comunque arrivare dalla sorgente.

## Quando un record manca dal file

L’assenza di un’intera riga è distinta da un campo vuoto. Se è configurata la gestione delle assenze e la scheda dispone di uno stato compatibile, Nesso può chiudere i record non più presenti nella sorgente.

La prima chiusura richiede conferma. Il record resta nello storico: questa operazione non equivale alla cancellazione dei dati personali.

## Una verifica da fare con chi usa il CRM

Prima di attivare il flusso, concorda quali campi dipendono dal gestionale e quali vengono gestiti dal team. Controlla poi l’anteprima con un esempio che contenga valori diversi, celle vuote e record assenti.

La pagina [Regole di aggiornamento](/it/coperture/) riepiloga le scelte disponibili.
