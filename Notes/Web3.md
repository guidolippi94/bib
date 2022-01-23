# Web3
---
Created: 05 gennaio 2022 11:40
Tags: #blockchain #web3 
Reference:

---
## Cos'è Web3
[Web2 vs Web3 Ethereum](https://ethereum.org/it/developers/docs/web2-vs-web3/)
[web1 vs 2 vs 3](https://www.themarketingfreaks.com/2014/02/web-1-0-web-2-0-e-web-3-0/)

Per iniziare a parlare di Web3 è fondamentale innanzitutto comprendere quelle che sono classificabili come versioni precedenti del web. La distinzione su cui si pone l'attenzione è quella basata sull'analisi del flusso di creazione e consumo dell'informazione, che ha sancito la possibilità di discriminare le varie versioni.
Nel Web1 o semplicemente Web, vediamo la nascita di reti di comunicazione globali e massive in cui la maggioranza del contenuto è generato da aziende che danno la possibilità ai propri utenti di fruire dei contenuti creati, sfogliare cataloghi e acquistare i propri prodotti o servizi. La comunicazione è quindi perlopiù unidirezionale, dall'alto verso il basso.
Il Web2 invece sposta il paradigma verso l'utente, ponendo interazione e condivisione al centro del sistema.
Questa fase vede la nascita e l'espansione dei social network e dei blog, in cui è proprio l'utente finale a generare contenuto e ad interagire con la piattaforma o gli altri utenti. Questo tuttavia non ferma le aziende dal generare contenuti per attrarre nuovi clienti, ma cambia radicalmente le tecniche e la comunicazione che queste adottano.
Abbiamo infine il Web3, da non confondere con il Web 3.0, cioè una versione semantica del Web2 che sfrutta l'impiego di intelligenza artificiale, ambienti 3D e portabilità dei sistemi.
Il Web3 preso in analisi in questo elaborato, cioè nel contesto blockchain, si riferiscce ad una nuova infrastruttura basata sullo sviluppo di app decentralizzate che vengono eseguite sulla blockchain stessa, che consentono di essere sviluppate da chiunque e di implementare nuovi modelli di business che non siano basati sulla monetizzazione dei dati personali.
I principali vantaggi dei sistemi Web3 sono: il deploy delle app è sempre permission-less, nessun utente può essere impossibilitato all'accesso al servizio, i pagamenti sono incorporati tramite i token nativi delle blockchain.
Le limitazioni imposte dai vincoli architetturali sono attualmente di importante entità: la scalabilità è limitata dalla decentralizzazione, rendendo di fatto il sistema più lento, lo sviluppo di interfacce utente e UX è più complesso in quanto ancora devono essere definiti degli standard a cui l'utente finale deve abituarsi, ed infine il costo di rilascio degli applicativi su blockchain è molto elevato, costringendo gli sviluppatori a caricare su blockchain solo piccole porzioni di codice.

## Applicativi decentralizzati (DAPP)
Si definisce applicazione decentralizzata o dapp un'applicativo che integra uno o più smart contract con un'interfaccia utente. 
Lo sviluppo di dapp è fondato sul paradigma di scissione tra front-end (interfaccia utente) e back-end.
Il back-end di una dapp viene eseguito su una rete decentralizzata P2P ed è costituito da uno o pi smart contract. Essendo questi pubblicamente accessibili è possibile implementare nella propria dapp anche smart contract sviluppati da terzi, senza necessità di richiedere approvazione e senza che questa possibilità venga preclusa.
Il front-end invece può essere sviluppato sfruttando tutti i sistemi tradizionali, solitamente vengono sfruttati i moderni framework Javascript come ReactJS o VueJS. L'hosting del frontend può essere eseguito sia su piattaforme di storage decentralizzato che su server centralizzati, questo non va ad inficiare i benefici apportati da un sistema basato su blockchain.

Le app decentralizzate apportano grandi vantaggi all'utente finali, infatti non si sperimentano tempi di inattitività, grazie all'infrastruttura totalmente decentralizzata, la quale garantisce anche una protezione pressoché totale di attacchi DoS verso una singola dapp.
La privacy degli sviluppatori è sempre garantita, in quanto per distribuire una dapp non è necessario fornire i propri dati personali.
I dati forniti da uno smart contract e quindi da una dapp sono sempre assolutamente integri, poiché sono tutti conservati su una blockchain e pertanto immutabili e garantiti dal sistema crittografico che sta alla base di questa. 
Tutte le dapp godono della proprietà di "trustless", cioè la loro esecuzione è sempre prevedibile, senza necessità alcuna di doversi fidare di un'entità centrale.
I benefici che questa tecnologia apporta agli utenti non è esente da importanti limitazioni ed impedimenti, in particolar modo per quello che riguarda gli sviluppatori.
Un dapp infatti risulta molto complessa da mantenere e aggiornare, in quanto uno smart contract generalmente non può essere aggiornato, ma solamente distrutto e ricreato, lasciando comunque traccia del suo ciclo di vita nella blockchain.
A causa della decentralizzazione, del fatto che ogni nodo deve mantenere la copia di ogni transazione e della proof-of-work è stimato un overhead computazionale di un fattore 10^6 rispetto ai servizi tradizionali.
Anche l'esperienza utente è notevolemente impattata, in quanto ancora il pubblico generalista risulta poco formato rispetto a queste tematiche e potrebbe trovare complesso dover eseguire una serie di passaggi tecnici per poter sfruttare a pieno le potenzialità del sistema. Un classico esempio di utilizzo di una dapp prevede infatti la creazione di uno wallet come Metamask, la connessine di questo alla dapp e la conseguente approvazione.

## Criticità del Web3
Il Web3 sta riscuotendo un grande successo a livello sia mediatico, sia di implementazioni, grazie all'enorme entusiasmo generato dal mondo delle cryptovalute. Questo può essere un beneficio nel momento in cui le cryptovalute verranno regolate e diventeranno un standard realmente utilizzabile in tutto il mondo. D'altro canto questo potrebbe anche essere un grande punto a sfavore per il Web3, poiché se il mercato delle crypto, e la relativa eccitazione, stanno vivendo, come molti suppongo, una "bolla", allora un collasso del sistema crypto provocherebbe danni probabilmente irreparabili anche al mondo Web3.
Dal punto di vista tecnico però, un sistema di app decentralizzato come quello preso in esame, non deve necessariamente vivere su un ecosistema blockchain, infatti è possibile realizzare dapp anche sfruttando reti decentralizzate di approccio più classico, in cui si mantengono tanti dei vantaggi offerti da una blockchain, se ne superano alcuni vincoli, come il prezzo e i tempi di deploy di un app, e indubbiamente si perdono alcune peculiarità, come ad esempio il sistema di pagamento integrato e nativo.
Un'altra criticità riguarda lo storage per gli applicativi Web3. Archiviare un qualsiasi tipo di dato in una blockchain, attualmente è esageratamente costoso e poco prestante, per cui è di fatto impossibile pensare di poter pubblicare un'intera applicazione su blockchain. Per superare tale vincolo, gli sviluppatori, sono soliti limitare al minimo indispensabile la scrittura di contratti e quindi le porzioni di back-end che saranno pubblicate su blockchain, mentre tutto il resto dei dati, sia front che back-end sono pubblicati su server centralizzati tradizionali.

## Autenticazione
A differenza dei sistemi che quotidianamente vengono usati da ogni persona connessa ad internet, nel Web3 è stato profondamente modificato il paradigma di autenticazione.

[Sistemi di autenticazioe wikipedia](https://en.wikipedia.org/wiki/Authentication)

I principali modelli tradizionali di autenticazione si possono distinguere in autenticazione a fattore singolo e autenticazione a fattore multiplo.
I fattori di autenticazione si possono distinguere in fattori di conoscenza, cioè qualcosa che l'utente sa, come una password, fattori di possesso, cioè qualcosa che l'utente possiede, come una smart card, ed infine fattori di inerenza, cioè qualcosa che l'utente è o fa, come l'impronta digitale o il pattern vocale.
Nel caso dell'autenticazione a singolo fattore, come esplica il nome, l'utente dovrà fornire uno solo dei 3 possibili fattori di autenticazione, rendendola di fatto la più vulnerabile.
Mentre nel caso dell'autenticazione a fattore multiplo l'utente dovrà superare più passaggi di autenticazione che coinvologono, generalmente fattori di autenticazione diversi.
In aggiunta ai due modelli di autenticazione visti sopra è possibile identificarne altri:
l'autenticazione continua, che si fonda sull'osservare i comportamenti del'utente o dell'entità registrata sul sistema ed ha la possibilità di rimuove l'autorizzazione in ogni istante, all'insorgere di comportamenti sospetti;
l'autenticazione step-up invece combina la semplicità dell'autenticazione a fattore singolo, per fornire all'utente un accesso a proprietà basilari del sistema, mentre per scalare i propri privilegi quest'ultimo dovrà superare ulteriori fattori di autenticazione.

Un esempio di autenticazione tradizionale a 2 fattori, anche detta 2FA, prevede che l'utente si registri al sistema tramite l'impiego di username e password, per poi inserire un codice PIN generato da un'applicazione associata.

A differenza dei sistemi citati sopra, nel mondo Web3 il sistema di autenticazione offre la possibilità agli utenti di interagire direttamente o indirettamente con una o più blockchain.
Il processo più comune di autenticazione in una dapp prevede l'impiego di un wallet, come ad esempio Metamask, che garantisce accesso a molteplici blockchain. In questo caso l'autenticazione sfrutta il sistema crittografico a chiave pubblica con il quale il wallet è stato generato e assicurando la validità del certificato di autenticazione grazie alla firma con chiave pubblica. Tuttavia, per come è costruita la rete, non è possibile associare l'identità di una persona a quella del wallet, lasciando di fatto l'utilizzatore anonimo.
Eseguendo l'accesso ad un sistema tramite la connesione di un wallet corrisponde all'autenticazione a singolo fattore nei sistemi tradizionali. Tuttavia è possibile, e sotto opportune ipotesi persino consigliato, aggiungere ulteriori layer di sicurezza. Per fare ciò è possibile utilizzare tutti i fattori di autenticazione elencati sopra. 

Un esempio di autenticazione in una dapp prevede appunto la connessione del poprio account Metamask all'applicativo tramite accettazione della richiesta popup proveniente dall'estensione Metamask per i comuni browser. Sucessivamente possono essere richiesti ulteriori fattori di autenticazione, come l'inserimento di un password, di un PIN usa e getta o perfino l'acquisizione di dati biometrici.


[]() 
