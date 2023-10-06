DNS:
	Risoluzione degli indirizzi IP in nomi host
Database di tipo gerarchico con una struttura ad albero che rappresenta tutti domini che costituiscono lo spazio dei nomi su internet

In cima all'albero c'è il dominio radice (root)

Il DNS ha queste 3 componenti:
1) Domain Name Space: Specifica la struttura ad albero dei nomi di dominio
2) Name Server: è un processo applicativo che contiene informazioni sullo spazio dei nomi 
3) Resolver (Client)

Come funziona:
1) il client DNS fa una richiesta (DNS Request)
2) il server risponde con un messaggio che si chiama DNS reply

Resource record: ogni dominio è associato a un insieme di resource record, che sono usati dai DNS per mappare i nomi di dominio sugli indirizzi ip
![[Nomi di dominio e DNS 2023-10-06 09.18.13.excalidraw|20%]]

![[Nomi di dominio e DNS 2023-10-06 09.22.02.excalidraw]]

Esempi di resource record
pingu.di.school.it 86400 IN A 198.45.30.165

IN = internet
A = address IPv4

Esempio 2:
www.di.school.it ... IN CNAME pingu.di.school.it

CNAME = mi permette di definire gli alias
definisce www.di.school.it come un alias di un host il cui nome canonico è pingu.di.school.it. Quindi se in futuro all'host pingu gli viene associato lix