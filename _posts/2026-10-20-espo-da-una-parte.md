---
layout: post
title: "Espo da una parte"
date: 2026-10-20
lang: it
locale: it_IT
permalink: /it/blog/espo-da-una-parte/
alt: /en/blog/espo-on-one-side/
description: "Nesso ha sempre Espo da una parte e un canale dall'altra. Il collegamento è il canale. L'integrazione è la regola."
image: /assets/images/blog/ch1-two-sides.webp
image_sm: /assets/images/blog/ch1-two-sides-640.webp
image_alt: "Fogli da una parte, quattro quadrati in mezzo, un archivio scuro dall'altra."
series: giro
series_order: 1
author: Nesso
---

Questa è la prima di quattro letture sullo stesso giro. Non racconta un cliente. Racconta una decisione già presa nel motore, e le conseguenze che quella decisione ha su un file di anagrafiche arrivato di notte. Il file è un esempio, lo stesso che la home del sito mostra in piccolo: una riga nuova, una riga invariata, una riga con una colonna mancante, una nota che una persona ha scritto su Espo e che il file non deve svuotare. I capitoli dopo entrano nella chiave, nella cella vuota e negli interruttori che restano spenti. Qui si ferma il confine: chi sta da una parte, chi sta dall'altra, e che cosa non attraversa.

Se una frase di questo diario e una frase del manuale divergono, vale il manuale. Il manuale sta nella cartella docs del repository pubblico, e cambia insieme al codice. Questo sito non lo ricompila. Il diario spiega il perché. Il manuale resta il testo che dice che cosa il programma fa oggi.

## La frase

Nesso ha sempre Espo da una parte. Dall'altra c'è un sistema esterno. In mezzo c'è un canale, una scheda e un abbinamento di campi. Il passaggio verso Espo usa le API HTTP di Espo, con l'header di autorizzazione che Espo si aspetta. Le tabelle di Espo non sono un'interfaccia. Non si aprono, non si aggiornano con una query, non si usano come una coda.

La frase è corta perché il prodotto è corto. Chi configura non scrive una stored procedure. Sceglie il canale, indica la scheda, dice quale colonna è l'identità e quale campo finisce dove, e decide ogni quanto il giro deve partire. Da lì lo stesso motore sposta i record, qualunque sia la scheda. Un webhook di un sito può alimentare i Lead. Una seconda integrazione, sullo stesso collegamento o su un altro, può alimentare i Contatti. Il motore non cambia mestiere quando cambia la scheda. Cambia la regola.

Il nome del sistema esterno non sta nel codice. Può essere un gestionale, un sito, una cartella di file, un database letto con una SELECT. Il prodotto non diventa quel nome. Se il nome entrasse nel codice, ogni cliente nuovo sarebbe una modifica del programma. Invece ogni cliente nuovo è una configurazione: un collegamento, una o più integrazioni, un abbinamento riletto da una persona.

## Due oggetti, non uno

Il collegamento è il canale. Tiene l'indirizzo, il modo di autenticarsi, il tipo di ingresso o di uscita. L'integrazione è la regola. Tiene la scheda, la colonna che fa da identità, l'abbinamento dei campi, la cadenza, il padrone di ciascun campo, e se la scrittura di ritorno è accesa. Di default quella scrittura è spenta. Il capitolo quattro spiega perché, e che cosa succede se qualcuno la accende.

Un'integrazione ha un solo collegamento. Un collegamento può avere più integrazioni. È la forma giusta per un file che di notte porta le anagrafiche e, in un secondo giro, le sedi. Le due regole non si mescolano, perché ciascuna ha la sua identità. La chiave contiene l'id dell'integrazione. Due file sulla stessa scheda Account restano due storie. Il capitolo due mostra come è fatta quella chiave. Qui basta sapere che la separazione è voluta: un collegamento solo, con una regola sola, obbligherebbe a infilare due mestieri nello stesso abbinamento, e il giorno in cui uno dei due file cambia colonna si romperebbero entrambi.

La direzione segue il canale. Se il collegamento è HTTP, l'integrazione esce da Espo: il cursore ricorda l'ultimo record mandato e il giro successivo manda solo quello che è cambiato. Se il collegamento è un webhook, una SELECT, un CSV, un Excel, un SFTP, un FTPS, un PDF il cui nome contiene la chiave dell'azienda, o un documento, l'integrazione entra. Una integrazione HTTP non diventa un caricamento. Una integrazione da file non diventa un'uscita. Cambiare direzione significa cambiare collegamento, non spuntare una casella nascosta dentro la stessa regola.

Questa separazione evita un errore comune. Si prende un file, lo si carica, e poi si vuole «rinviare le modifiche di Espo sullo stesso file» senza aver deciso quali colonne tornano indietro. In Nesso quel ritorno è un'altra decisione, spenta finché le colonne non sono nominate. Il canale di ingresso resta un canale di ingresso. Il ritorno, se un giorno si accende, scrive solo lì dove qualcuno ha indicato un nome di colonna.

## Il file di stanotte, come filo

Per non parlare a vuoto, i quattro capitoli usano lo stesso file. Si chiama, nel racconto, il file delle anagrafiche. Arriva di notte in una cartella. Ha una colonna con il codice esterno, una con il nome, una con la città, una con la partita IVA, una con una nota. Il codice esterno è l'identità. Il nome e la città e la partita IVA sono campi della sorgente. La nota, in questa integrazione, ha come padrone Espo, perché una persona del commerciale la scrive sul record e il file di notte non deve cancellarla.

Nel file di questa notte ci sono tre casi che bastano a vedere il giro.

La riga del codice C014 è identica all'ultima volta. L'hash della riga è già quello salvato. Espo non viene richiamato. Non c'è un aggiornamento da fare, e non c'è un motivo per toccare il record. Un secondo invio identico non duplica e non riscrive.

La riga del codice C001 non c'è ancora su Espo. Il giro la prepara come un Account nuovo. Nel racconto della home il nome è Nord Est e la città è Trieste. La chiave che nascerà sulla scheda standard è fatta dall'id dell'integrazione, due punti, e C001. Il campo, sulle schede che Espo ha già, si chiama cExternalKey. La nota, in creazione, si scrive lo stesso se il file la porta: il record non esiste ancora, e non c'è una nota di una persona da proteggere. Dal giro successivo il padrone conta, e il capitolo tre lo spiega con calma.

Una riga, la diciottesima del racconto, non ha una colonna obbligatoria. Il file non si sposta in elaborati. Lo scarto è uno solo, di file, non una coda di righe. Le altre righe non vengono fatte passare a metà. Manca invece una cella, e la colonna c'è: si scarta quella riga, e le altre proseguono. Sono due errori diversi. Il primo dice che il file non è quello atteso. Il secondo dice che una riga è incompleta. Trattarli allo stesso modo farebbe o bloccare tutto per una cella, o caricare un file troncato come se fosse intero.

C'è poi il caso che il file di questa notte non mostra, e che il capitolo tre tiene come centro: una riga che ieri c'era e stanotte non c'è più. Il record su Espo si chiude e resta nello storico. La prima volta che un giro chiuderebbe dei record, chiede conferma. Qui si anticipa solo il gesto, perché senza il confine di questo capitolo quel gesto sembrerebbe una cancellazione. Non lo è.

## Chi legge il giro

Quattro persone guardano lo stesso file, e non cercano la stessa cosa.

Chi tiene il numero guarda la home. Il numero delle anagrafiche allineate vale solo se il giro di oggi verso Account, in ingresso, è riuscito. Un successo di ieri non viene presentato come oggi. Se il giro fallisce, la percentuale non si mostra. Se un file è atteso entro un'ora e quell'ora passa senza un giro riuscito, il bordo si accende. Il numero è un controllo. Non scrive su Espo e non corregge il file.

Chi ha la nota è la persona del commerciale. Ha scritto sul record una frase che il file non conosce, o che il file porterebbe vuota. Il campo ha come padrone Espo. Il giro di notte non lo svuota. Se il file porta un valore diverso, quel valore finisce in una coda da guardare. Il badge sul record dice chi ha scritto per ultimo. Non è una cronologia legale. È il segno dell'ultimo giro che ha toccato il record, utile a chi deve capire se la riga è ancora quella del file.

Chi controlla apre l'anteprima prima della scrittura. Vede che cosa nascerebbe e che cosa cambierebbe. Una partita IVA già presente si vede prima del POST. L'annullamento torna indietro su quello che il giro ha scritto. La prima chiusura di record spariti chiede conferma proprio a questa persona, o a chi ha il compito di dire sì: un file troncato non chiude l'elenco da solo.

Chi installa fa quattro passi: collegamento, scheda, abbinamento, giro. La ricetta di anagrafiche, contatti, sedi o listino è un punto di partenza. Si rilegge. Non è un connettore certificato, e il nome del gestionale non è scritto nel programma. Il piano di accensione dice che cosa resta spento: la scrittura di ritorno, la coda di ritento, il filtro del portale, il sigillo dei segreti. La pagina di consegna non contiene le password. Senza la variabile NESSO_SECRET_KEY il volume le tiene in chiaro. Va detto a chi riceve la prova. Il capitolo quattro è tutto questo, con i dettagli. Qui entra solo come parte del confine: chi installa consegna un giro, non un secondo gestionale.

## Schede, non un secondo archivio

Le schede stanno in Espo. Il motore non inventa nomi di entità. Legge le schede che questa installazione espone. Account, Contatto, Lead, Opportunità, Caso, Compito, Riunione, Chiamata e Documento sono schede standard, quando ci sono. Su quelle la chiave esterna è il campo custom cExternalKey.

Se la scheda non esiste, Nesso può crearla via API. Si indicano il singolare e il plurale. Espo mette il prefisso C. I campi della scheda nuova non ricevono un secondo prefisso. La chiave, su una scheda creata qui, si chiama externalKey. Una scheda creata qui è una scheda Espo. La vede chi ha il team. Non è un archivio parallelo tenuto nel file SQLite del motore.

Il file SQLite è la memoria del motore: collegamenti, integrazioni, hash, cursore, giornale. Non sostituisce Espo e non è un secondo CRM. Le anagrafiche non «vivono» lì. Lì vive il ricordo di quale riga è già stata vista e di quale record è già stato mandato. Sono due memorie diverse, e il capitolo due le separa. Confonderle è il modo in cui un caricamento riscrive tutto ogni notte, o un'uscita rimanda gli stessi record all'infinito.

Il team e la persona assegnata arrivano da una colonna del file o da un team fisso. La visibilità è una regola di Espo: questa riga è del team Vendite, assegnata a questa persona. Nesso non inventa un permesso fuori da Espo. Gli utenti di Espo non si creano da un'anagrafica. Una colonna di nomi di persone non diventa un elenco di login. Creare un utente è un gesto di amministrazione, con una password e un ruolo. Un file di clienti non ha quel gesto dentro.

Il listino della ricetta punta alla scheda Product. Se questa installazione non ha la scheda, i campi del listino restano vuoti. La ricetta non inventa il catalogo. È un limite onesto: meglio un abbinamento vuoto, visibile, che un Product fantasma creato per far tornare i conti di una slide.

## Che cosa non attraversa

La posta del CRM resta in Espo. Nesso non diventa il programma che legge la casella e non diventa il programma che spedisce. Chi ha già la posta configurata in Espo la lascia lì. Aggiungere un canale di posta «perché tanto siamo in mezzo» mescolerebbe due mestieri e due segreti. Il segreto di una casella non è il segreto di un file di anagrafiche.

L'Advanced Pack non viene riscritto. Non sta nel repository. Se qualcuno lo ha in locale, resta locale. Il motore non lo pubblica e non lo copia insieme ai dati di una installazione vera. Il confine è lo stesso dei dump: la prova parte vuota.

I dump di produzione non si importano nell'Espo di prova. Non si montano, non si copiano gli allegati, non si usa il backup come database di sviluppo. Un Espo vuoto è la prova. Un dump è un'altra cosa: contiene persone, note, file, e una storia che non ha chiesto di finire su un portatile. Il repository pubblico alza, con Docker Compose, il database, un Espo vuoto e il motore. Questa pagina non raccoglie email e non apre un account. Il contatto è il repository.

Non esiste un giro senza Espo. Il prodotto non è un ponte generico fra due sistemi qualsiasi. Togliere Espo da una parte e mettere «qualunque cosa» dall'altra farebbe un altro programma, con un altro nome. La frase di apertura è anche un rifiuto di quella generalizzazione. Il canale può cambiare. Il lato Espo no.

## Uno script, una query, un secondo CRM

Uno script legge il CSV e fa un inserimento. Il giorno dopo il file ha una riga in meno e lo script cancella, oppure lascia il record e nessuno sa che la sorgente non lo ha più. Non c'è anteprima. Non c'è un hash, quindi riscrive anche la riga che non è cambiata. Se la nota del commerciale sta nella stessa tabella, lo script la svuota quando la cella arriva vuota. Non ha un padrone del campo. Funziona la prima notte. La seconda notte è già un incidente, solo che l'incidente ha la forma di un successo: il comando è uscito con codice zero.

Una query sulle tabelle di Espo salta i controlli, i team, la storia e gli hook. Il giorno in cui Espo cambia uno schema, la query è il primo pezzo che si rompe, e si rompe in silenzio: la colonna c'è ancora, il significato no. Nesso parla con Espo solo via HTTP. La chiave, il team e la chiusura passano dalle API. Il database di Espo non è un canale, nemmeno «solo per leggere». La lettura di una scheda è una chiamata. La scrittura di una scheda è una chiamata. Il cursore di uscita ricorda l'ultimo modifiedAt e l'id, e avanza solo dopo i POST riusciti. Se manca la chiave esterna, il pull si ferma: i record dopo non escono. Anche questo è nel capitolo due. Qui serve a dire che la cautela sta nel protocollo, non in una query più attenta.

Un secondo CRM tiene le anagrafiche in un altro prodotto e poi le rincorre in Espo. La verità si sdoppia. Una correzione fatta di là non è la correzione fatta di qua, e il lunedì mattina si sceglie a sentimento quale delle due è «quella vera». Nesso non è quel secondo posto. Ha sempre Espo da una parte. L'altro lato è un canale: un file, una SELECT, una chiamata. La verità dei campi della sorgente, di default, è la sorgente, compresa la cella vuota. L'eccezione è nominata campo per campo, ed è il padrone Espo. Non c'è una terza verità nel mezzo, tenuta «per sicurezza» nel file del motore.

## Le ricette e la demo

Anagrafiche, contatti, sedi e listino sono quattro punti di partenza. Ognuno nomina una scheda e delle colonne. Non scrivono da soli. Non certificano che il sistema dall'altra parte si chiami in un modo preciso. Proponi l'abbinamento legge i nomi delle colonne, nella lingua della pagina, e propone il campo Espo, compresa la partita IVA se la scheda ha un campo fiscale. Una colonna non riconosciuta resta vuota, da compilare a mano. I sinonimi sono un elenco. Non escono in rete. Non salvano l'integrazione. La persona rivede e poi salva.

Completa le colonne vuote chiama un modello solo se un indirizzo è impostato. Riempie le colonne ancora vuote, fra i campi che la scheda conosce. Non tocca una colonna già abbinata. Non salva. La chiamata manda i nomi delle colonne, al massimo tre celle corte, e il nome del campo. Non manda la password del collegamento. L'indirizzo del modello non entra nello scarico della configurazione. Senza indirizzo non parte nessuna chiamata, e la proposta per sinonimi resta. Il modello non sceglie il canale, non crea le schede, non accende la scrittura di ritorno. Il giornale di un giro e il pianificatore restano nella lingua del giro. Il modello non li riscrive.

La demo del Gruppo Meridia, nel manuale, è la prova di un giro. Non è un secondo prodotto e non è un cliente pubblicato su questo sito. Nominarla qui serve a non lasciarla aleggiare come un caso commerciale. È un Espo di prova, con dei giri descritti nel manuale, utile a chi vuole vedere la forma di un caricamento prima di mettere i propri file. I quattro flussi del backup da cui è nata l'idea — il sito, i file di notte, le anagrafiche, i lavori — non sono codice. Diventano, se servono, delle configurazioni. Non sono quattro programmi dentro Nesso.

## Il giro, senza ancora i dettagli

La cadenza è a mano, cinque minuti, quindici, un'ora, o un orario fisso. Un'integrazione in pausa viene saltata dal pianificatore e dal webhook. Esegui ora no: quello parte perché una persona lo ha chiesto. La stessa integrazione non parte due volte. La seconda riceve che un'esecuzione è già in corso. Due integrazioni diverse possono girare insieme. Se una è già in corso, il pianificatore la salta e non scrive un errore ogni trenta secondi.

Dopo un errore l'orologio si aggiorna e si aspetta l'intervallo intero. Solo con retry_failed acceso l'orologio resta fermo, e il giro può ripresentarsi prima. È una scelta, spenta di default. Un errore non è un invito a martellare Espo. È un invito a leggere il giornale, che resta nella lingua in cui il giro è stato lanciato. La pagina può essere in italiano o in inglese. Il giornale no, non si traduce a posteriori.

L'anteprima non scrive. La modalità lettura e l'interruttore generale fermano le scritture. Un giro in lettura legge, confronta, e non manda il POST. Sono i freni. Stanno nel capitolo quattro insieme alla coda, al portale e al sigillo, perché sono tutti dello stesso tipo: esistono, e di default non cambiano un giro che già funziona.

## La pagina, il giornale, la lingua

La pagina con cui si configura il giro è in italiano o in inglese. La scelta è della pagina, non del file. Un file di anagrafiche non ha una lingua del prodotto: ha delle colonne, e i nomi di quelle colonne vengono letti nella lingua della pagina quando si chiede la proposta di abbinamento. Un nome di colonna italiano e un nome di colonna inglese possono proporre lo stesso campo, perché i sinonimi sono un elenco per lingua. La proposta non salva. Chi conferma è una persona, e la conferma è il salvataggio.

Il giornale di un giro resta nella lingua del giro. Se il giro è partito da una pagina in italiano, le frasi del giornale restano in italiano anche se il giorno dopo si apre la pagina in inglese. Non è una svista. Il giornale è il verbale di quell'esecuzione, non una brochure da riallineare. Tradurlo a posteriori farebbe due verbali. Il pianificatore, allo stesso modo, parla la lingua in cui è stato impostato. Chi legge un errore alle sette del mattino deve leggere la frase che il motore ha scritto, non una parafrasi.

Questo diario, invece, esiste due volte, in italiano e in inglese, perché è una spiegazione e non un verbale. I due testi dicono gli stessi fatti. Non dicono che il giornale farà lo stesso. Se si cerca nel giornale la frase di questo capitolo, non la si trova: il giornale dice che cosa è successo a una riga, non perché il prodotto ha due oggetti.

## Due integrazioni sullo stesso Account

Vale la pena vedere, prima dei capitoli tecnici, un caso che il confine rende possibile e che uno script unico rende confuso. Lo stesso Espo, la stessa scheda Account, due file. Il primo è il file delle anagrafiche, con il codice cliente. Il secondo è il file delle sedi, con il codice sede. Se finissero nella stessa integrazione, la colonna identità sarebbe una sola, e un codice sede verrebbe letto come un codice cliente, o il contrario. Con due integrazioni, la chiave dell'anagrafica contiene l'id della prima, la chiave della sede contiene l'id della seconda. Entrambe possono vivere su Account. Non si sovrascrivono, perché la chiave intera è diversa anche quando il valore esterno, per caso, è la stessa stringa.

Il collegamento può essere lo stesso, se i due file arrivano dallo stesso canale, per esempio la stessa cartella o lo stesso SFTP. Può essere diverso, se le anagrafiche arrivano da un CSV e le sedi da una SELECT. L'integrazione non eredita la direzione da un'opinione: la eredita dal collegamento a cui è attaccata. Attaccare l'integrazione delle sedi a un collegamento HTTP la farebbe uscire da Espo, non entrare. È un errore di configurazione visibile, non una sorpresa a runtime scritta in un commento.

La persona che installa tiene le due regole affiancate e le accende una alla volta. Prima le anagrafiche, con l'anteprima. Poi le sedi, con l'anteprima. Il numero in home, quello delle anagrafiche allineate, conta i giri in ingresso verso Account. Un giro delle sedi verso Account entra in quel conto se è un ingresso verso Account. Va saputo, così un successo delle sedi non viene scambiato per il successo del file clienti, e un fallimento del file clienti non viene coperto da un giro di sedi andato a buon fine la stessa mattina. Il numero è uno. I giri sono tanti. Il capitolo sul giro, più avanti, dice quando il numero ha il diritto di comparire.

## Il lunedì mattina

Il confine si giudica il lunedì, non la sera in cui il file è stato caricato la prima volta. La prima sera uno script e Nesso si assomigliano: le righe nuove diventano record. Il lunedì il file ha una riga in meno, una cella svuotata, una nota scritta a mano il venerdì, e una persona che chiede se «il sistema ha aggiornato». La risposta dipende da dove sta la verità.

Se la verità è una query scritta una volta, la risposta è «ha fatto quello che c'era scritto», e quello che c'era scritto non nominava la nota. Se la verità è un secondo archivio, la risposta è «dipende da quale dei due hai guardato». Se la verità è questo confine, la risposta è più lunga e più utile. I campi della sorgente sono quelli del file di stanotte, compresi i vuoti. I campi il cui padrone è Espo sono quelli lasciati dalla persona. I record la cui riga non c'è più sono chiusi, se qualcuno ha confermato la prima chiusura, e restano nello storico. Il file già elaborato non viene riletto. Il file atteso che non è arrivato ha acceso il bordo, e il numero in home non mente sull'ora.

Nessuna di queste risposte richiede di aprire le tabelle. Si leggono dal giornale, dall'anteprima, dal badge. Il confine è anche questo: il lunedì si ragiona su oggetti che una persona può nominare, non su una colonna di un database che solo chi ha scritto lo script ricorda.

## Che cosa questo capitolo non ha fatto

Non ha descritto il formato della chiave carattere per carattere: lo fa il secondo capitolo, insieme all'hash e al cursore, che sono le due memorie. Non ha detto che cosa succede, campo per campo, quando la cella arriva vuota: lo fa il terzo, insieme alla chiusura del record sparito. Non ha acceso niente. La scrittura di ritorno, la coda, il filtro del portale e il sigillo restano spenti anche alla fine del quarto capitolo, perché spenti è il comportamento della prova e il comportamento di un'installazione che non ha ancora deciso altrimenti.

Il file di stanotte, alla fine di questo confine, è ancora un file. C001 non è ancora un Account. C014 non è ancora stata riconosciuta come invariata. La riga senza colonna non è ancora uno scarto. I capitoli dopo fanno quei gesti, uno per volta, senza spostare Espo dall'altra parte e senza dare al file un nome di prodotto.

Una ultima distinzione, prima di passare alla chiave. Il confine non è una preferenza di stile. È il motivo per cui il motore può restare lo stesso quando cambia il file. Se il confine fosse «Nesso parla con il gestionale X», il capitolo dopo sarebbe un elenco di campi di quel gestionale, e il giorno in cui il file cambia nome di colonna si riscriverebbe il programma. Il confine è «Nesso parla con Espo da una parte e con un canale dall'altra». Il capitolo dopo può allora parlare di una chiave, di un hash e di un cursore, senza chiedere come si chiama il sistema che ha posato il file nella cartella. Il nome resta fuori. La regola resta dentro.
