[[Informatica per Istituti Tecnici Tecnologici - Indirizzo Informatica e Telecomunicazioni - Volume C (atlas-91705) (1).pdf]]
In generale un archivio è un insieme organizzato di informazioni caratterizzate da alcune
proprietà fondamentali:
• tra esse esiste un nesso logico (cioè sono in qualche modo inerenti ad un medesimo
argomento);
• sono rappresentate secondo un formato che ne rende possibile l’interpretazione;
• sono registrate con un supporto su cui è possibile scrivere e rileggere informazioni anche
a distanza di tempo.
• sono organizzate in modo che siano facilmente consultabili.

Questi insiemi di informazioni logicamente organizzate e riferite a un unico soggetto sono
chiamati con il termine record (che in italiano significa registrazione); le singole informazioni che
compongono il record si chiamano campi; l’elenco dei campi che lo compongono viene detto
tracciato del record.

Un file è una collezione di record, cioè di informazioni logicamente omogenee, che descrivono le istanze di una entità. Ogni record è composto da un insieme di campi che contengono i valori assunti dalle caratteristiche scelte per descrivere le entità.

Dopo aver creato l’archivio, su di esso si possono effettuare operazioni di:
• manipolazione, cioè inserimento di nuovi dati o variazione dei dati registrati;
• interrogazione, cioè reperimento all’interno dell’archivio delle informazioni necessarie.

Il modulo del software di base che svolge le funzioni di gestore dei file viene chiamato file
system. Esso è costituito dall’insieme delle routine del sistema operativo che consentono
all’utente-programmatore di usufruire degli archivi sulle memorie di massa, senza preoccu-
parsi dei dettagli delle operazioni di input/output (I/O) e facendo riferimento ai file solo con
nomi simbolici.

Infatti il file system regola l’organizzazione, l’assegnamento, la protezione e il ritrovamento di
insiemi di dati, cioè di file. In particolare esso svolge le seguenti funzioni:
• tiene traccia dei file, della loro posizione, del loro stato, usando particolari strutture dati dette
file directory;
• decide secondo le richieste, le protezioni e i diritti di accesso (per esempio, lettura e scrittura,
solo lettura) a quale programma assegnare un file o una parte di esso;
• assegna, cioè rende disponibile, un file al programma che lo ha richiesto;
• toglie l’uso di un file a un programma rendendolo disponibile ad altri programmi.

Organizzazione Sequenziale: consiste nel registrare
i record uno di seguito all’altro, in modo sequenziale,
intervallati da sequenze di caratteri che indicano la
fine del record (EOR, End Of Record). Consente
l’uso di record a lunghezza variabile.

In un archivio ad organizzazione diretta, i
record sono identificati dalla posizione nel file.
Volendo accedere a un dato record occorre
specificare, con un valore numerico, la sua
posizione in ogni operazione di lettura.

il database è una collezione di archivi di dati ben organizzati e ben strutturati, che sono
gestiti in modo integrato e che costituiscono una base di lavoro per utenti diversi con
programmi diversi. I prodotti software per la gestione dei database sono indicati con il
termine DBMS, acronimo di DataBase Management System.

![[Pasted image 20240116142633.png]]

Il database è una collezione di dati logicamente correlati e condivisi, che ha lo scopo di
soddisfare i fabbisogni informativi di una specifica organizzazione. I dati, congiuntamente
con la loro descrizione, sono gestiti da un unico sistema, chiamato DBMS (DataBase Management System), che ne permette la gestione e ne regola gli accessi.

Un DBMS deve essere in grado di:
• Permettere la creazione di una nuova base di dati, definendo gli archivi che la compongono, la loro
articolazione, le correlazioni logiche tra archivi, i limiti nell’accesso ai dati e i vincoli imposti alla loro
manipolazione. La creazione della base dati avviene mediante un apposito linguaggio che prende
il nome di linguaggio di definizione dei dati, ovvero DDL (Data Definition Language).
• Facilitare gli utenti nell’inserimento, nella cancellazione e variazione dei dati nel database
sfruttando uno specifico linguaggio che prende il nome di linguaggio di manipolazione dei
dati, DML (Data Manipulation Language).
• Rendere possibile l’estrazione di informazioni dal database interrogando la base dati mediante
un apposito linguaggio di interrogazione, QL (Query Language).
• Effettuare le precedenti operazioni tramite un linguaggio semplice da apprendere e standar-
dizzato in modo che l’utente possa agevolmente passare da un DBMS a un altro.

![[Pasted image 20240116142819.png]]

La descrizione dei dati è formata dai metadati, cioè dati che descrivono i dati, e prende il
nome di dizionario dei dati o anche catalogo dei dati (in inglese, data dictionary).
Il fatto che la descrizione dei dati che compongono il database sia conservata all’interno dello stesso
database e non nei programmi applicativi garantisce l’indipendenza logica dei programmi dai dati.
Il DBMS attingendo alle informazioni memorizzate nel dizionario dei dati è anche in grado di:
• realizzare i controlli per garantire l’integrità dei dati,
• autorizzare gli utenti in base alle politiche definite per l’accesso ai dati,
• fornire servizi per il controllo della consistenza.

Per descrivere i dati, il loro significato, come sono correlati e i vincoli definiti su di essi si fa uso
di modelli dei dati. Essi sono classificabili secondo diversi livelli di generalità.
Il livello più generale è noto come modello concettuale (o modello a livello di oggetti), seguito
dal modello logico dei dati (o modello a livello di record) e infine, al livello più basso, si trova
il modello fisico dei dati, che si occupa delle modalità e delle tecniche usate nella registrazione
sulle memorie di massa.

Tra i numerosi modelli proposti per la progettazione concettuale, i più noti sono il modello
orientato agli oggetti e il modello Entità/Associazioni. Il modello Entità/Associazioni, indicato
come modello E/R dal termine inglese Entity/Relationship, è il modello adottato in questo testo
per la progettazione concettuale e sarà sviluppato nel Capitolo 2, mentre il modello orientato agli
oggetti è presentato nei Contenuti digitali integrativi.
Nella costruzione del modello E/R di una realtà si individuano gli oggetti che la compongono
dette entità, gli attributi, che rappresentano le caratteristiche delle entità individuate, e infine
le associazioni che individuano le correlazioni logiche tra entità. Entità, attributi, associazioni
sono rappresentate graficamente in un diagramma E/R.

A partire dallo schema concettuale Entità/Associazioni, un database può essere progettato e
realizzato passando al modello logico, cioè alle strutture di dati che organizzano i dati, in modo
da consentire le operazioni di manipolazione e di interrogazione.
Nello sviluppo della teoria dei database, dagli anni ’60 in poi, sono emersi tre diversi tipi di
modelli a livello di record per le basi di dati: il modello gerarchico, il modello reticolare e il modello
relazionale.

Il modello relazionale rappresenta il database come un insieme di tabelle. Esso viene
considerato attualmente il modello più semplice ed efficace, perché è più vicino al modo
consueto di pensare i dati, e si adatta in modo naturale alla classificazione e alla strutturazione
dei dati.

Il modello relazionale è un modello basato sui valori. Le associazioni tra entità sono descritte
solamente tramite i valori assunti da campi, nelle righe delle tabelle che modellano le entità
stesse, senza fare uso di puntatori.

Il modello fisico dei dati ha la funzione di descrivere il modo con il quale un dato modello logico
è mappato sulle memorie di massa del computer. Nel caso del modello relazionale, il modello
fisico precisa come sono realizzate le tabelle, il modo per implementare i vincoli sui dati che le
compongono, come rappresentare le associazioni tra tabelle, come costruire gli indici sui campi
di una tabella e così via.

I moderni DBMS seguono, di fatto, l’impostazione concettuale dell’architettura a tre livelli
ANSI/SPARC, proposta nel 1975 da un comitato (Standard Planning And Requirements Committee)
dell’ANSI (American National Standards Institute). Secondo questa impostazione i dati sono
descritti secondo tre differenti livelli di astrazione, mediante opportuni schemi. I tre livelli sono
indicati come il livello esterno, il livello logico e il livello interno.

![[Pasted image 20240117103102.png]]

L’architettura a tre livelli dei database realizza meccanismi di astrazione dei dati e assicura
l’indipendenza dei dati. Con questo termine si vuole indicare che i livelli superiori non sono
influenzati, entro certi limiti, dai cambiamenti che avvengono nei livelli inferiori dell’architet-
tura dei dati. Si identificano due livelli di indipendenza dei dati: l’indipendenza logica e
l’indipendenza fisica.

Il DBMS (DataBase Management System) è il software che consente di costruire e gestire una
base di dati, realizzandola nella pratica su memoria di massa, a partire da un progetto e da
uno schema dei dati definiti a livello concettuale e tradotto poi in un modello logico dei dati.
Il DBMS costituisce quindi un’interfaccia tra gli utenti di un database con le loro applicazioni
e le risorse costituite dall’hardware e dagli archivi di dati presenti in un sistema di elaborazione.

![[Pasted image 20240117103611.png]]

Una transazione consiste in un insieme di operazioni di interrogazione o di modifica del
database che devono essere eseguite unitariamente come se fossero un’unica operazione.

![[Pasted image 20240117103738.png]]

