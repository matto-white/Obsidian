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

