La cifratura e la decifratura sono tipicamente algoritmi fissi e pubblici

N.B. principio di Kerchoffs - Shannon:
Il nemico prima o poi conoscerà il tuo sistema;

crittografia -> arte di camuffare un messaggio...
crittoanalisi -> arte di infrangere i sistemi crittografici
cifrario -> corrispondenza tra i simboli del messaggio in chiaro

Testo in chiaro -> plaintext
Testo cifrato -> cipherext

### Crittografia simmetrica:
La chiave di cifratura coincide con quella di decifratura

- Codici a sostituzione
- Codici a trasposizione

#### Cifrari a sostituzione
ogni unità del testo in chiaro è sostituita dal testo cifrato secondo uno schema regolare

##### Cifrario di cesare:
È un cifrario a sostituzione
Sineddoche       k=3
    |
   V
V...

#### Cifrari a trasposizione
Le posizioni occupate dalle unità di testo in chiaro sono cambiate secondo un determinato schema, cioè il testo cifrato costituisce una permutazione del testo in chiaro

"Viva la sineddoche per sempre"

		pesca
		vival
		asine
		ddoch
		epers
		empre

chiave: pesca


#### Cifrari mono alfabetici
su utilizza un alfabeto per il testo in chiaro e una permutazione dello stesso alfabeto per il testo cifrato

#### Cifrari poli alfabetici
se alterna più alfabeti cifranti che sono permutazioni dell'alfabeto in chiaro
#### Cifrari Moderni
##### Cifrario DES (Violato)
Il testo in chiaro viene diviso in blocchi di 8 Byte

Testo in chiaro (64bit) -> Trasposizione iniziale -> (Iterazione 1) -> Nuova stringa -> ... (Iterazione 16) -> Trasposizione inversa -> Testo cifrato

Iterazione=Funzione cifrante di sostituzione dei bit usando due porzioni della chiave da 28
##### Cirario 3-DES
Uguale al DES ma più lungo
##### Cifrario AES
Cifrario a blocchi
Chiave a 128 bit

Si crea una matrice 4x4 (16 Byte / 16 caratteri (8bit) = 128bit)

codifica -> 10 fasi (Rounds) ciascuna composta da 4 trasformazioni (nel caso di chiave a 128 bit)
1) Substitute bytes -> ogni Byte con una permutazione
2) Shift rows
3) Mix colums (si prende una colonna, si moltiplica per un polinomio) -> nuova tabella con le colonne mischiate
4) Add Round key -> viene inserita la chiave che rende il cifrario sicuro -> ogni Byte viene combinato in XOR con la chiave
5) Ricomincia da 1 ancora 9 volte. A ogni round la chiave aggiunta muta secondo un calcolo mtematico
### Crittografia asimmetrica
La chiave di cifratura è diversa da quella di decifratura
2 chiavi: 1 pubblica e 1 privata

Es 1) Voglio garantire la riservatezza e l'integrità
chiave pubblica -> file originale --> file criptato ->-> file criptato -> chiave privata -> file originale

Es 2) Modalità autenticazione
chiave privata -> file originale -> file criptato ->-> file criptato -> chiave pubblica -> file originale

#### RSA
Utilizzo: 
1) Si può utilizzare per inviare una chiave segreta
2) Per la cifratura di firme digitali

Funzionamento di RSA
1) A deve spedire un messaggio segreto a B
2) B sceglie due numeri primi molto grandi e li moltiplica tra loro
3) B invia ad A in chiaro il numero ottenuto
4) A usa questo numero per crittografare il messaggio
5) A manda il messaggio a B
6) B riceve il messaggio e utilizzando i due fattori primi (che solo lui conosce) decifra il messaggio