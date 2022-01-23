# Blockchain
---
Created: 05 dicembre 2021 15:14
Tags: #tesi #blockchain 
Reference:
- [Blockchain Wikipedia](https://it.wikipedia.org/wiki/Blockchain)
- [Blockchain spiegata semplice](https://blog.osservatori.net/it_it/blockchain-spiegazione-significato-applicazioni)
- [Tesi Bitcoin e Blockchain #tesi](https://etd.adm.unipi.it/theses/available/etd-06012016-164829/unrestricted/Blockchain.pdf)
- [Tesi sicurezza bitocin](https://amslaurea.unibo.it/7934/1/bertani_beatrice_tesi.pdf)

---
## Cosa è una blockchain
La _**blockchain**_ (letteralmente "catena di blocchi") è una [struttura dati](https://it.wikipedia.org/wiki/Struttura_dati "Struttura dati") condivisa e "immutabile". È definita come un registro digitale le cui voci sono raggruppate in "blocchi", concatenati in ordine cronologico, e la cui integrità è garantita dall'uso della #crittografia.

![[blockchain structure image.png]]

Si basa sulla tecnologia chiamata [[Distributed Ledger]], ossia sistemi che si basano su un registro distribuito, che può essere letto e modificato da più nodi nella rete. Tra i nodi non ci deve essere fiducia reciproca poiché l'intero sistema è regolato da un protocollo condiviso, cioè per l'aggiunta di un nuovo blocco ogni nodo deve aggiornare la propria copia privata.

Le dimensioni di una blockchain sono in costante aumento, in quanto. viene sempre tenuta traccia di tutto lo storico della transazioni.

## Storia della blockchain
La prima blockchain è stata rilasciata nel 2008-2009 da [[Satoshi Nakamoto]], con lo scopo di implementare un "libro mastro" (registro di transazioni) della nascente valuta [[Bitcoin]].

Nel 2014 la blockchain di Bitcoin pesava circa 20 GB, nel 2021 siamo oltre i 300GB.

## Descrizione della blockchain
Una _blockchain_ è un registro digitale aperto e distribuito, in grado di memorizzare [record](https://it.wikipedia.org/wiki/Record_(tipo_di_dato) "Record (tipo di dato)") di dati (solitamente, denominati "transazioni") in modo sicuro, verificabile e permanente. Una volta scritti, i dati in un blocco non possono essere retroattivamente alterati senza che vengano modificati tutti i blocchi successivi ad esso.

La _blockchain_ è quindi rappresentabile come una **lista, in continua crescita, di "blocchi" collegati tra loro** e resi sicuri mediante l'uso della #crittografia.
Ogni blocco:
- Contiene una o più transazioni
- Un puntatore [[hash]] al blocco precedente
- Marca temporale #timestamp

Il sistema per come è costruito è robusto e sicuro, tuttavia i tempi di aggiornamento sono elevati, a causa del processo di validazione dei blocchi e della sincronizzazione della rete.

L'utilizzo di questa tecnologia consente anche di superare il problema dell'**infinita riproducibilità** di un bene digitale e della [doppia spesa](https://it.wikipedia.org/wiki/Doppia_spesa "Doppia spesa"), senza l'utilizzo di un server centrale o di un'autorità.

Se due nodi generano simultaneamente due blocchi concorrenti, collegati allo stesso blocco già esistente si ha un **fork** nella catena.
Il protocollo di aggiornamento specifica la regola che i nodi devono usare per selezionare un solo blocco. Il blocco scartato viene detto **blocco orfano**.

## Decentramento della blockchain
L'intero sistema blockchain è decentralizzato, quindi non esiste un **single point of failure**.

Tra i metodi di [[Sicurezza della blockchain]] c'è la [[Crittografica a chiave pubblica]].
Nella blockchain:
- Chiave pubblica == indirizzo sulla blockchain
- Chiave privata == password per accedere al proprio wallet e interagire con la blockchain

I dati salvati in blockchain sono **incorruttibili**.

Ogni _nodo_ o _miner_ nel sistema decentrato ha una copia della _blockchain_: difatti la qualità dei dati è mantenuta grazie a una **massiva replicazione del database**. Non esiste nessuna copia ufficiale centralizzata e nessun utente è più credibile di altri, tutti sono allo stesso livello di credenziali. I nodi _miner_, ovvero gli utenti, validano le nuove transazioni e le aggiungono al blocco che stanno costruendo dopo aver verificato l'intera _blockchain_. Una volta completato il blocco, lo trasmettono agli altri nodi della rete.

La _blockchain_ usa differenti schemi di _[timestamp](https://it.wikipedia.org/wiki/Timestamp "Timestamp")_ per serializzare le modifiche.

Al crescere della blockchain si rischia la centralizzazione della stessa, poiché le risorse richieste per operare e gestire i dati sono sempre più costose e gli utenti standard non riescono a stare dietro alle _pool_ di miners.

## Come è strutturato un blocco di una blockchain
Le transazioni sono raggruppate nei blocchi della _blockchain_ e il numero di transazioni all'interno di ognuno di questi blocchi varia in base alla dimensione della transazione stessa. 
Un blocco è composto da due parti principali: l'**header** e il **body**. Le transazioni sono racchiuse nel _body_ del blocco e nell'_header_ sono presenti sette campi di gestione del blocco stesso.
### Header del blocco
| Elemento header       | Descrizione                                                                                                                                                                                                                                                          |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Versione              | versione software utilizzato                                                                                                                                                                                                                                         |
| PrevHash              | _hash_ di 256 bit che serve per fare riferimento al precedente blocco della catena                                                                                                                                                                                   |
| Merkle Root           | _hash_ di tutti gli _hash_ di tutte le transazioni nel blocco                                                                                                                                                                                                        |
| Timestamp             | rappresenta il _time stamp_ dell'ultima transazione con un algoritmo conosciuto come _Unix hex timestamp_ da non confondere con il _timestamp UNIX_ che esprime bit numerici in secondi dal 1970-01-01T 00:00 UTC                                                    |
| Bits                  | rappresenta il corrente valore _target_: l'_hash_ dello SHA-256 dell'_header_ di un blocco dev'essere minore o al massimo uguale al corrente valore di _target_ per essere accettato dalla rete                                                                      |
| Nounce                | valore a 8 byte che viene aggiunto al blocco in modo che l'output della funzione di _hash_ vari facendo in modo che risulti inferiore al valore _target_, il valore viene ricalcolato finché l'_hash_ del blocco non contiene il richiesto numero di zeri principali |
| Numero di transazione | identifica il numero della transazione                                                                                                                                                                                                                               |

### Validazione dei blocchi -> Mining
Un nodo, dopo aver verificato l'intera _blockchain_, raccoglie e colleziona le nuove transazioni generate ancora non validate e suggerisce alla rete quale dovrebbe essere il nuovo blocco. 
I computer usano la funzione crittografica di _hash_ per stimare l'output fino a che non risulta inferiore al valore di _target_ (valore dato dal campo "bits" nell'_header_ del blocco). Il primo nodo che risolve il blocco lo trasmette nella rete dove viene accettato come blocco successivo nella catena.

Siano:
- H la funzione di hash imposta dalla rete
- x le transazioni pendenti
- n il valore di nounce

L'**hash di output** deve iniziare con degli zeri e deve essere inferiore al valore di target.
Il problema è determinare il valore di nounce per far si che la condizione sopra sia rispettata.
La variazione di un bit genera hash output totalmente differenti, quindi è impossibile predire il valore di nounce.

Una volta che il blocco è risolto il suo **hash è come un'impronta digitale**, lo rappresenta univocamente.
Alla risoluzione del blocco la rete aggiusta automaticamente il valore di _target_.

L'intero processo di validazione è chiamato **mining**.

### Blockchain open e proprietarie
Le prime blockchain erano tutte open, mentre alcune più recenti sono proprietarie, cioè i nodi devono essere autorizzati da un'autorità centrale. Un dibattito verte sul poter considerare tali sistemi blockchain oppure no.

**Open blockchain**
In questo caso non è necessaria alcuna autenticazione ed è possibile aggiungere applicazioni alla rete senza alcuna approvazione, usando la blockchian come **livello di trasporto**.
La sicurezza di queste blockchain è data dalla [[proof of work]]. ^29b73d

**Private blockchain**
Le _blockchain_ con permessi (o _permissioned_) usano un _layer_ di controllo degli accessi per controllare chi accede alla rete. Sono quindi caratterizzate da un accesso alla rete ristretto ad alcuni partecipanti autorizzati e da un processo di validazione demandato a un gruppo ristretto di attori.
Le _blockchain_ private si dividono essenzialmente in due tipologie: i _Consortium Blockchain_ e i _Fully Private Blockchain_.

## [[Meccanismi di consenso]]
[Ethereum consensum](https://ethereum.org/it/developers/docs/consensus-mechanisms/)


## Applicazioni della blockchain
L'uso della _blockchain_ promette di portare significativi miglioramenti alle catene di fornitura globali, alle transazioni finanziarie, ai beni contabili e ai _social network_ distribuiti.

La _blockchain_ può essere utilizzata come strumento per **certificare la data certa di un documento e il suo non aver subito alcuna variazione**. Questa applicazione della catena a blocchi, ottenuta inserendo l'_hash_ dei documenti che si vogliono certificare, è detta notarizzazione.

Sono state anche sviluppate diverse _blockchain_ per l'archiviazione di dati, pubblicazione di testi e identificazione delle origini dell'[arte digitale](https://it.wikipedia.org/wiki/Arte_digitale "Arte digitale").

La principale implementazione dei sistemi blockchain è quella riguardante il mondo delle [[Criptovalute]]
[[Applicazioni di blockchain]]

### [[Smart Contract]]
Gli **smart contract** basati sulla _blockchain_ sono contratti che possono essere stipulati e imposti senza la necessità di un'interazione umana. L'[FMI](https://it.wikipedia.org/wiki/Fondo_monetario_internazionale "Fondo monetario internazionale") crede che la _blockchain_ potrebbe ridurre il _rischio morale_ e ottimizzare l'uso dei contratti in generale ma, momentaneamente, a causa della mancanza d'uso, il loro _status_ non è ancora chiaro.

Alcune implementazioni della _blockchain_ potrebbero consentire la codifica di contratti che verranno eseguiti quando sono soddisfatte determinate condizioni. Vedi [[Solidity]]

## [[Glossario blockchain]]
![[Glossario-Blockchain.pdf]]

## Tool e piattaforme per sviluppo blockchain
- [[Cosmos]]: Strumenti per creare blockchain
- [[Truffle Suite]]: Strumenti per smart contracts
- [Consensys - Infura](https://consensys.net/products/#infura)