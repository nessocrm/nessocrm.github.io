---
layout: post
title: "Quello che resta spento"
date: 2026-10-23
lang: it
locale: it_IT
permalink: /it/blog/quello-che-resta-spento/
alt: /en/blog/what-stays-off/
description: "Il quarto capitolo dice quali freni esistono, perché la prova li lascia spenti, e che cosa una persona vede prima della prima scrittura."
image: /assets/images/blog/ch4-switches-off.webp
image_sm: /assets/images/blog/ch4-switches-off-640.webp
image_alt: "Quattro interruttori spenti accanto a un foglio ancora da leggere."
series: giro
series_order: 4
author: Nesso
---

Questa è la quarta di quattro letture sullo stesso giro. La prima ha messo Espo da una parte e il canale dall'altra, e ha separato il collegamento dalla integrazione. La seconda ha mostrato la chiave, l'hash e il cursore. La terza ha seguito la cella vuota, il padrone del campo, e la chiusura che lascia il record nello storico. Questo capitolo non accende niente. Racconta i freni, e gli interruttori che esistono e restano spenti.

Spento, qui, è una scelta. Non è un pezzo dimenticato, e non è un difetto nascosto sotto un nome più gentile. La prova lascia spenti quattro interruttori apposta: la scrittura di ritorno, la coda di ritento, il filtro del portale, il sigillo dei segreti. Un giro può partire lo stesso. Quello che non parte è il comportamento che quegli interruttori aggiungerebbero. Chi legge il lunedì mattina deve poter dire, a voce alta, quale leva è giù e quale leva non è mai stata alzata.

Se una frase di questo diario e una frase del manuale divergono, vale il manuale. Il manuale sta nella cartella docs del repository pubblico, e cambia insieme al codice. Questo sito non lo ricompila. Il diario spiega il perché. Il manuale resta il testo che dice che cosa il programma fa oggi.

Il filo è ancora il file delle anagrafiche. Arriva di notte. Ha il codice esterno, il nome, la città, la partita IVA, una nota. Nel racconto della serie, C001 è la riga nuova, Nord Est, Trieste. C014 è la riga identica all'ultima volta. Una riga non ha una colonna obbligatoria, e quello scarto è di file. La nota, su questa integrazione, ha come padrone Espo. Niente di tutto questo, all'apertura del capitolo, è già stato scritto. Il capitolo si ferma un passo prima del POST, e poi dice che cosa, anche dopo, resta spento.

## Prima della prima scrittura

Chi installa ha già fatto i quattro passi, o è fermo sul terzo. Il collegamento c'è: un indirizzo, un tipo, e se serve una password. L'integrazione c'è, o è ancora una bozza: la scheda, la colonna identità, l'abbinamento, la cadenza. Il file è nella cartella, oppure la SELECT è salvata, oppure il webhook non ha ancora chiamato. Espo è dall'altra parte, vuoto se si tratta della prova, oppure già in uso se si tratta di un giro vero. In entrambi i casi la domanda del mattino è la stessa. Che cosa succederebbe se adesso partisse il giro, e che cosa non succederà comunque, perché la leva è giù.

La risposta sta su tre fogli, non su una query.

Il primo foglio è l'anteprima. Conta il giro intero e non scrive. Dice che cosa nascerebbe, che cosa cambierebbe, che cosa resterebbe com'è, che cosa verrebbe scartato. Una partita IVA già presente si vede prima del POST.

Il secondo foglio è un freno che si può tirare. La modalità lettura, su una integrazione, e l'interruttore generale delle scritture, su tutto il motore. Un giro in lettura legge, confronta, e non manda il POST. L'interruttore generale ferma ogni scrittura verso Espo. Non sono i quattro interruttori della prova. Sono i freni da usare quando si vuole guardare un giro che, di default, avrebbe il permesso di scrivere. La modalità lettura nasce spenta. L'interruttore generale, se nessuno lo ha tolto, lascia le scritture permesse. Tirarli è una scelta. Lasciarli è l'altra scelta. Nessuno dei due è un guasto.

Il terzo foglio è l'elenco di ciò che la prova non alza. La scrittura di ritorno resta a zero finché una persona non la accende, e anche allora tocca solo le colonne nominate. La coda di ritento resta spenta finché l'impostazione `retry_queue` non è `1`. Il filtro del portale resta spento finché la regola non si legge come accesa. Il sigillo resta assente finché la variabile `NESSO_SECRET_KEY` non c'è nel processo: la prova non la imposta, e la password del collegamento resta in chiaro nel volume SQLite locale. Dire queste quattro cose a chi riceve la prova fa parte della consegna. Non sono note a piè di pagina.

L'annullamento viene dopo, non prima. Torna indietro su quello che il giro ha scritto. Prima della prima scrittura non ha un giro da disfare. Va saputo adesso, così nessuno lo cerca al posto dell'anteprima. L'anteprima è lo sguardo. L'annullamento è il ritorno, e il ritorno esiste solo dove una scrittura c'è stata.

## Il file, ancora fermo

Conviene tenere le righe sotto gli occhi, perché gli interruttori si giudicano su una riga, non su uno slogan.

C001 non è ancora un Account. L'anteprima la conta fra ciò che nascerebbe. Il nome Nord Est e la città Trieste sono i valori che il file porta. La chiave che nascerebbe è quella del secondo capitolo: l'id dell'integrazione, due punti, C001, sul campo che la scheda già ha. Finché non parte il POST, quella chiave non è su Espo e non è nella memoria del motore come riga sincronizzata. L'anteprima non la crea per «vedere l'effetto». La descrive.

C014 è già stata vista, nel racconto, e l'hash della riga è quello salvato. L'anteprima la conta fra ciò che non cambierebbe. Non prepara un aggiornamento. Non prepara un secondo invio. Un giro che poi partisse davvero farebbe lo stesso, per la ragione del secondo capitolo: hash uguale, stato già allineato, Espo non viene richiamato. Qui il punto è precedente. Anche il conto di «non cambierebbe» è un conto, e non è una scrittura.

La riga senza colonna obbligatoria non fa passare il file a metà. Lo scarto è di file. Il file non si sposta in elaborati. L'anteprima lo dice come scarto, e non sistema il file al posto di chi lo ha posato. Un'identità esterna vuota è uno scarto di file, e più avanti si vedrà che la coda di ritento, anche da accesa, non lo prende. Da spenta, non prende niente.

La nota del commerciale è sul record, se il record esiste già, ed è vuota sul file, oppure il file porterebbe un altro testo. Il padrone è Espo. Il terzo capitolo ha detto che il giro non la svuota. Questo capitolo aggiunge solo il confine del ritorno: spento, la scrittura di ritorno non copia quella nota sul file. Sono due protezioni diverse. Una tiene il campo su Espo. L'altra non riscrive la sorgente. Entrambe, nella prova e in un'installazione che non ha deciso altrimenti, sono il comportamento di default.

Nessuna di queste righe ha bisogno che un interruttore spento venga «riparato» per essere capita. Il file si legge. L'anteprima lo conta. Il POST aspetta una persona, oppure la cadenza, quando la persona ha deciso che il giro può scrivere.

## L'anteprima

L'anteprima conta il giro intero senza scrivere. Il conto è quello che una persona legge prima di dire sì: quante righe nascerebbero, quante cambierebbero, quante resterebbero com'è, quante verrebbero scartate, e se una chiusura di record spariti sarebbe in attesa di conferma. Le righe pericolose, quando ci sono, portano il valore di oggi e il valore in arrivo. Sono il contrasto che il terzo capitolo mette in coda da guardare, mostrato prima che qualcuno lo scriva.

L'anteprima non sposta i CSV. Un file che è ancora nella cartella di ingresso resta nella cartella di ingresso. Non finisce in elaborati solo perché qualcuno ha chiesto il conto. L'anteprima non avanza il cursore. Un'uscita non «consuma» i record solo perché li ha contati. Il cursore è la memoria del secondo capitolo, e si sposta quando un invio è riuscito, non quando un conto è stato letto.

La prova a secco è il fratello corto dello stesso freno. Legge al massimo cinque righe e restituisce il corpo abbinato, oppure lo scarto di quella riga. Non scrive su Espo. Serve a vedere la forma, non il totale. Chi confonde le cinque righe con il giro intero si ferma troppo presto: una partita IVA duplicata può stare alla sesta riga. L'anteprima è il conto del giro. La prova a secco è un campione. Nessuna delle due è il POST.

Una partita IVA già presente si vede prima. Se il campo fiscale della riga è già su un altro record della stessa scheda, il motore lo dice prima di creare. La frase è quella del campo: partita IVA o codice fiscale già presente. Nell'anteprima quella frase entra nel conto degli scarti. Il record già esistente resta com'è. Il record nuovo non nasce. Non c'è un POST di creazione «tanto per provare», e non c'è un POST che poi si cancella. Lo sguardo è una lettura. La scrittura non è partita.

Questo ordine conta il lunedì, quando un file di anagrafiche ripete una partita IVA che un commerciale ha già caricato a mano il venerdì, con un'altra chiave. Senza l'anteprima, il primo segno sarebbe uno scarto nel giornale, dopo il giro. Con l'anteprima, il segno è prima. Chi controlla può fermarsi, può correggere il file, può decidere che quella riga deve restare fuori. Il giro, se poi parte, incontra lo stesso controllo prima del POST. L'anteprima non è una regola più morbida. È la stessa regola, senza la scrittura.

Sul piano di accensione, l'anteprima ha un secondo uso, stretto. Un piano ordina integrazioni già salvate. Il gradino successivo si riattiva solo se il precedente è stato confermato dopo la sua anteprima, e non si accende da solo. Confermare non accende il gradino dopo. Un'integrazione fuori dal piano si mette in pausa e si riattiva come prima. Il piano non è uno dei quattro interruttori. È l'ordine con cui si dice sì. La frase che blocca un sì prematuro è semplice: prima va vista l'anteprima.

Un webhook, finché il sistema esterno non chiama, non ha righe da leggere. L'anteprima lo dice, e non inventa un corpo. La prova a secco, se le si incolla un esempio, interpreta quel corpo e non scrive. Sono ancora sguardi. Il primo POST vero resta un gesto distinto.

## Modalità lettura e interruttore generale

La modalità lettura sta sull'integrazione. Si accende con un gesto esplicito. Un giro partito mentre è accesa legge, confronta, e non manda il POST. Il confronto è quello dell'anteprima: che cosa nascerebbe, che cosa cambierebbe, che cosa è invariato, quale scarto ci sarebbe. La differenza è che il giro c'è, nel giornale, come lettura. Non è un'anteprima chiesta a mano e dimenticata. È un'esecuzione che ha scelto di non scrivere.

La modalità lettura non torna da sola alla scrittura. Uscire è un secondo gesto, quello che la spegne. Un numero di ore può essere scritto accanto all'integrazione, come scadenza annotata. Quella scadenza non è un POST rinviato che parte da solo allo scoccare. Il freno non si sgancia da solo. Chi lo ha tirato lo rilascia, oppure lo lascia tirato. Entrambe le cose si vedono sulla scheda.

L'interruttore generale sta sul motore, non su una integrazione. Fermo, ogni scrittura verso Espo si ferma. Vale per il giro di anagrafiche e per un'uscita, per «Esegui ora» e per il pianificatore. L'anteprima e la prova a secco restano. Si può ancora contare. Non si può ancora scrivere. È il freno da tirare quando il dubbio non è su un file solo, ma su tutto quello che il motore potrebbe mandare stamattina.

I due freni si sommano. Se l'interruttore generale è fermo, una integrazione che non è in modalità lettura non scrive lo stesso. Se l'interruttore generale permette le scritture, e una integrazione è in modalità lettura, quella integrazione non scrive, e un'altra integrazione, non in lettura, può scrivere. Il freno generale è uno. La modalità lettura è per integrazione. Sapere quale dei due è tirato evita una mattina in cui si crede di aver fermato tutto e si è fermata una scheda sola, oppure si crede di aver fermato una scheda e si è fermato il motore.

Un giro trattenuto non è un giro fallito da ritentare con la coda. Non ha mandato il POST. Non ha un fallimento HTTP da rimettere in fila. Ha un conto. Quando si rilascia il freno, il giro successivo è un giro nuovo, con le regole di sempre: hash, padrone del campo, partita IVA già presente, cursore. Non «completa» la lettura di prima come se la lettura avesse lasciato un invio a metà. La lettura non lascia un invio a metà. Non lo inizia.

## L'annullamento

L'annullamento torna indietro su quello che il giro ha scritto. La memoria è lo storico dei campi di quel giro: il valore precedente e il valore scritto. Per ogni record toccato, il motore rilegge il valore attuale. Se il valore attuale è ancora quello che il giro ha scritto, lo rimette al precedente. Se qualcuno lo ha cambiato dopo, quel campo resta com'è. La risposta dice quanti campi sono tornati indietro e quanti sono stati tenuti.

Il limite è il punto. L'annullamento non è un viaggio nel tempo dell'intero Espo. Non cancella il record. Non chiude il record. Non rimette una nota che una persona ha riscritto dopo il giro, perché quella nota non è più «quello che il giro ha scritto»: è quello che la persona ha scritto dopo. Il terzo capitolo ha separato la chiusura dalla cancellazione. L'annullamento è un terzo gesto ancora: il ritorno dei campi dell'ultimo giro, dove il record è ancora nello stato in cui il giro li ha lasciati.

Prima della prima scrittura, chiedere l'annullamento non ha oggetto. Non c'è un giro da annullare. La risposta è questa, non un'anteprima travestita. Chi vuole vedere senza scrivere usa l'anteprima o la modalità lettura. Chi ha scritto e vuole tornare indietro usa l'annullamento, e lo usa mentre le scritture sono permesse. L'annullamento è esso stesso una scrittura verso Espo: rimette i valori precedenti con le API, non con una query sulle tabelle. Se la modalità lettura o l'interruttore generale tengono ferme le scritture, l'annullamento non parte. Il freno che impedisce il POST impedisce anche il POST di ritorno. Per disfare un giro bisogna prima lasciare che le scritture esistano, e poi chiedere il ritorno. È un ordine voluto. Un freno tirato non deve poter scrivere «solo per sistemare».

L'annullamento guarda l'ultimo giro che ha lasciato storico, non un giro a scelta nella settimana. Non è un editor di record. Non è la coda dei contrasti, dove un padrone Espo ha tenuto il valore della persona e il valore del file aspetta un occhio. Quella coda si risolve campo per campo, tenendo Espo o tenendo la sorgente. L'annullamento rimette, in blocco sui campi ancora intatti, lo stato precedente dell'ultimo giro. Sono vicini, e non sono la stessa leva.

## Quattro interruttori, lasciati giù

I freni di sopra si tirano quando si vuole guardare o quando si vuole disfare. I quattro interruttori di questo elenco sono un'altra famiglia. Esistono. Nella prova sono giù. In un'installazione che non ha ancora deciso, sono giù. Alzarne uno cambia il giro. Lasciarlo giù non toglie al giro la capacità di leggere, confrontare e, quando le scritture sono permesse e la modalità lettura è spenta, di mandare il POST delle regole già scelte.

Il primo è il sigillo. Senza `NESSO_SECRET_KEY` la password del collegamento resta in chiaro nel file SQLite del volume locale. La prova non imposta la variabile.

Il secondo è la coda di ritento. L'impostazione `retry_queue` non è `1`. Un giro che scarta una riga non la riscrive una seconda volta attraverso la coda.

Il terzo è il filtro del portale. La regola è nulla o spenta. L'uscita non cambia select e non cambia l'elenco dei record. Non chiama le API di portale o di ruolo di Espo, e non crea utenti di portale.

Il quarto è la scrittura di ritorno. Il default è zero. Accesa, aggiorna solo le colonne nominate. Non riscrive il file intero. Non è il cursore HTTP dell'uscita.

Il resto del capitolo li percorre uno per uno, poi dice che cosa una persona vede sulla pagina, e poi torna sul file di stanotte con le quattro leve ancora giù. Non c'è un quinto interruttore nascosto che li accende «per la demo». La demo del manuale, il Gruppo Meridia, è la prova di un giro. Non è un secondo prodotto e non è un cliente pubblicato su questo sito. Non serve ad alzare queste leve.

## Il sigillo, e la prova che non lo mette

La password di un collegamento sta nel `config_json` di quel collegamento, nel SQLite del volume locale. È la password del database esterno, o l'altro segreto che il tipo di collegamento tiene: non è la password di un utente Espo, e non è un segreto da mandare nel giornale. Senza la variabile `NESSO_SECRET_KEY`, quel valore resta in chiaro sul volume. Chi può leggere il file del volume può leggere la password. Va detto a chi riceve la prova, con la stessa calma con cui si dice dove sta la cartella dei file. Non è una sorpresa da scoprire il martedì.

La prova non imposta la variabile. Docker Compose alza il database, un Espo vuoto e il motore. Non aggiunge, di suo, la chiave dei segreti. Il volume di questa prova resta in chiaro. Non è una dimenticanza del compose da «sistemare» in silenzio dentro un'immagine. È il comportamento pubblicato: finché chi installa non mette la variabile nel processo, i salvataggi nuovi non vengono sigillati.

Con la variabile presente, un salvataggio nuovo si sigilla. Il valore nel file porta il prefisso `enc1:`. La pagina pubblica del collegamento non mostra il testo e non mostra il sigillo. Al posto della password c'è il segno che una password c'è, non la password. Lo scarico della configurazione non riceve i segreti: niente password, niente token, niente valori di intestazione, e niente sigillo da copiare in un altro file credendo che sia la password. Lo scarico è la forma dei collegamenti e delle integrazioni, da rivedere. Non è un backup dei segreti.

Una riga già in chiaro si apre ancora, se la variabile c'è. Il motore sa leggere il testo che non ha il prefisso. Mettere la variabile non è un giro che percorre i collegamenti vecchi e li sigilla da solo. Un salvataggio nuovo, fatto mentre la variabile c'è, nasce sigillato. La riga vecchia, finché resta quella riga, si apre. Sono due fatti, e vanno tenuti distinti. Confonderli farebbe credere che «accendere la chiave» abbia già protetto il volume, mentre il volume ha ancora la riga di prima, in chiaro.

Togliere la variabile dopo che un salvataggio è stato sigillato ha l'effetto inverso, e va detto prima di toglierla. Quel collegamento non si apre finché la password non viene riscritta. Il sigillo senza la chiave non è una password che si indovina. È un valore che il motore rifiuta di aprire. La pagina, anche in quel caso, non mostra il sigillo come se fosse un indizio. Chi ha tolto la variabile deve avere la password da un altro posto, e deve riscriverla. Non c'è un interruttore «mostra i segreti» sulla pagina pubblica.

Lo scarico resta senza segreti sia quando il volume è in chiaro sia quando il volume è sigillato. La pagina di consegna, a sua volta, non contiene le password. Sono tre superfici diverse. Il volume è il posto dove il segreto sta, in chiaro o sigillato. La pagina del collegamento è il posto dove si configura, senza vedere il segreto. Lo scarico e la consegna sono i posti che si possono passare a un'altra persona, e non portano il segreto con sé. Chi riceve lo scarico dovrà rimettere le password. È il passaggio fra prova e esercizio: si tolgono segreti e indirizzi, e non si salva finché non si rivede.

Il sigillo non sceglie il canale. Non accende la scrittura di ritorno. Non mette la coda di ritento a `1`. Non accende il filtro del portale. È una chiave di processo, per i segreti dei collegamenti. Il resto del giro, con o senza di essa, obbedisce alle altre leve. La prova, non mettendola, chiede a chi installa di sapere che il volume è in chiaro, e di decidere se, fuori dalla prova, la variabile deve esserci. Decidere di non metterla su un volume che altri possono leggere non è il consiglio di questo capitolo. Il fatto di questo capitolo è più stretto: la prova non la mette, e un salvataggio nuovo si sigilla solo quando c'è.

## La coda di ritento, spenta

L'impostazione si chiama `retry_queue`. Spenta vuol dire che il valore non è `1`. In quello stato il motore, quando scarta una riga, scrive lo scarto e non scrive una seconda riga di coda. Il giro che ha scartato non scrive una seconda volta attraverso la coda. Non c'è un `next_at`. Non c'è un tentativo differito. Lo scarto sta dove stanno gli scarti. Il giro dopo, se la cadenza lo prevede, leggerà di nuovo la sorgente, con le regole di sempre. Non perché una coda lo abbia rimesso in marcia. Perché il giro è partito di nuovo.

Questo è il default, ed è il default della prova. Un errore di una riga non è, da solo, un invito a riscriverla fra un minuto. Il lunedì mattina, se Espo ha rifiutato una riga, il giornale ha la riga. La coda non ne ha preparata un'altra. Chi si aspettava un secondo POST automatico e non lo vede non sta guardando un buco. Sta guardando l'interruttore giù.

Accesa, la coda fa una cosa sola, e la fa stretta. Rimette in coda solo una riga in ingresso che ha un'identità esterna non vuota. L'identità è la colonna che il secondo capitolo usa per la chiave. Senza quel valore, non c'è una riga da ritentare: c'è uno scarto di file. Lo scarto di file non entra in coda. Una colonna identità vuota non diventa un lavoro differito. Il file va sistemato, non rinviato.

Il ritento non avviene nello stesso giro. Quando la coda è accesa e l'identità c'è, la riga nasce in attesa con `next_at` almeno un minuto avanti. `retry_wait(0)` è un minuto. Il giro che ha appena scartato non la riprende prima di chiudersi. Non c'è un secondo POST «subito, tanto la coda è accesa». Il minuto è il minimo. Il ciclo che scarta non è il ciclo che riscrive.

L'uscita HTTP non usa questa coda. Il cursore dell'uscita ritenta già il record che non è uscito: resta sull'ultimo POST riuscito, e il giro dopo manda quello che non era partito. Rimandare l'uscita anche dalla coda conterebbe due volte lo stesso fallimento, con due orologi. La coda non lo fa. Il dettaglio del cursore sta nel secondo capitolo. Qui basta non cercarlo nella coda di ritento, e non accendere la coda «per far ripartire l'uscita». L'uscita riparte dal cursore, con la coda spenta o accesa allo stesso modo.

Quando un tentativo della coda fallisce, i tentativi aumentano e `next_at` si allontana. L'attesa, in minuti, è il minimo fra due elevato al passo e `24` per `60`. Il passo non supera `10`. All'inizio il passo è zero, e l'attesa è un minuto: due elevato a zero fa uno, e uno è minore del tetto. Al fallimento successivo il passo vale uno e l'attesa è due minuti, poi quattro, poi otto, poi sedici, poi trentadue, poi sessantaquattro, poi centoventotto. Dopo otto tentativi lo stato della riga di coda diventa `scarto`. Non resta in attesa all'infinito. Otto è la fine di quella riga di coda, non un arrotondamento. Il tetto di un giorno, `24` per `60` minuti, sta nella formula insieme al passo che si ferma a dieci. La formula è questa, anche quando gli otto tentativi arrivano prima di quel tetto. Non se ne ricava un nono orario «di cortesia».

Un successo segna la riga di coda come `fatto`. Non la rimette in attesa. Non la cancella per farla sembrare mai nata. `fatto` è il segno che quel ritento ha scritto. Il giornale del giro resta il giornale. La riga di coda non lo sostituisce.

Da spenta, niente di questo calendario esiste. Non c'è un `fatto` da cercare, e non c'è uno `scarto` di coda dopo otto tentativi, perché i tentativi della coda non sono iniziati. Lo scarto del giro c'è, nella tabella degli scarti, come c'era prima che la coda esistesse come interruttore. Il default spento significa una cosa pratica: il ciclo che scarta non scrive una seconda volta attraverso la coda. Chi vuole il calendario deve mettere `retry_queue` a `1`, sapendo che il primo ritento è almeno un minuto dopo, che l'identità vuota non entra, che l'uscita HTTP non entra, e che all'ottavo tentativo la riga di coda è `scarto`.

Due righe del file, per non lasciare la formula in astratto. C001, se il POST fallisce e l'identità c'è, con la coda accesa aspetterebbe almeno un minuto e poi riproverebbe, con l'attesa che cresce, fino a otto tentativi. Con la coda spenta, quel fallimento resta uno scarto del giro. C014, se è invariata, non è uno scarto e non entra in coda né accesa né spenta: non c'è niente da ritentare. La riga senza identità non entra in coda neanche da accesa. Il file di stanotte, sulla prova, incontra la versione spenta.

## L'altro orologio, dopo un errore

C'è un secondo orologio, e non è la coda. Dopo un errore il pianificatore aspetta l'intervallo intero. `last_run` si aggiorna nel ramo di errore, e il prossimo tentativo dell'integrazione si misura da lì. Se la cadenza è un'ora, l'ora ricomincia dall'errore. Non dal momento in cui l'integrazione era stata tentata la volta prima, e non da un minuto. Solo con `retry_failed` a `1` l'orologio resta fermo: `last_run` precedente non si sposta, lo stato diventa errore, e il giro può ripresentarsi prima, perché l'intervallo si conta ancora dal vecchio orario.

Il default è l'attesa intera. `retry_failed` non è `1` se nessuno lo ha messo. La prova non lo alza per compensare la coda spenta. Sono impostazioni diverse. La coda, quando c'è, riguarda una riga in ingresso con identità. `retry_failed` riguarda l'orologio dell'integrazione intera, dopo un errore del giro. Accendere l'una non accende l'altra. Spegnere l'una non spegne l'altra. Il lunedì, se il giro è caduto, la domanda «quando riparte da solo» si risponde con la cadenza e con questo orologio, non con `retry_wait`.

Tenere l'intervallo intero è la scelta contraria al martellare. Espo che non risponde, una SELECT che fallisce, un'eccezione nel giro: il giornale ha l'errore, l'orologio si sposta, e si aspetta. Chi è sveglio alle sette legge il giornale e decide se lanciare «Esegui ora». «Esegui ora» è un gesto di persona. Non è `retry_failed`. La pausa, a sua volta, è un'altra leva ancora: il pianificatore e il webhook saltano un'integrazione in pausa, «Esegui ora» no. Nessuna di queste leve è la coda di ritento.

La stessa integrazione non parte due volte. Se un giro è già in corso, il secondo riceve che un'esecuzione è già in corso. Il pianificatore, in quel caso, la salta e non scrive un errore ogni trenta secondi. Due integrazioni diverse possono girare insieme. Il dettaglio di questo vincolo sta nel secondo capitolo. Qui entra per una ragione sola: un errore non deve diventare due giri sovrapposti della stessa regola, e l'orologio dell'errore non è un permesso di sovrapporli. Il freno della doppia partenza resta, con la coda spenta e con la coda accesa, con `retry_failed` fermo e con `retry_failed` a `1`.

## Il filtro del portale, spento

Il filtro sta in `portal_json`, sull'integrazione di uscita. Nullo, oppure letto e non acceso, non cambia l'uscita. Il select è quello di prima: i campi dell'abbinamento, insieme a `id` e `modifiedAt`. `teamsNames` non viene aggiunto per questo filtro. L'elenco dei record è l'elenco di prima. Un record del team Vendite e un record del team Acquisti escono entrambi, se il cursore dice che devono uscire. Il filtro non li ha distinti, perché il filtro non è in funzione.

Non chiama le API di portale di Espo. Non chiama le API dei ruoli. Non crea utenti di portale. Un'uscita di Lead o di Account non diventa, per il solo fatto di esistere, un invito al portale. I ruoli del portale, su Espo, restano quelli che un amministratore ha messo. Nesso non li modifica. Questo vale spento, e vale anche acceso: acceso, il filtro sceglie quali record escono, e non riscrive i ruoli.

Quando la regola si legge come accesa, l'uscita aggiunge `teamsNames` al select. Poi salta i record per cui `portal_visible` è falso. La funzione è stretta. Se la regola non c'è o non è accesa, il record non viene saltato da questo filtro. Se la regola è accesa e l'entità del record non è quella della regola, il record non è visibile per l'uscita. Se la regola nomina un team e quel team non è fra i team del record, il record non è visibile per l'uscita. Un record di un altro team non esce. Il cursore resta sull'ultimo record uscito. Un cambio di team, su Espo, aggiorna `modifiedAt`, e il record può essere riletto al giro dopo. Il filtro non tiene una seconda memoria dei team. Legge quello che l'uscita ha chiesto.

C'è un'eccezione che il filtro non si prende. Una chiave esterna mancante ferma ancora il pull. Il filtro non trasforma quella fermata in un salto silenzioso, e non fa proseguire i record dopo come se la chiave ci fosse. Il secondo capitolo possiede il dettaglio del cursore che si ferma. Questo capitolo dice solo che accendere il portale non toglie quella fermata. La regola del portale e la chiave mancante non si scambiano il mestiere.

Da spento, select ed elenco non cambiano. Non c'è un team «di default» applicato in segreto. Non c'è un portale vuoto creato per la prova. Chi si aspettava che l'uscita parlasse il linguaggio dei ruoli portale, e vede uscire i record senza quel filtro, sta vedendo la leva giù. Alzarla è nominare la regola e averla accesa. Non è un flag ereditato dal nome dell'integrazione, anche se il nome dice «portale». Il nome non è la regola. La regola è `portal_json` letto come acceso.

## La scrittura di ritorno, spenta

`write_back` nasce a zero. Finché una persona non lo mette a uno, il giro non aggiorna la sorgente. Il file di notte resta il file che è arrivato. Una SELECT resta una lettura. Il database esterno non riceve un UPDATE per il solo fatto che Espo ha un valore più nuovo, o un valore che il file non aveva. Spenta, la scrittura di ritorno non tocca la sorgente.

Accesa, tocca solo le colonne nominate. L'elenco è `write_fields`. Una colonna non nominata non entra nell'aggiornamento. Non è una riscrittura del file intero. È un aggiornamento delle colonne che qualcuno ha scritto nell'elenco.

Non è il cursore HTTP dell'uscita. Il cursore ricorda l'ultimo record mandato fuori da Espo verso un collegamento di uscita, e avanza dopo i POST riusciti. La scrittura di ritorno, quando un giorno è accesa, è l'altro verso: dalla memoria di ciò che Espo ha, verso colonne nominate della sorgente. Un'integrazione di ingresso non diventa un'uscita perché si è acceso il ritorno. Il collegamento resta quello che è. Il ritorno è una decisione in più, sulla stessa regola, e di default non c'è.

Sul file delle anagrafiche la differenza si tocca con la nota. Il padrone Espo tiene la nota sul record. Il ritorno spento non scrive quella nota nella cella del file. Se un giorno il ritorno si accende e la colonna nominata è la città, e solo la città, la nota non parte lo stesso. Nominare è l'unica lista. «Tutto quello che Espo sa» non è una voce di quella lista.

Il ritorno non sceglie il canale, non crea utenti, non accende la coda, non accende il portale, non mette la variabile dei segreti. È una leva sull'integrazione. La prova la lascia a zero. Un'installazione che copia la prova senza leggere la leva la lascia a zero, e fa bene finché qualcuno non ha deciso quali colonne tornano. Decidere le colonne è il lavoro. L'interruttore senza colonne non è un ritorno.

## Ciò che non si sposta, anche con le leve giù

Alcuni confini non sono interruttori di questo capitolo. Restano confini, e vale la pena nominarli qui perché un interruttore spento viene spesso scambiato per uno di essi, o uno di essi viene cercato fra gli interruttori.

La posta del CRM resta in Espo. Nesso non diventa il programma che legge la casella e non diventa il programma che spedisce la posta del CRM. Una leva di ritento, di portale o di ritorno non «include la posta» quando la si alza. La posta di Espo resta configurata dove è. Il motore, se un giorno avrà una posta sua, sarà un'altra cosa, agganciata al proprio invio, e oggi non è il giro delle anagrafiche.

L'Advanced Pack non viene riscritto. Non sta nel repository. Se qualcuno lo ha in locale, resta locale. Il motore non lo pubblica e non lo copia insieme ai dati. Spegnere il portale non è un modo di tenere fuori l'Advanced Pack: l'Advanced Pack è già fuori. Accendere il portale non lo fa entrare.

Niente SQL sulle tabelle di Espo. I freni di questo capitolo fermano dei POST, o evitano degli UPDATE sulla sorgente esterna. Non aprono una via laterale sul database di Espo «per leggere più in fretta» o «per sistemare a mano». La lettura di una scheda è una chiamata. La scrittura di una scheda è una chiamata. Quando la chiamata di scrittura non parte, non parte. Non viene sostituita da una query.

I dump di produzione non entrano nella prova. L'Espo che Compose alza è vuoto. Non si monta un backup, non si copiano gli allegati, non si usa la storia vera di un'azienda come dati di sviluppo. Gli interruttori spenti non sono un sostituto di questa regola. Anche con le quattro leve alzate, un dump di produzione non è un passo della prova. La prova è vuota prima di ogni leva.

Gli utenti di Espo non si creano da un'anagrafica. Un file di persone non è un file di login. Il filtro del portale, anche acceso, non crea utenti di portale. Il sigillo non crea utenti. La ricetta dei contatti prepara un abbinamento verso Contact, da rivedere, e non crea gli utenti che quei contatti potrebbero un giorno diventare. Creare un utente è un gesto di amministrazione, con una password e un ruolo. Nessuna leva di questo capitolo lo fa al posto di quel gesto.

## La proposta di abbinamento, e le colonne ancora vuote

Prima del POST c'è l'abbinamento, e anche l'abbinamento ha i suoi freni. Non sono i quattro interruttori. Sono il motivo per cui un abbinamento non nasce da solo mentre si guarda una colonna.

Proponi l'abbinamento legge i nomi delle colonne, nella lingua della pagina. I sinonimi sono un elenco, per lingua. Una colonna che si chiama come una partita IVA può proporre il campo fiscale, se la scheda lo ha. Una colonna non riconosciuta resta vuota, da compilare a mano. La proposta non esce in rete. Non salva l'integrazione. La persona rivede, cambia quello che non torna, e poi salva. Il salvataggio è il sì. La proposta è il foglio prima del sì.

Completa le colonne vuote chiama un modello solo se un indirizzo è impostato. Senza indirizzo non parte nessuna chiamata, e la proposta per sinonimi resta. Con l'indirizzo, la chiamata riempie solo le colonne ancora vuote, fra i campi che la scheda conosce già. Non tocca una colonna già abbinata. Non salva l'integrazione. Non manda la password del collegamento. Manda i nomi delle colonne, al massimo tre celle corte, e il nome del campo. L'indirizzo del modello non entra nello scarico della configurazione. Chi passa lo scarico a un'altra persona non le passa, insieme, l'indirizzo del modello.

Il modello non sceglie il canale. Non crea le schede. Non accende la scrittura di ritorno. Non mette `retry_queue` a `1`. Non accende il filtro del portale. Non imposta `NESSO_SECRET_KEY`. Una colonna proposta bene non è una leva alzata. È una riga di abbinamento, ancora da salvare, ancora da far passare dall'anteprima.

La lingua della proposta è la lingua della pagina. La pagina può essere in italiano o in inglese. I sinonimi di una lingua non cancellano l'altra: un nome di colonna italiano e un nome di colonna inglese possono proporre lo stesso campo, ciascuno dal proprio elenco. Il giornale, invece, resta nella lingua del giro. Se il giro è partito in italiano, le frasi del giornale restano in italiano anche se il pomeriggio si apre la pagina in inglese. Non si traducono a posteriori. Il giornale è il verbale. La proposta è un aiuto prima del salvataggio. Non si scambiano.

## Le ricette, da rivedere

Anagrafiche, contatti, sedi e listino sono quattro punti di partenza. Ognuno prepara un abbinamento. Nessuno è un connettore certificato. Il nome del sistema dall'altra parte non è scritto nel programma, e non è scritto nella ricetta. La ricetta dice: questa scheda, queste colonne, questa identità. La persona legge e può cambiare le righe prima di salvare. La ricetta non salva da sola l'integrazione.

Le anagrafiche preparano Account, con l'identità sulla colonna del codice e con i campi che un'esportazione di clienti ha già, compresa la partita IVA se il campo c'è. I contatti preparano Contact: codice, nome, cognome, email, telefono, e l'azienda cercata per nome su Account. Le sedi preparano l'indirizzo di spedizione su Account, una sede per azienda, solo se il campo c'è già. Nessuna di queste ricette crea la scheda. Se il campo non c'è, la riga dell'abbinamento non inventa il campo per far tornare la ricetta.

Il listino punta alla scheda Product. Le righe sono descrizione, codice, prezzo e valuta, solo se il campo è già sulla scheda. Non crea Product. Nella prova, se Product non c'è, i campi del listino restano vuoti. È un vuoto visibile. Non è un catalogo fantasma creato per riempire l'anteprima. Chi vuole il listino ha prima la scheda su Espo, poi la ricetta, poi la revisione, poi l'anteprima. Saltare al POST non è un passo della ricetta.

Una ricetta non alza i quattro interruttori. Non mette la scrittura di ritorno sulle colonne che ha nominato. Nominare un campo nell'abbinamento verso Espo non è nominarlo in `write_fields`. Non accende la coda. Non accende il portale. Non sigilla il volume. Dopo la ricetta, la prova è ancora la prova di prima: quattro leve giù, e un abbinamento da leggere.

## La prova, il clone, la consegna

La prova si prende clonando il repository pubblico, `https://github.com/nessocrm/nessocrm`. Non c'è un installer da scaricare a parte. Non c'è un modulo che chiede un indirizzo email. Non c'è una lista di attesa. Il contatto è il repository. Docker Compose alza il database, un Espo vuoto e il motore. La prima volta il lavoro è quello: costruire, attendere che Espo sia su, aprire la pagina. I dump di produzione non sono un passo di quel lavoro.

La pagina di consegna elenca gli indirizzi, le integrazioni, la cadenza, il padrone di ciascun campo, e come si fermano le scritture. Non contiene le password. Non contiene i token. Non contiene gli indirizzi di webhook o di casella come segreti da incollare in un messaggio. Chi consegna passa quella pagina, e passa a voce, o per un canale che non è lo scarico, le password che lo scarico ha tolto. La pagina di consegna non è lo scarico, e lo scarico non è il volume. Tre oggetti, già detti sul sigillo, e qui ripetuti perché la consegna è il momento in cui si scopre se qualcuno si aspettava di trovare la password scritta in fondo.

Il giornale resta nella lingua del giro. La pagina può essere in italiano o in inglese, e la scelta è della pagina. Un giro lanciato da una pagina in italiano lascia frasi in italiano. Aprirla dopo in inglese non le riscrive. Il pianificatore parla la lingua in cui è stato impostato. Chi legge un errore alle sette deve leggere la frase che il motore ha scritto. Questo diario, a differenza del giornale, esiste due volte, in italiano e in inglese, perché è una spiegazione. I due testi dicono gli stessi fatti. Non promettono che il giornale farà lo stesso.

Sulla prova, prima del primo POST, una persona può fare questo, e solo questo è già il giro di questo capitolo. Salva un collegamento, sapendo che la password resta in chiaro sul volume. Chiede una ricetta, o propone l'abbinamento per sinonimi, e non considera salvato ciò che non ha confermato. Guarda l'anteprima. Se vuole un'esecuzione che non scriva, accende la modalità lettura, oppure ferma l'interruttore generale. Legge il conto. Lascia giù la scrittura di ritorno, la coda, il portale e il sigillo, finché non ha una ragione per alzarne uno, e la ragione non è «vediamo che cosa succede».

## Il Gruppo Meridia, e i due giri

Nel manuale, il Gruppo Meridia è la prova di un giro. Serve a vedere la forma di un caricamento, con schede e team, dentro un Espo di prova. Non è un secondo prodotto, accanto a Nesso, da installare con un altro nome. Non è un cliente pubblicato su questo sito. Nominarlo nel diario serve a toglierlo dall'elenco delle cose che questo capitolo avrebbe acceso. Non ha acceso le quattro leve. Non le accende per chi clona il repository oggi. Chi cerca sul sito un caso commerciale con quel nome non lo trova, perché non è questo l'uso del nome. L'uso è nel manuale, come prova.

La stessa integrazione non parte due volte. Due integrazioni diverse possono girare insieme. Il secondo capitolo tiene il dettaglio: il secondo avvio della stessa riceve che un'esecuzione è già in corso, e il pianificatore non riempie il giornale di quell'errore ogni trenta secondi. In questo capitolo la frase serve a leggere i freni senza mescolarli. La modalità lettura è per integrazione: una può leggere mentre l'altra, se le scritture sono permesse, scrive. L'interruttore generale no: fermo, non scrive nessuna delle due. La coda di ritento è un'impostazione del motore, una per tutti i giri. Il sigillo è una variabile del processo, una per i salvataggi dei collegamenti. La scrittura di ritorno e il filtro del portale stanno sull'integrazione, e possono essere diversi fra anagrafiche e un'uscita. Due giri insieme non fondono queste leve in una leva sola.

## Il lunedì, con le leve ancora giù

Alle sette il file c'è. Chi tiene il numero in home non ha ancora un successo di oggi da mostrare, se il giro non è partito. L'anteprima non glielo fabbrica. Un conto senza POST non sposta l'ultimo successo e non spegne un bordo di file atteso. Il numero resta un controllo. Non diventa verde perché qualcuno ha guardato.

Chi ha la nota apre il record, se il record c'era già, e la nota c'è ancora. Il giro non è partito, oppure è partito in lettura e non ha mandato il POST. In entrambi i casi la scrittura di ritorno, spenta, non ha copiato la nota sul file. Il padrone Espo e il ritorno spento hanno lavorato nello stesso senso, per ragioni diverse. Il badge, se il giro non ha scritto, non ha una origine nuova da mostrare. Il terzo capitolo dice che cosa il badge significa quando il giro scrive. Qui il badge non viene chiamato a coprire un'anteprima.

Chi controlla apre l'anteprima e legge i conti. C001 fra le nascite. C014 fra le invariate. Lo scarto di file, se manca la colonna, in evidenza, senza che il file sia stato spostato. La partita IVA già presente, se c'è, nel conto degli scarti, prima di ogni POST. Se i conti tornano e le scritture sono permesse e la modalità lettura è spenta, «Esegui ora» è il primo POST. Se i conti non tornano, il POST non è il passo successivo. Il passo successivo è il file, o l'abbinamento, o la decisione di lasciare il freno tirato.

Chi installa, la stessa mattina, sa dire quattro no. No, la password non è sigillata, perché la prova non ha `NESSO_SECRET_KEY`, ed è in chiaro sul volume, e non è sulla pagina di consegna. No, la riga scartata non verrà riscritta fra un minuto dalla coda, perché `retry_queue` non è `1`. No, l'uscita non sta filtrando i team, perché la regola del portale non è accesa, e i ruoli del portale su Espo non sono stati toccati. No, il file non è stato aggiornato di ritorno, perché `write_back` è zero, e non lo sarebbe comunque sull'intero file anche se qualcuno nominasse delle colonne. Quattro no sono la consegna. Non sono quattro scuse.

Se il giro poi parte e cade, l'orologio aspetta l'intervallo intero, salvo che qualcuno abbia messo `retry_failed` a `1`, cosa che la prova non fa per conto suo. L'attesa intera e la coda spenta si sommano. Non si annullano. Il giornale ha l'errore, nella lingua del giro. La persona legge quella frase. Non una traduzione fatta dopo, e non un secondo POST partito dalla coda che non c'è.

Se il giro poi parte e scrive, e la scrittura è sbagliata, l'annullamento torna indietro su quello che quel giro ha scritto, sui campi che nessuno ha cambiato dopo. Non accende il ritorno verso il file. Non sigilla il volume. Non mette in coda le righe. Non filtra il portale. Disfare un POST non alza le leve che il POST non ha usato.

## Lo stesso giro, nell'ordine della pagina

Conviene rileggere i fatti nell'ordine in cui una persona li incontra, perché l'ordine è parte del freno. Si incontra prima ciò che non scrive, e dopo ciò che potrebbe scrivere, e per tutto il tempo le quattro leve restano dove sono.

Si crea il collegamento. Se è un database, una SELECT, un indirizzo, un utente, una password. Il salvataggio che elenca le colonne ha già eseguito la lettura. La password, sulla prova, finisce in chiaro nel volume. La pagina del collegamento, subito dopo, non la mostra. Lo scarico, se lo si prende adesso, non la contiene. Niente di questo ha scritto su Espo.

Si sceglie la scheda. Account, per il file delle anagrafiche. Si chiede la ricetta, oppure si propone l'abbinamento. Le colonne riconosciute ricevono un campo. Le altre restano vuote. Se si chiede di completare le vuote e l'indirizzo del modello non c'è, non parte nessuna chiamata. Se l'indirizzo c'è, si riempiono solo i vuoti, senza salvare e senza mandare la password. La persona conferma. Solo allora l'abbinamento è salvato. La scrittura di ritorno è ancora zero. La coda è ancora spenta. Il portale è ancora spento. Il sigillo c'è solo se la variabile c'era al salvataggio del collegamento, e sulla prova non c'era.

Si guarda l'anteprima. Il conto di C001, di C014, dello scarto, della partita IVA se è già presente. I CSV non si spostano. Il cursore non avanza. Se il piano di accensione ha questa integrazione come gradino, il gradino può essere confermato solo dopo questo sguardo, e il gradino dopo non si accende da solo.

Si decide del freno. Modalità lettura, se si vuole un giro che confronti e non mandi il POST. Interruttore generale, se si vogliono ferme tutte le scritture verso Espo. Oppure nessuno dei due, se il conto torna e il POST è voluto. Il POST, quando parte, è il POST delle regole già scritte nei capitoli di prima: chiave, hash, padrone, cella vuota, chiusura solo con le conferme che il terzo capitolo ha detto. Non è un POST allargato dalle leve di questo capitolo, perché quelle leve sono giù.

Se una riga in ingresso con identità viene scartata, lo scarto resta uno scarto. La coda non la riprende un minuto dopo. Se l'identità è vuota, lo scarto è di file e non entrerebbe in coda nemmeno con la coda accesa. Se l'errore è del giro intero, si aspetta l'intervallo, perché `retry_failed` non è `1`. Se l'uscita è un'altra integrazione, il suo elenco di record è l'elenco intero che il cursore consente, senza `teamsNames` aggiunto per un filtro che non c'è, e una chiave mancante ferma ancora il pull. Se qualcuno cerca nel file di notte la nota del commerciale, non la trova scritta di ritorno.

Se, dopo un POST, si vuole tornare indietro, l'annullamento usa lo storico di quel giro. Poi le leve sono ancora giù. Il capitolo finisce nello stesso stato in cui è cominciato, con una differenza sola, voluta: la persona ha visto il conto prima di scrivere, e sa dire che cosa non è partito.

## Che cosa questo capitolo non ha acceso

Non ha messo `NESSO_SECRET_KEY` nella prova, e non ha riscritto le righe già in chiaro. Non ha messo `retry_queue` a `1`, e non ha fatto scrivere due volte il ciclo che scarta. Non ha acceso `portal_json`, e non ha chiamato il portale di Espo. Non ha messo `write_back` a uno, e non ha riscritto il file. Non ha messo `retry_failed` a `1`, e non ha accorciato l'attesa dopo un errore. Non ha fatto partire un POST dall'anteprima. Non ha fatto salvare la proposta di abbinamento. Non ha fatto scegliere al modello il canale. Non ha certificato le ricette. Non ha creato Product perché il listino aveva dei campi vuoti. Non ha importato un dump. Non ha creato utenti da un'anagrafica. Non ha spostato la posta fuori da Espo. Non ha pubblicato l'Advanced Pack. Non ha fatto del Gruppo Meridia un cliente di questo sito.

Il file di stanotte, alla fine di questo capitolo, può essere ancora un file. Può anche essere già stato scritto, se la persona ha visto l'anteprima e ha detto sì: in quel caso C001 è un Account, C014 non è stata riscritta, la nota di Espo è ancora di Espo, e le quattro leve sono giù lo stesso. Il sì del POST non è il sì di quelle leve. Sono sì diversi. Il prodotto li tiene separati perché il lunedì mattina si possa dire quale dei due è stato detto, e quale no.

Un interruttore spento si legge. Si legge sulla scheda, nell'impostazione, nell'assenza della variabile, nel conto dell'anteprima che non ha spostato nulla. Non si deduce da un successo. Un giro andato a buon fine con le leve giù è il giro delle regole di prima, più i freni che non sono stati tirati e più gli interruttori che non sono stati alzati. È il giro che la prova consegna. Chi lo riceve riceve anche il dovere di sapere che la password è in chiaro, che uno scarto non si riscrive da solo, che l'uscita non filtra il portale, e che la sorgente non viene aggiornata di ritorno. Sapere questo è il capitolo. Alzare una leva, quando servirà, sarà un'altra mattina, e sarà ancora una scelta.
