# Smart Contract
---
Created: 20 dicembre 2021 23:15
Tags: #smartcontracts #tesi 
Reference:

---
## Cosa sono e come funzionano gli smart contracts
[Storia smart contracts](https://etherevolution.eu/storia-degli-smart-contract/#:~:text=L'idea%20di%20%E2%80%9Csmart%20contract,un%20paper%20pubblicato%20nel%201996.&text=in%20maniera%20affidabile.-,L'idea%20di%20%E2%80%9Csmart%20contract%E2%80%9D%20fu%20coniata%20per%20la,un%20paper%20pubblicato%20nel%201996.)
L’idea di “**smart contract**” fu coniata per la prima volta da **Nick Szabo**, un informatico e crittografo, in un paper pubblicato nel 1996. La sua ideazione quindi risale ad un periodo antecedente al rilascio di tecnologie basate su blockchain, tuttavia hanno trovato in queste un terreno fertile per applicazioni nel mondo reale.

Gli smart contract sono semplicemente **script di codici che funzionano autonomamente e che funzionano esattamente secondo come sono stati programmati**, permettendo alle transazioni o agli accordi di essere portati avanti in maniera affidabile.
Questo **elimina la necessità di servizi da parte di intermediari e diminuisce le possibilità di conflitti, inattività, frode o interferenze da parte di terzi**.

Il primo promotore di smart contract su rete blockchain fu Vitaliy Buterin, che nel 2014, a soli 17 anni, ha dato vita al celeberrimo progetto _Ethereum_, in cui ogni transazione all'interno della rete avviene sotto forma di smart contract. Tale implementazione ha posto le basi per successivi sviluppi di tecnologie che si appoggiano sulla rete di Ethereum e permettono la creazione di applicazioni innovative.

Il nome _smart contract_ potrebbe risultare fuorviante, in quanto riporta subito alla mente l'idea di un contratto digitale, interpretandolo come un tradizionale contratto riportato in un ambiente informatizzato.
Più semplicemente invece, si definisce smart contract, un programma in grado di essere eseguito su rete blockchain che opera in modalità **if this - then that**, cioè esegui un operazione prestabilità all'occorrenza di un particolare evento.
In termini pratici uno smart contract è composto da una collezione di codice, che implementa le sue funzionalità, e una serie di dati, cioè lo stato del contratto. Esso sarà sempre raggiungibile ad uno specifico indirizzo sulla rete blockchain.

In particolare, per quanto riguarda la rete Ethereum, che da ora in poi prenderemo come riferimento per gli smart contract in questo elaborato, uno smart contract è un tipo particolare di account ethereum. Di conseguenza, come ogni altro account, questo avrà un bilancio, cioè un certo ammountare di token _Ether_, che potrà distribuire arbitrariamente all'interno della rete.Tuttavia a differenza di un regolare account utente, gestito da un umano, ogni movimentazione di token sarà effettauta in base al codice che viene eseguito al suo interno. 
Un esempio pratico di facile comprensione è quello della _vending machine_:
Lo smart contract interpreta il ruolo del distributore automatico, che al suo interno è caricato con un certo numero finito di snack.
Un utente che si interfaccia con lo smart contract, o il distributore, dovrà inserire un predefinito ammontare di denato, selezionare lo snack e ritirare lo stesso.
Lo smart contract sarà programmato per eseguire automaticamente la funzione di calcolo dell'ammontare richiesto per la selezione effettuata dal cliente, verificare che quest'ultimo abbia introdotto o disponga di una quantità sufficiente di denaro e in caso positivo erogare lo snack, mentre in caso negativo rifiutare la transazione.


---

Gli smart contract sono definiti [[permissionless]], cioè possono essere scritti e pubblicati sulla rete Ethereum senza alcuna approvazione. 
Gli unici requisiti per la creazione e la pubblicazione sono:
- avere le competenze per scrivere codice nel linguaggio adeguato
- avere Ether a sufficienza per pagare la transazione, cioè la pubblicazione del contratto

Ogni transazione quasi tutte le reti blockchain richiede il pagamento di una  quantità variabile di denaro, generalmente espressa in token, per far si che questa venga eseguita e quindi inserita nel prossimo blocco minato dalla rete.
Questa "tassa" prende il nome di _ #gas fee_, ed è la ricompensa che viene assegnata ai miner per la potenza di calcolo messa a disposizione. In questo modo utenti ed aziende sono incentivati a minare, rendendo la rete sempre più grande e prestante.

I principali linguaggi di programmazione per smart contract su Ethereum sono Solidity e Vyper. Il primo presenta una sintassi similare al Javascript, linguaggio ampiamente utilizzato in ambito web, mentre il secondo ha una sintassi simile al Python, ma entrambi consentono di sviluppare smart contract completi e funzionanti.
Un altro grande vantaggio degli smart contract è quello della possibilità di essere composti tra loro. Ciò significa che un contratto può richiamare dal suo codice interno un altro contratto nella rete, estendendo così le proprie funzionalità. 

Oltre ai molteplici vantaggi che un sistema di smart contract offre, ci troviamo a dover affrontare anche numerose ed importanti limitazioni.
Una delle limitazioni più importanti riguarda il non poter comunicare con il mondo esterno alla rete su cui sono pubblicati, infatti i contratti sono impossibilitati nel fare richieste HTTP, in quanto potrebbero andare ad inficiare la sicurezza offerta dal sistema. Questo limite sta trovando una soluzione negli oracoli, sistemi in grado di far comunicare il mondo reale con le reti blockchain, in modo affidale, non corruttibile e automatizzato.


## User authentication in smart contracts web3

## Sicurezza negli smart contracts
Gli smart contract pubblicati sulla rete blockchain attirano l'interesse di soggetti malintenzionati in quanto spesso contengono quantità di token rilevanti e di conseguenza un alto valore in denaro. Questi possono essere soggetti a tecniche di exploiting che vedremo di seguito, pertanto è necessario seguire le buone pratiche consigliate dalle documentazioni ufficiali dei vari progetti blockchain sui quali è possibile creare contratti di questo tipo.

La sicurezza degli smart contract, come del resto di ogni altro prodotto software, non risiede esclusivamente in un buon codice privo di bug, ma anche in una buona ricerca e progettazione di tutto il sistema da implementare.

### Processo di sviluppo di uno smart contract
La documentazione di Ethereum fornisce una lista di punti chiave su cui fondare lo sviluppo di uno smart contract:
- Usare sistemi di versionamento del codice, come Git
- Revisione del codice da parte di uno sviluppatore terzo prima che questo sia approvato e pubblicato
- Usare sistemi di testing automaizzato, come Truffle
- Documentare il codice


### Attacchi agli smart contract
[Elenco di attacchi agli smart contract](https://consensys.github.io/smart-contract-best-practices/known_attacks/)

Di seguito vengono presentati alcuni degli attacchi più conosciuti e attuati nei confronti di smart contract.

L'attacco **re-entrancy** sfrutta l'architettura di Ethereum per l'esecuzione di un contratto. Al momento della chiamata ad uno smart contract, la rete Ethereum, detta EVM (Ethereum Virtual Machine), non può eseguire altri contratti. Se il contratto deve eseguire chiamate ad altri contratti, questo viene messo in pausa per poter eseguire il contratto richiamato, per poi riprendere il controllo una volta terminata l'esecuzione. Questa pratica espone una vulnerabilità detta apunto re-entrancy. Grazie a questa vulnerabilità l'attaccante può prendere il controllo al momento della chiamata ad un contratto esterno ed eseguire delle modifiche ai dati, per forzare ad un comportamento indesiderato il contratto chiamante.

Un esempio di codice soggetto a re-entrancy è il segente:
```javascript
mapping (address => uint) private userBalances;

function withdrawBalance() public {
    uint amountToWithdraw = userBalances[msg.sender];
	// In questo punto l'attaccante può richiamare la funziona withdrwaBalance per eseguire un nuovo ritiro di denaro senza che il suo saldo sia ancora stato azzerato. 
    (bool success, ) = msg.sender.call.value(amountToWithdraw)(""); 
    require(success);
    userBalances[msg.sender] = 0;
}

```
Mentre una versione del codice che non espone questa vulnerabilità è la seguente:
```javascript
mapping (address => uint) private userBalances;

function withdrawBalance() public {
    uint amountToWithdraw = userBalances[msg.sender];
	// Azzerando il saldo ritirabile prima di eseguire l'azione di ritiro dei token ci assicuriamo che l'attaccante non possa eseguire molteplici volte l'azione facendola andare a buon fine
    userBalances[msg.sender] = 0;
    (bool success, ) = msg.sender.call.value(amountToWithdraw)(""); 
    require(success);
}

```

L'attacco Cross-function Reentrancy è una variante della versione base di re-emtrancy in cui l'attaccante sfrutta lo stato condiviso da due funzioni all'interno dello stesso contratto.

La buona norma per evitare attacchi di questo tipo è quella di eseguire  innanzitutto tutte le operazioni interne al contratto e solo infine eseguire le chiamate a contratti esterni, così da azzerare o limitare al minimo le possibilità di exploiting re-entrancy.

Un altro tipo di attacco agli smart contracts Ethereum è denominato **Front Running**. A differenza del re-entrancy questo non mina la funzionalità di uno smart contract soggetto a vulnerabilità, ma adotta una strategia per generare guadagni per l'attaccante sfruttando informazioni che questo non dovrebbe possedere.
Questa tecnica è usata anche nel mercato azionario, infatti l'attaccante cercherà di leggere le richieste di ordini di token che vengono fatte ad esempio dagli utenti verso un exchange, ente terzo per trading di criptovalute, e piazzerà il suo ordine prima che questo venga effettivamente evaso dall'exchange. In questo modo l'attaccante riuscirà ad aggiudicarsi dei token ad un prezzo più vantaggioso, andando a rivenderlo poco dopo ad un prezzo sicuramente maggiore di quello di acquisto.
Non è semplice trovare soluzioni a questa tipologia di attacco, alcune pratiche sfruttano l'evasione di ordini basata sul timestamp della richiesta, altre sulla confidenzialità della richiesta, sfruttando tecniche di hashing delle informazioni.

L'attacco **Integer Overflow and Underflow**  punta a minare l'integrità del dato di uno smart contract. I numeri interi negli smart contract in formato _uint_ possono rappresentare al più il numero decimale 2^256.
Al raggiungimento della soglia limite, un incremento ulteriore farebbe tornare il numero a 0, compromettendo così l'integrità del contratto.
Generalmente sono soggetti a questa vulnerabilità contratti che consentono la l'incremento di un certo valore a tutti gli utenti, senza regolarne l'accessibilità e i limiti. 

Un attacco chiamato  **DoS with (Unexpected) revert** sfrutta le vulnerabilità degli smart contracts che necessitano di interagire più volte con l'attaccante per proseguire la propria esecuzione.
Un ottimo esempio riguarda sistemi di aste su blockchain. Non avendo enti terzi che facciano da garante ogni smart contract, per validare un'offerta, deve ricevere la somma dell'offerta per intero. Al momento in cui un nuovo utente effettua un'offerta più alta il contratto rimborserà l'utente precedente per poi accettare la nuova. 
L'attaccante una volta eseguita l'offerta, farà si che il proprio contratto esegua una funziona di callback che, al momento in cui arriverà la funzione di richiesta del rimborso la respinga automaticamente, aggiudicandosi così obbligatoriamente l'asta al prezzo della prima offerta.

Gli attacchi di tipo **dusting** vengono eseguiti inviando piccoli ammontare di token a un vasto numero di wallet differenti. Al momento le principali blockchain non consentono ad un utente di rifiutare una transazione che apporti token al proprio wallet, per cui i token inviati vengono accreditati.
L'attaccante cercherà poi di risalire all'identità dell'utente o della compagnia proprietaria del wallet tracciando le transazioni che includono questi token inviati in modo malevolo. In caso l'identità venga scoperta si avrà la perdita permanente dell'anonimato del proprietario.
L'unica attuale mitigazione di questo attacco consiste nell'individuazione dei token "dust", nella creazione di un nuovo wallet e nello spostare tutti i token e gli asset corretti che non fanno parte dell'attacco nel wallet appena creato.

[Smart contracts attacks](https://freemanlaw.com/blockchain-attacks-is-no-one-safe-in-the-world-of-cryptocurrencies/)

**DOS with Gas limit**
Ogni blocco ha un limite superiore alla quantita di gas che può essere spesa, direttamente proporzionale alla computazione che può essere eseguita.
Se il gas limit viene ecceduto allora la transazione fallisce, ed è qui che un attaccante può intervenire per mettere in atto attacchi di tipo Denial of Service.

Questi attacchi possono sfruttare vulnerabilità in caso di pagamenti a indirizzi multipli simultaneamente. Un attaccante può inserire diverse piccole transazioni in un contratto che esegue un ciclo su gli address a cui inviare token, così da far si che il gas limit venga superato, facendo fallire la transazione per tutta la durata dell'attacco.


## Gli oracoli
[Oracoli ethereum](https://ethereum.org/it/developers/docs/oracles/#top)

I sistemi basati su blockchain consentono la creazione di applicazioni in grado di sfruttare tutte le loro potenzialità fintanto che i dati utilizzati nascono e rimangono all'interno della blockchain stessa, come ad esempio accade per le transazioni ti token.
Tuttavia questo impone dei limiti importanti a molte implementazioni, in quanto non esiste alcuna funzionalità nativa per connettere la blockchain a fonti di dati provenienti dal mondo esterno. Qui entrano in gioco gli oracoli, cioè dei feed di dati che collegano le blockchain ad informazioni del mondo reale.
Gli oracoli sono particolarmente utili nella creazione di smart contract, in quanto, grazie ad essi, è possibile interrogare o eseguire un contratto al trigger di determinate condizioni all'esterno dell'ambiente in cui è sviluppato.
Un esempio di utilizzo potrebbe essere quello legato all'ambito assicurativo:
per l'attivazione della polizza è necessario che il cliente paghi, ovvero esegua una transazione verso lo smart contract, pari alla cifra prestabilita. Al verificarsi di un evento certificabile da un oracolo ed incontestabile, come ad esempio danni legati ad eventi climatici, il cliente che ha attivato la polizza riceverà una transazione a credito pari all'indennizzo previsto dal contratto.

Un oracolo può essere quindi visto come un ponte tra la blockchain e il mondo reale, che opera come un'API per la blockchain, che è possibile interrogare per ottenere informazioni da inserire negli Smart Contract.
Possono esistere svariati tipi di oracoli, tra cui: informazioni sui prezzi, meteo, scorrere del tempo, eventi sociali.

Nelle blockchain non è possibile utilizzare delle API tradizionali, su cui oggi si basa una notevole fetta del web, poiché queste potrebbero divenire obsolete, invalidando di fatto le funzionalità del contratto, potrebbero essere corruttibili, essendo sviluppate e mantenute generalmente da entità centralizzate.
Così è nata l'esigenza di creare gli oracoli, che spesso utilizzano sistemi di raccolta di una stessa informazioni disparati e ridondanti, così che il dato possa essere validato comparandolo da più fonti di provenienza.
Per ciò che riguarda la sicurezza degli oracoli possiamo qundi affermare che la sua affidabilità è pari a quella delle sue fonti di dati.
Al fine di evitare possibili manipolazioni sui dati è buona norma collezionarli da più fonti, implementando quello che viene chiamato un sistema di feed.

