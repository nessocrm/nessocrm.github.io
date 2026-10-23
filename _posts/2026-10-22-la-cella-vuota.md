---
layout: post
title: "La cella vuota"
date: 2026-10-22
lang: it
locale: it_IT
permalink: /it/blog/la-cella-vuota/
alt: /en/blog/the-empty-cell/
description: "Di notte una cella vuota svuota il campo di cui la sorgente è padrona, e la nota scritta su Espo resta."
image: /assets/images/blog/ch3-empty-cell.webp
image_sm: /assets/images/blog/ch3-empty-cell-640.webp
image_alt: "Una cella di città vuota e una nota che resta sul record."
series: giro
series_order: 3
author: Nesso
---

Questa è la terza di quattro letture sullo stesso giro. Non racconta un cliente. Racconta che cosa fa una cella quando il file di notte arriva, e chi ha il diritto di svuotarla. La prima lettura ha messo Espo da una parte e il canale dall'altra: il collegamento è il canale, l'integrazione è la regola, e il passaggio usa le API HTTP. La seconda tiene la chiave, l'hash e il cursore, cioè il modo in cui una riga viene riconosciuta e il modo in cui una riga identica non viene riscritta. La quarta tiene ciò che resta spento: la scrittura di ritorno, la coda di ritento, il filtro del portale, il sigillo. Qui non si accende niente di tutto questo. Qui si guarda una cella, e si dice perché il vuoto è fastidioso e perché è corretto.

Se una frase di questo diario e una frase del manuale divergono, vale il manuale. Il manuale sta nella cartella docs del repository pubblico, e cambia insieme al codice. Questo sito non lo ricompila. Il diario spiega il perché di una notte. Il manuale resta il testo che dice che cosa il programma fa oggi.

Il giornale di un giro resta nella lingua del giro. Se il giro è partito da una pagina in italiano, le frasi del giornale restano in italiano anche se il giorno dopo si apre la pagina in inglese. Il badge già messo sul record non si traduce a posteriori. Questo diario esiste due volte, in italiano e in inglese, perché è una spiegazione e non un verbale. I due testi dicono gli stessi fatti. Non dicono che il giornale farà lo stesso.

## Il file, prima della regola

Il file è quello delle anagrafiche, lo stesso dei capitoli accanto e lo stesso che la home mostra in piccolo. Arriva di notte in una cartella. Le colonne che questo capitolo segue sono cinque. Ciascuna ha già un padrone, scelto nell'abbinamento, prima che il file si posi.

Il codice esterno è l'identità della riga. Serve a sapere di quale record si parla. Come quell'identità diventa la chiave sulla scheda — l'id dell'integrazione, due punti, e il codice — è il lavoro del capitolo sulla chiave. Qui il codice si legge e si tiene da parte. C001 è la riga nuova. C014 è la riga invariata. Una terza situazione, senza un codice inventato per l'occasione, è la riga già nota la cui città arriva vuota.

Il nome è un campo della sorgente. La città è un campo della sorgente. La partita IVA è un campo della sorgente. La nota, in questa integrazione, ha come padrone Espo. Di default il padrone è la sorgente. Spostare la nota su Espo è una decisione esplicita: una persona del commerciale scrive su quel campo, e il file di notte non deve portarglielo via. La decisione sta sulla riga dell'abbinamento, accanto al campo, e si rivede sulla pagina di consegna, dove c'è il padrone di ogni campo e non ci sono password.

C'è poi tutto ciò che l'abbinamento non nomina. Un campo della scheda che non compare nella mappa non entra nel giro. Una colonna del file che nessuno ha collegato a un campo non scrive da nessuna parte. Lo svuotamento, quando arriva, non è un passaggio del record intero. È un passaggio dei campi di cui la sorgente è padrona, e solo di quelli.

La visibilità non è una di queste cinque colonne di anagrafica. È una regola a parte: questa riga è del team Vendite, assegnata a questa persona. Il team e la persona arrivano da una colonna oppure il team è fisso. Ci torno quando i valori della riga sono stati letti fino in fondo. Mescolarli adesso farebbe sembrare che svuotare la città riassegni il cliente. Non è quello che succede.

## Di default vince la sorgente

La regola è corta. Di default vince la sorgente, compresa una cella vuota. Se il file di stanotte porta una città vuota, la città su Espo diventa vuota. La cella non viene letta come «dato assente, lascia com'è». Viene letta come un valore, e il valore è vuoto. Nel file una cella vuota resta una stringa vuota. La colonna c'è. Il contenuto no. Quella stringa, sul campo di cui la sorgente è padrona, è ciò che si scrive.

Il motivo è lo stesso per cui un nome nuovo sostituisce il nome vecchio. La sorgente è il posto da cui quel campo prende la verità di questo giro. Una cella che dice Trieste e una cella che non dice nulla hanno la stessa forma: sono il contenuto arrivato stanotte. Trattare il vuoto come un'eccezione silenziosa vorrebbe dire che il file comanda solo quando riempie, e che quando smette di riempire il record conserva un ricordo che la sorgente ha già ritirato. Il lunedì quel ricordo sembrerebbe prudenza. Sarebbe una seconda verità, tenuta sul record contro il file. Il primo capitolo ha già detto che non c'è una terza verità nel mezzo. Questo capitolo è il punto in cui quella frase si tocca con un dito: la terza verità sarebbe proprio la città vecchia lasciata in pace perché la cella nuova è bianca.

Per questo lo svuotamento dà fastidio, e per questo è corretto. Il fastidio e la correzione stanno nello stesso gesto. Una persona apre l'azienda e la città non c'è più. Ieri c'era. Nessuno ha premuto un tasto cancella sul campo, a mano, nell'interfaccia. Il file, in una cella, era bianco. Il fastidio è la reazione giusta davanti a un dato visibile che non si vede più. La correzione del fastidio non è impedire lo svuotamento su tutti i campi. È avere scelto, prima della notte, quali campi accettano questa regola. La città l'ha accettata, perché il padrone è la sorgente. La nota non l'ha accettata, perché il padrone è Espo.

Lo svuotamento non attraversa la scheda a caso. Vale solo dove il padrone è la sorgente. Un campo il cui padrone è Espo non si svuota perché la cella è bianca. Un campo non abbinato non si svuota, perché il file non ha nulla da dire su di lui: né un pieno né un vuoto. La frase «il file ha aggiornato l'anagrafica» è vera per i campi mappati della sorgente. Diventa falsa se la si legge come «il file ha riscritto la scheda». La scheda ha campi che la notte non conosce. Quei campi, al mattino, sono quelli della sera prima.

C'è un caso vicino, e non va confuso con la città bianca. Se l'abbinamento segna un campo come obbligatorio e la cella arriva vuota, la riga si scarta e il campo viene nominato, prima della chiamata a Espo. Non si svuota il record a metà, e non si scrive il vuoto su un campo che la regola ha dichiarato necessario. Il primo capitolo separa già due errori diversi: manca una colonna obbligatoria, e allora il file non si sposta; manca una cella e la colonna c'è, e allora si scarta quella riga. La cella vuota di questo capitolo è la terza situazione. La colonna c'è, la cella è bianca, il campo non è tenuto come obbligatorio, il padrone è la sorgente, e il campo su Espo diventa vuoto. La città dell'esempio è questa terza situazione. Se qualcuno, nell'abbinamento, avesse segnato la città come obbligatoria, la riga non arriverebbe allo svuotamento: verrebbe scartata col nome del campo. L'esempio non fa quella scelta. L'esempio lascia che il vuoto vinca, perché è così che si vede la regola di default.

## Una riga già nota, cella per cella

Conviene seguire una riga che esiste già su Espo e che stanotte è ancora nel file, con la città bianca. Non le do un codice che il racconto non ha. È la riga su cui la città arriva vuota. Le altre celle della stessa riga non condividono un destino unico. Si leggono una per una.

Il codice c'è. Senza codice non sapremmo quale record aggiornare, e l'errore di un'identità mancante sta nel capitolo della chiave, non qui. Con il codice, il giro sa quale Account è questo. Il codice non è un campo che «si svuota» nel senso della città: è il modo di trovare il record. Una cella codice vuota non è l'esempio di stanotte.

Il nome, se la cella del nome porta un valore, viene scritto, perché il nome è della sorgente. Se la cella del nome fosse bianca, e il nome non fosse obbligatorio, il nome su Espo diventerebbe vuoto, per la stessa regola della città. Nel file che questo capitolo racconta, la cella che arriva vuota è la città. Il nome resta un campo che la sorgente può aggiornare quando porta un testo. Non si inventa, qui, un nome nuovo per quella riga, e non si inventa un nome svuotato. Si dice solo che la regola che svuota la città è la regola del nome, il giorno in cui la cella del nome è bianca.

La città è bianca, e la colonna c'è. Il padrone è la sorgente, quindi la città sul record diventa vuota. È il gesto al centro del capitolo. La scrittura verso Espo è una chiamata HTTP, sullo stesso record, del campo città. Non è una query sulla tabella. Non è un comando che azzera la riga. Gli altri campi di questa chiamata sono quelli che l'abbinamento manda insieme, non l'intera scheda. La città parte vuota. La nota, se è di Espo, non parte in quella chiamata come un vuoto che cancella.

La partita IVA, se la cella porta un numero, resta un campo della sorgente e segue la cella. Se quel numero è già presente su un altro record, si vede prima della scrittura. L'anteprima lo mostra, e il giro lo vede prima del POST. Non si scopre il duplicato solo dopo aver creato un secondo Account con lo stesso numero. Una partita IVA vuota, se la cella è presente e vuota, il campo è della sorgente e non è obbligatorio, svuoterebbe il campo. È la stessa regola della città. Il trattamento in più, quello che la partita IVA ha e la città non ha in questo racconto, è solo questo: un numero già presente si vede per primo.

La nota non segue la città. Il padrone è Espo, e il record esiste già. Se una persona ha scritto una nota, la nota resta. Se la cella della nota arriva vuota, il campo non si svuota, e il vuoto non finisce nemmeno in coda: non c'è un testo diverso da guardare, c'è un'assenza, e l'assenza non ha il diritto di sostituire la frase. Se la cella porta un testo diverso da quello già sul record, quel testo va nella coda da guardare. Il campo su Espo non cambia. La coda tiene il valore arrivato accanto a quello che c'è già, perché qualcuno possa guardarlo. Guardare non è scrivere.

Un campo non abbinato sta fermo per tutta la riga. Può essere un telefono che una persona ha compilato sulla scheda, se il telefono non è nella mappa. Può essere una colonna del file, presente stanotte, che nessuno ha collegato. Nel primo caso il giro non ha un nome di campo su cui scrivere. Nel secondo caso ha una colonna e non ha un destinatario. In entrambi i casi il mattino trova quel dato com'era, oppure non lo trova su Espo perché non è mai stato un campo del giro. L'abbinamento è l'elenco dei campi su cui la notte ha diritto di parola. Fuori da quell'elenco la notte tace, anche quando la città, che è nell'elenco, diventa vuota.

Sulla stessa riga i due gesti possono convivere. La città si svuota, perché è della sorgente e la cella è vuota. La nota resta, perché è di Espo. Se inoltre il file porta una nota diversa, la città si svuota e, insieme, il testo diverso entra in coda. Non sono due modalità del giro tra cui scegliere. Sono due padroni sulla stessa riga, applicati nella stessa notte. Chi al mattino dice «o si aggiorna tutto o non si tocca niente» sta descrivendo uno script, non questo abbinamento.

## Perché il fastidio è il segno che la regola funziona

Vale la pena restare sulla città, perché è il punto in cui una persona ragionevole chiede di spegnere la regola per tutti i campi.

La scena è questa. Sul record la città c'era. Non le do un nome di città precedente: il racconto non lo fissa, e non serve. Importa che ci fosse un valore, e che stanotte la colonna ci sia e la cella no. Al mattino la città sul record è vuota. Chi ha in mano il commerciale dice che il giro ha cancellato un dato buono. A volte ha ragione sul dato. La cella vuota può essere un export mal fatto, una colonna spostata, un file che ha tenuto le righe e ha perso i valori. Avere fastidio è il modo in cui ci si accorge dell'export. Non è il modo in cui si disegna il padrone di tutti i campi.

Se il motore, davanti al vuoto, lasciasse la città precedente, l'export mal fatto passerebbe in silenzio. La città vecchia resterebbe. Il file nuovo direbbe un'altra cosa. Le due cose convivrebbero, e il lunedì successivo nessuno saprebbe quale delle due è la sorgente. Si tornerebbe a scegliere a sentimento, che è il difetto del secondo archivio descritto nel primo capitolo. Il prodotto ha scelto l'altra convivenza: il fastidio è visibile, la città vuota è visibile, e si può tornare indietro su ciò che il giro ha scritto. L'annullamento fa questo. Non è una rete stesa davanti al vuoto per impedirgli di passare. È il modo di disfare una notte, dopo averla vista.

C'è un secondo fastidio, speculare, ed è quello che l'eccezione evita. La persona ha scritto una nota. Il file della notte porta la nota vuota, oppure porta una nota diversa, prodotta da un sistema che non conosce la frase del commerciale. Se la nota seguisse la città, il lunedì la frase sarebbe sparita. Il fastidio sarebbe giusto e la regola sarebbe sbagliata, perché quel campo non era stato dato alla sorgente. La nota resta. Il vuoto della città passa. Sono due decisioni, salvate prima, visibili sull'abbinamento, eseguite insieme.

Chi configura non deve ricordarlo a memoria la mattina dopo. Lo rilegge sull'abbinamento: per ogni campo, la sorgente oppure Espo. La sorgente vince anche se la cella è vuota. Espo protegge il valore già scritto da una persona. Il foglio di abbinamento, quello che si scarica e si ricarica, porta colonna, campo, trasformazione, padrone e se il campo è obbligatorio. La pagina di consegna elenca gli stessi padroni, senza segreti. Sono i posti in cui la cella vuota si può prevedere di giorno, con calma, prima che il file arrivi.

## La coda, quando i due testi non coincidono

Sulla nota, il caso che chiede uno sguardo non è la cella vuota. È la cella piena di un altro testo.

Il record ha la nota della persona. Il file porta una frase diversa. Il padrone è Espo. Il record esiste già, quindi non siamo nella creazione. Il campo non si tocca. Il valore arrivato finisce nella coda da guardare. Chi apre la coda vede che cosa c'è oggi e che cosa è arrivato. Può decidere con calma, di giorno. La notte si è fermata al non scrivere. Non ha applicato il testo del file «nel dubbio», e non ha svuotato il campo «per sicurezza» in attesa di quella decisione.

La coda non è un secondo CRM. Non tiene l'anagrafica vera in un posto parallelo, da cui poi si rincorre Espo. Tiene un contrasto, su un campo, per una chiave. L'Account resta su Espo. La nota che una persona legge aprendo l'Account è ancora la sua. Il contrasto è un promemoria. Non è una copia che vince di nascosto se nessuno la guarda entro un'ora. Non scade in una scrittura automatica. Resta da guardare.

Una cella vuota sulla nota non alimenta quella coda. Nessuno, al mattino, deve confermare il vuoto per salvare la frase. La frase non era in gioco. Questo evita un falso lavoro: la coda si riempirebbe di assenze, e il lavoro vero — un testo diverso, degno di lettura — si perderebbe in mezzo. Il vuoto è già stato deciso dal padrone. Il testo diverso no: il padrone dice di non scriverlo, e la coda dice di non dimenticarlo.

In creazione la coda, per la nota, non ha un testo già scritto con cui confrontare. È il caso di C001, e va tenuto separato. Lì la nota del file può entrare sul record, perché non c'è ancora una nota di persona. Dal giro dopo il confronto esiste, e da allora un testo diverso prende la via della coda.

Se sulla stessa riga la città va scritta vuota e la nota va in coda, il giro fa entrambe le cose quando scrive. La chiamata verso Espo porta la città vuota e non porta la nota nuova. La coda riceve la nota nuova. Il badge, se il giro ha scritto, dirà che l'ultimo passaggio sui campi toccati è il gestionale. La nota, non essendo stata toccata, resta il testo della persona. I tre segni — città vuota, nota intatta, riga in coda — raccontano la stessa notte senza contraddirsi.

## C001, che nasce

C001 non è ancora su Espo. Nel racconto il nome è Nord Est e la città è Trieste. Il giro la prepara come un Account nuovo. La chiave che nascerà, sulle schede che Espo ha già, sta nel campo cExternalKey: l'id dell'integrazione, due punti, e C001. Il formato appartiene al capitolo sulla chiave. Qui importa che la riga sia nuova, perché su una riga nuova il padrone della nota si comporta in un modo che dal giro dopo non si ripete.

In creazione il record non esiste. Non c'è una nota di una persona da proteggere. Per questo, in creazione, si scrive anche il campo il cui padrone è Espo. Se il file porta una nota per C001, quella nota può essere scritta insieme al nome e alla città. Non è una dimenticanza. È il motivo della protezione: la protezione vale per una nota già scritta da qualcuno. Stanotte nessuno l'ha ancora scritta, perché l'Account non c'è. «Può» vuol dire questo: se la cella della nota porta un testo, quel testo entra nella creazione. Se la cella della nota è vuota, non c'è un testo da posare, e non si usa il vuoto per preparare un campo bianco da proteggere. La protezione, dal giro dopo, protegge ciò che una persona avrà scritto, non un vuoto lasciato dal file la prima notte.

Dal giro successivo il padrone conta. Se una persona, dopo la nascita di Nord Est, scrive la sua nota, il file della notte dopo non la svuota. Se quel file porta un testo diverso, il testo va in coda e il campo resta quello della persona. C001, la prima notte, è il caso in cui la nota del file ha ancora un posto. La seconda notte è il caso in cui quel posto, se una persona lo ha occupato, appartiene a Espo.

Conviene leggere anche C001 cella per cella, perché è lo stesso file e non la stessa situazione della città bianca.

Il codice C001 non esiste ancora come record. Diventa parte della chiave. Non è un aggiornamento di un Account omonimo trovato per somiglianza di nome. Il primo capitolo ha già detto che due anagrafiche con chiavi diverse restano due record, e che un nome simile non è una fusione. Qui si usa solo la conseguenza: Nord Est nasce perché C001 non c'è, non perché il nome sia nuovo nel mondo.

Il nome Nord Est si scrive perché è della sorgente e la cella lo porta. La città Trieste si scrive per lo stesso motivo. Non c'è, su quei campi, una protezione da attivare dopo la prima volta. Se una notte futura la città di C001 arrivasse vuota, Trieste diventerebbe vuota, e sarebbe corretto per la stessa ragione per cui è corretto sulla riga già nota di stanotte. La prima notte non è quel caso: la prima notte Trieste c'è.

La partita IVA, se la cella la porta, si scrive come gli altri campi della sorgente. Se quel numero è già presente su un record diverso, si vede prima. C001, in quel caso, non nasce come secondo Account con lo stesso numero. L'anteprima lo mostra prima della scrittura. È lo stesso controllo della riga già nota, applicato a una nascita invece che a un aggiornamento. Il numero già presente ferma la riga e nomina il campo. Non sceglie in silenzio quale dei due Account «è quello giusto».

La nota, se c'è nel file, può essere scritta in questa creazione, come detto. Un campo non abbinato non viene riempito per l'occasione. Nord Est non riceve un telefono, una categoria o un qualsiasi altro dato che l'abbinamento non nomina, anche se una persona, più tardi, li compilerà a mano. Quei campi, quando qualcuno li compilerà, saranno protetti dal fatto di non essere nel giro, non dal padrone Espo. Il padrone Espo è una scelta su un campo che il file conosce. Il campo non abbinato è un campo che il file non ha il diritto di nominare.

La visibilità, se la regola c'è, si applica anche alla nascita. Nord Est può nascere nel team indicato, assegnato alla persona indicata. Il team viene da una colonna o è un team fisso, per esempio Vendite. La persona è una persona che in Espo c'è già. C001 non crea un utente perché nel file c'è un nome di commerciale. Su questo torno nella parte sulla visibilità: qui basta vedere che la nascita del record e la nascita di un login sono due gesti, e solo il primo appartiene a questa notte.

Il badge, dopo la creazione, dice chi ha scritto per ultimo. In questo momento ha scritto il giro. La frase, nella lingua del giro, dice che l'aggiornamento viene dal gestionale, con data e ora. Non è una cronologia legale di Nord Est. È il segno sull'Account appena nato. Quando, nei giorni successivi, una persona salverà la nota, il segno potrà diventare il suo nome. Fino a quel salvataggio, l'ultimo a scrivere è il file.

## C014, solo come contrasto

C014 è identica all'ultima volta. L'hash della riga è già quello salvato. Il capitolo sulla chiave e sull'hash spiega perché, in quel caso, Espo non viene richiamato. Questo capitolo non la apre. Non è la riga della città vuota e non è la riga nuova.

Serve da contrasto. Una riga invariata non incontra la regola della cella vuota, perché non c'è una cella nuova da applicare. Non si può usare C014 per dimostrare che il vuoto è innocuo. Il vuoto, su C014, non è arrivato. Se sulla stessa anagrafica la città fosse bianca, l'hash sarebbe un altro, il giro richiamerebbe Espo, e la città si svuoterebbe, perché la città è della sorgente. C014 di questa notte non è quel caso. È la riga che il giro lascia stare. Il resto del capitolo parla delle righe su cui c'è qualcosa da decidere: una nascita, un vuoto, una nota da non toccare, una riga che manca.

C014 non è nemmeno l'esempio della chiusura. È nel file. La chiusura riguarda chi nel file non c'è. Tenerle vicine nel racconto serve a non attribuire a una riga ferma i gesti delle righe che si muovono. Al mattino, chi cerca «che cosa è successo a C014» trova una risposta corta: niente, era invariata. La risposta lunga sulla cella vuota appartiene all'altra riga.

## Il badge non è uno storico

Sul record c'è un badge. Dice chi ha scritto per ultimo. Nel prodotto è il campo Origine Nesso. Non arriva da una colonna del file. Lo mette il giro quando scrive.

Se l'ultimo passaggio è il file, il badge dice che l'aggiornamento viene dal gestionale, con la data e l'ora, nella lingua del giro. Se dopo quel passaggio una persona salva il record, il badge dice che l'ultimo ritocco è di quella persona, col suo nome, la data e l'ora. Un salvataggio fatto dall'utente con cui Nesso parla a Espo non conta come ritocco di una persona. Quell'utente è il canale tecnico. Il badge non lo scambia per il commerciale che ha scritto la nota. Senza questa distinzione, ogni scrittura di notte sembrerebbe un ritocco umano, e il segno «chi ha scritto per ultimo» diventerebbe il nome del collegamento, sempre, e non servirebbe più a niente.

La lingua del badge è la lingua del giro. Un giro partito in italiano lascia la frase italiana. Un giro partito in inglese lascia la frase inglese. Cambiare lingua alla pagina, il giorno dopo, non riscrive il badge già messo, e non riscrive il giornale già scritto. Il pianificatore, che non ha una persona davanti, ha la sua lingua di giro. Questo diario non è quel verbale. Se si cerca nel giornale la prosa di questo capitolo, non la si trova. Si trova l'esito: che cosa è nato, che cosa è cambiato, che cosa è rimasto in coda, che cosa è chiuso, che cosa è stato scartato.

Il badge non conserva la serie delle note. Non dimostra chi ha scritto la città il mese scorso. Non è un registro da esibire come storia legale delle modifiche. Dice l'ultimo segno: o il gestionale, o una persona. Per la città svuotata, se il giro l'ha svuotata e nessuno ha salvato dopo, l'ultimo segno è il gestionale. Per la nota, se una persona l'ha salvata dopo il giro, l'ultimo segno è quella persona, anche se il file aveva portato un altro testo finito in coda. I due fatti stanno insieme. Il badge non sostituisce la coda. La coda non sostituisce il badge. Nessuno dei due sostituisce l'abbinamento, che è il posto in cui si legge il padrone.

Chi al lunedì chiede chi ha toccato il record ha una risposta corta, e deve sapere che è corta. Per disfare i valori dell'ultimo giro c'è l'annullamento, che torna indietro su ciò che quel giro ha scritto. Per la nota protetta c'è il padrone. Per il testo che il file voleva e non ha potuto scrivere c'è la coda. Per la nascita di Nord Est c'è il record stesso. Il badge, su tutti questi, dice solo l'ultimo autore del salvataggio che il prodotto riconosce come gestionale o come persona.

## La riga che non c'è più

Fin qui la riga era nel file. C'è l'altro caso. Il file di questa notte può non mostrarlo, e la regola deve comunque averlo: una riga che ieri c'era e stanotte non c'è.

Il record su Espo si chiude e resta nello storico. Chiudere non è cancellare. Il record si trova ancora. La nota, i legami, la città che c'era, il nome, restano da leggere su quell'Account. Chiudere non è il diritto all'oblio. L'oblio è un altro gesto, e non è questa chiusura. Questa chiusura non dimentica una persona e non svuota il record per farne sparire i dati. Segna che la sorgente non elenca più quella chiave, e lascia il record dov'è, nello storico.

La chiusura passa dalle API HTTP, come la città e come la creazione di Nord Est. È una scrittura dello stato che la scheda ha già, non una istruzione sulle tabelle di Espo. La scheda deve avere già uno stato su cui chiudere. Se lo stato non c'è, il giro non inventa un campo per l'occasione. Senza uno stato, la chiusura non parte. È un limite voluto: meglio non chiudere che chiudere su un campo inventato, o su una scheda che non ha un modo proprio per dire «chiuso».

La prima volta che un giro chiuderebbe dei record, chiede conferma. Il motivo è un file troncato. Un export interrotto può contenere una parte dell'elenco e presentarsi come un file intero: le colonne ci sono, le righe ci sono, solo che sono troppo poche. Se il giro trattasse quel file come l'elenco completo, i record assenti verrebbero chiusi senza che nessuno abbia visto il taglio. La conferma mette una persona in mezzo, la prima volta. Un file corto non chiude l'elenco da solo, non visto.

La conferma riguarda le chiavi che in quel giro risultano sparite. Dopo quel sì, la chiusura può compiersi. Non è un interruttore del capitolo quattro. Quegli interruttori — scritture ferme, modalità lettura, coda di ritento, filtro del portale, sigillo — restano un altro capitolo, e restano spenti finché qualcuno non li sceglie. La conferma della prima chiusura è la domanda propria di questo gesto. Si fa quando il giro sta per chiudere dei record per la prima volta, proprio perché un elenco più corto può essere un incidente e non una verità.

Un giro che non ha visto l'intera sorgente non tratta l'assenza come una sparizione. È il caso del cursore, e appartiene al secondo capitolo: se si cammina solo su ciò che è cambiato, non si sa chi manca. La conferma di cui si parla qui protegge l'altro incidente, quello del file che sembra completo ed è corto. Sono due cautele diverse. Questo capitolo tiene la seconda. La prima si indica e non si riscrive.

Un record chiuso può essere riaperto se la riga torna. Non era stato cancellato. C'è ancora un Account, con la sua chiave e la sua storia. Il ritorno della riga ha un record su cui posarsi. Non c'è un secondo archivio in cui la riga chiusa vivrebbe nel frattempo, in attesa. Vive su Espo, chiusa, nello storico. Il ritorno non è una creazione che dimentica la chiusura precedente. È la stessa scheda, che può tornare aperta perché c'è ancora.

C014 non illustra la chiusura: è nel file. C001 non illustra la chiusura: arriva, e nasce. La riga della città vuota non illustra la chiusura: è nel file, e si aggiorna. La chiusura riguarda solo chi manca. Tenerli in quattro casi distinti è il modo di non chiudere Nord Est perché Trieste è una città, e di non svuotare una città perché una riga diversa è assente.

## A chi si vede la riga

I valori e la chiusura non dicono chi, dentro Espo, vede il record. La visibilità è una regola, ed è una regola di Espo: questa riga è del team Vendite, assegnata a questa persona. Nesso non inventa un permesso fuori da Espo. Non tiene una seconda lista di chi può aprire Nord Est.

Il team e la persona arrivano da una colonna del file, oppure il team è fisso. Un team fisso Vendite vuol dire che le righe di questa integrazione sono di quel team, senza che il file debba ripetere il nome a ogni riga. Una colonna team vuol dire che la cella nomina il team di quella riga. Una colonna persona nomina l'assegnatario. Sono dati della regola di visibilità. Non sono una anagrafica di utenti da importare.

Gli utenti di Espo non si creano da un'anagrafica. Una colonna di persone non diventa un elenco di login. Creare un utente è un gesto di amministrazione: una password, un ruolo, un ingresso. Il file dei clienti non ha quel gesto dentro. Se la colonna nomina una persona, nomina qualcuno che come utente c'è già, e quella persona può essere assegnata. Se il nome non corrisponde a un utente, il file non ne fabbrica uno per far tornare la colonna. Una colonna «commerciale» piena di nomi non è un elenco di accessi. È, quando la regola lo dice, il modo di indicare l'assegnatario tra persone che esistono già.

La visibilità non svuota la nota e non riempie la città. Sta accanto, su un'altra riga dell'abbinamento. Nord Est, quando nasce, può nascere nel team indicato, assegnato alla persona indicata, se la regola è stata configurata. La città vuota di un record già esistente non è, di per sé, un cambiamento di team. Se la regola di visibilità è della sorgente e la cella del team porta un team, il team segue quella cella, come un campo della sorgente. Se il team è fisso, la cella non c'è e il fisso resta. In nessuno di questi passaggi nasce un login. Confondere il team con la città produce il sospetto che ogni svuotamento riassegni i clienti. Il sospetto si scioglie rileggendo l'abbinamento: la città è un campo, il team è la regola di visibilità.

Anche qui un dato non deciso non si inventa. Se la regola non nomina una persona, il giro non sceglie un commerciale a caso per C001 o per la riga della città vuota. Se non nomina un team, non ne crea uno per far quadrare la frase «ogni riga ha una casa». La frase del prodotto è più stretta. Quando la visibilità è configurata, questa riga appartiene al team detto, assegnata alla persona detta. Il team e la persona vengono da una colonna o da un team fisso. Gli utenti restano quelli che l'amministratore ha già creato.

## L'anteprima, la partita IVA, l'annullamento

Prima della scrittura si può aprire l'anteprima. Non scrive. Mostra che cosa nascerebbe e che cosa cambierebbe. Non sposta il file e non mette da sola le righe in coda: conta il giro, e si ferma.

Per la notte di questo capitolo, nascerebbe C001: nome Nord Est, città Trieste, e la nota del file se il file la porta, perché il record non esiste e il campo di Espo, in creazione, si scrive. Cambierebbe la città della riga la cui cella è vuota: si vedrebbe il passaggio dal valore di oggi al vuoto. C014 comparirebbe fra ciò che non cambia, perché è invariata. Una partita IVA già presente si vede prima, non dopo un POST. Se il numero di C001, o il numero della riga già nota, è già su un altro record, l'anteprima lo incontra prima che nasca un doppione.

L'anteprima mostra anche il contrasto della nota, quando il file porta un testo diverso da quello della persona: il valore di oggi e il valore in arrivo, senza applicare il secondo. È lo stesso contenuto che, se poi il giro scrive, finirà in coda mentre la città vuota verrà scritta. Chi guarda l'anteprima può quindi vedere, sulla stessa riga, un cambiamento vero e un cambiamento che non avverrà. Il primo è la città. Il secondo è la nota. Vederli insieme è il motivo per cui l'anteprima vale la pena, su questo file, più di un conteggio secco di righe.

Gli interruttori che fermano ogni scrittura, la modalità lettura, la coda di ritento, il filtro del portale e il sigillo stanno nel capitolo quattro. Qui l'anteprima entra solo come il modo di vedere la cella vuota e la nascita di C001 senza ancora averle scritte. Non è il capitolo di quegli interruttori. Non li accende. Non descrive come si sigilla un segreto o come si ritenta una riga scartata. Dice che, prima del gesto, si può guardare.

L'annullamento torna indietro su ciò che il giro ha scritto. Se il giro ha svuotato la città, annullare rimette il valore che c'era prima di quella scrittura. Quello è il passo indietro sul campo che il giro ha toccato. Se dopo il giro una persona ha cambiato il campo, e il valore non è più quello scritto dal giro, l'annullamento non copre quel cambiamento successivo. Torna indietro su ciò che il giro ha scritto, non su ciò che una persona ha scritto dopo. La nota della persona, se il giro non l'ha scritta, non entra in quel passo. Non c'era un valore del giro da ripristinare su un campo che la notte ha lasciato stare.

L'annullamento non è il diritto all'oblio. Non cancella Nord Est dal mondo, e non è la riapertura di un record chiuso raccontata come il contrario di una cancellazione. È il ritorno dei valori dell'ultimo giro, sui campi che quel giro ha davvero scritto e che nel frattempo nessuno ha sostituito. Si usa la mattina in cui la città vuota era un export sbagliato. L'anteprima, se è stata aperta prima, aveva già mostrato quel vuoto. L'annullamento è il gesto successivo, quando il vuoto è stato scritto e lo si vuole disfare.

## Ciò che resta spento

La scrittura di ritorno resta spenta. Non è accesa in questa notte, e questo capitolo non la descrive come se lo fosse. Accenderla è una scelta successiva ed esplicita. La tiene il quarto capitolo, insieme alla coda di ritento, al filtro del portale e al sigillo. La cella vuota non viene riscritta sul file da Nesso. La nota della persona non viene depositata nel file di notte da questo giro. Il file entra. I campi della sorgente seguono il file, vuoti compresi. I campi di Espo restano su Espo. Il ritorno, se un giorno qualcuno lo vorrà, sarà un'altra decisione, presa a parte, non una conseguenza della cella vuota e non un modo per «rimettere la città» nel file senza aver nominato le colonne.

Il passaggio, in tutte le direzioni di questo capitolo, è solo via API HTTP. Svuotare la città è una chiamata. Creare Nord Est è una chiamata. Leggere la nota già presente, per sapere se il testo in arrivo è diverso, è una chiamata. Chiudere un record sparito è una chiamata, sullo stato che la scheda ha già. L'annullamento, quando rimette il valore precedente, è una chiamata. Le tabelle di Espo non sono un canale. Non lo sono per aggiustare a mano la cella vuota con una query, e non lo sono per leggere «più in fretta» il valore della nota. Chi ha in mente la query sta pensando al gesto che il primo capitolo ha messo fuori dal confine.

## Che cosa questo giro non è

Nesso non è un secondo CRM. La verità della città è la cella, perché la città è della sorgente. La verità della nota è il record, perché la nota è di Espo. Non c'è una terza città tenuta nel motore nel caso il file esageri. Il motore ricorda il giro: hash, cursore, coda, giornale, chiavi viste. Sono memorie del passaggio, e il capitolo sulla chiave le separa dai record. Non sono l'anagrafica. Aprire quelle memorie non mostra un cliente parallelo a Nord Est. Mostra se la riga era già stata vista, se un contrasto aspetta, se un giro si può annullare.

Questo file non è un connettore certificato. L'abbinamento è stato letto da una persona. Il nome del sistema che ha posato il file nella cartella non sta nel programma. La ricetta di anagrafiche, se è stata usata come punto di partenza, resta un punto di partenza: propone campi, non certifica un gestionale, e non si salva da sola. La persona rivede i padroni e poi salva. La cella vuota è corretta perché quel salvataggio ha lasciato la città alla sorgente, non perché un certificato dica che la colonna città di un certo prodotto va trattata così.

Non è la storia di un cliente. Nord Est e Trieste sono il nome e la città dell'esempio, gli stessi della prima lettura. Non c'è un'azienda da riconoscere dietro il codice C001. Non c'è una referenza, e non c'è un caso da citare come prova commerciale. Il file serve a vedere la regola su righe piccole: una nasce, una non si muove, una perde la città, una nota resta.

La posta non entra in questo giro. La posta del CRM resta in Espo. Il file delle anagrafiche non spedisce e non legge una casella. La nota è un campo del record. Non è un messaggio. Trattarla come posta, perché è un testo scritto da una persona, mescolerebbe il padrone del campo con un altro mestiere, e con un altro segreto. Il segreto di una casella non è il segreto di un file di anagrafiche. Qui non c'è né l'uno né l'altro da raccontare: c'è una cella, e c'è un campo.

## Il lunedì, la stessa notte

Conviene raccontare la stessa notte un'altra volta, nell'ordine in cui una persona la incontra il lunedì, senza aggiungere fatti.

Apre l'anteprima, se vuole vedere prima di scrivere. Vede C001 che nascerebbe: nome Nord Est, città Trieste, e la nota del file se c'è, perché il record non esiste e la nota il cui padrone è Espo, in creazione, si può scrivere. Vede la riga già nota la cui città arriverebbe vuota: il cambiamento è la città. La nota di quella riga, se una persona l'ha scritta, non è fra i cambiamenti. Se il file porta un testo diverso, l'anteprima mostra il valore di oggi e quello in arrivo, e quel campo non verrebbe scritto. Vede C014 fra ciò che non cambierebbe. Vede, prima della scrittura, una partita IVA già presente, se c'è, e la riga che la porta non diventa un secondo Account in silenzio. Se l'elenco è più corto di ieri e il giro ha visto l'intera sorgente, vede che una chiusura chiederebbe conferma la prima volta, e che senza quel sì i record non verrebbero chiusi non visti.

Poi, se il giro parte davvero, le scritture sono quelle che l'anteprima aveva contato. C001 diventa un Account, via HTTP. La città della riga col vuoto diventa vuota, via HTTP, perché quel campo è della sorgente. La nota della persona resta sul record. Il testo diverso, se c'era, è in coda da guardare, e il campo non è cambiato. I campi non abbinati sono come prima. Il team e la persona sono quelli della regola di visibilità, da colonna o da team fisso, e nessun login è nato dal file. Il badge, sui record che il giro ha scritto, dice che l'ultimo a scrivere è il gestionale, nella lingua del giro, finché una persona non salva. Un salvataggio dell'utente tecnico non sposta quel segno su un nome di persona. Il giornale di quel giro resta nella lingua in cui il giro è partito. Racconta l'esito, non questo capitolo.

Se la città vuota era un errore del file, l'annullamento torna indietro su ciò che il giro ha scritto. La città può tornare al valore precedente, se nel frattempo nessuno ha scritto un altro valore su quel campo. La nota che il giro non ha toccato non ha bisogno dell'annullamento per esistere: non se n'era andata. Annullare non svuota la coda al posto di una persona che deve ancora guardare il testo diverso, e non trasforma la coda in una scrittura.

Se una riga manca e qualcuno conferma la prima chiusura, il record si chiude e resta nello storico. Non è cancellato. Non è il gesto con cui si dimentica una persona. Se più avanti la riga torna, il record chiuso può essere riaperto, perché c'è ancora. La storia letta sul record non è stata sostituita da un buco.

Durante tutto questo la scrittura di ritorno è rimasta spenta. Nessun interruttore del quarto capitolo è stato acceso per far funzionare la cella vuota. La cella vuota funziona con la regola del padrone. Il file entra. Espo riceve, via HTTP, i campi della sorgente, vuoti compresi. I campi di Espo, dopo la creazione, restano a chi li ha scritti sul record.

## Due scrivanie, gli stessi fatti

La stessa notte si può rileggere dalle due persone che il primo capitolo ha già messo davanti al file, senza rifare il loro ritratto. Qui importa che cosa ciascuna vede di questa regola, e che nessuna delle due vede un fatto che l'altra non potrebbe verificare.

Chi ha scritto la nota apre l'Account. La frase c'è ancora, se c'era prima del giro e il record non era in creazione. La città può essere vuota. Il badge può dire che l'ultimo passaggio del gestionale è di stanotte, oppure, se questa persona salva dopo aver controllato, che l'ultimo ritocco è il suo. In coda, se il file aveva un altro testo, c'è quel testo, da guardare, e non è stato scritto al posto della frase. Questa persona non ha bisogno di sapere come è fatta la chiave. Ha bisogno di sapere che il padrone della nota è Espo, e che il padrone della città è la sorgente. Le due frasi spiegano il mattino per intero.

Chi conferma le chiusure, o chi ha il compito di dire sì la prima volta, guarda un altro elenco: le chiavi che nel file non ci sono più. Non guarda la città di chi c'è ancora. Un file troncato si riconosce lì, dall'ampiezza dell'elenco che si vorrebbe chiudere, non dal fatto che una città sia bianca. Dire sì chiude e lascia lo storico. Non dire sì lascia i record aperti, ancora elencati dalla sorgente precedente, in attesa di un file che sia davvero l'elenco. Nessuna delle due risposte cancella, e nessuna delle due è l'oblio.

Chi ha configurato l'abbinamento, il lunedì, non scopre la regola. La rilegge. La città è sorgente. La nota è Espo. Il team è la regola di visibilità. Gli utenti non nascono dal file. L'anteprima, se l'ha aperta, aveva già separato C001, la città vuota, C014 e il contrasto della nota. Il giornale conferma l'esito nella lingua del giro. Se qualcosa nel giornale e in questo diario non torna, si apre il manuale. Il diario può essere stato letto in inglese o in italiano. Il giornale no: è rimasto quello della notte.

## Il giro dopo, su Nord Est

Il giorno dopo, o la notte dopo, il padrone che in creazione aveva fatto un'eccezione torna alla regola ordinaria. Vale la pena raccontarlo su Nord Est da solo, perché è lo stesso record e non è più la stessa situazione.

Nord Est esiste. Trieste, se il file la riporta, resta o viene riscritta uguale: è della sorgente. Se il file di quella seconda notte porta la città vuota, Trieste se ne va, ed è lo stesso fastidio corretto della riga già nota. Non c'è una franchigia per i record nati da Nesso. Essere nati ieri non rende la città di proprietà della persona.

La nota, se in creazione il file l'aveva portata e nessuno l'ha ancora cambiata, è il testo posato la prima notte. Se una persona nel frattempo l'ha sostituita con la sua, il padrone Espo protegge la sua. Il file non la svuota. Un testo diverso del file va in coda. Il campo resta. Il badge, se la persona ha salvato, nomina la persona. Se nessuno ha salvato dopo il giro, e il giro ha comunque scritto altri campi della sorgente, il badge nomina il gestionale, e la nota della persona è comunque lì: il badge dice l'ultimo, non dice che ogni campo del record è stato riscritto da quell'ultimo.

C014, se resta identica, continua a non essere argomento. Una riga assente, se il file la perde e la prima chiusura è già stata confermata in un giro precedente, si chiude restando nello storico. Se torna, può essere riaperta. Nessuno di questi passi accende la scrittura di ritorno. Nessuno crea un utente. Nessuno parla alle tabelle.

## Che cosa questo capitolo non ha fatto

Non ha rifatto il confine. Espo sta ancora da una parte, il canale dall'altra, e il primo capitolo resta il posto di quella frase. Non ha spiegato come si calcola l'hash di C014, né come il cursore ricorda l'ultimo record mandato: è il secondo capitolo, e qui C014 entra solo per dire che una riga invariata non è una cella vuota. Non ha acceso la scrittura di ritorno, non ha descritto la coda di ritento, non ha aperto il filtro del portale e non ha messo il sigillo. Il quarto capitolo tiene quelle cose, e spente restano anche dopo che la città si è svuotata.

Ha seguito un file, di notte, campo per campo. La sorgente vince, e vince anche quando la cella è vuota, sui campi di cui è padrona e che non sono stati segnati come obbligatori. La città si svuota perché è sua. La nota non si svuota perché è di Espo, salvo in creazione, quando non c'è ancora una nota da proteggere e C001, Nord Est, Trieste, può ricevere la nota del file. Dal giro dopo, su quel record, il padrone conta. Un testo diverso aspetta in coda e non sostituisce la frase. Il badge dice l'ultimo autore, non la storia legale. La riga sparita chiude, non cancella, non dimentica, e la prima volta chiede un sì, così un file troncato non chiude l'elenco non visto. Se la riga torna, il record può essere riaperto. La visibilità assegna il team Vendite e la persona, da una colonna o da un team fisso, e una colonna di persone non diventa un elenco di login. L'anteprima mostra che cosa nascerebbe e che cosa cambierebbe, e una partita IVA già presente si vede prima. L'annullamento torna indietro su ciò che il giro ha scritto. Il manuale, se questo diario e il manuale non dicono la stessa cosa, è quello che resta.
