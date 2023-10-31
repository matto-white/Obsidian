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
### Crittografia asimmetrica
La chiave di cifratura è diversa da quella di decifratura
2 chiavi: 1 pubblica e 1 privata

Es 1) Voglio garantire la riservatezza e l'integrità
chiave pubblica -> file originale --> file criptato ->-> file criptato -> chiave privata -> file originale

Es 2) Modalità autenticazione
chiave privata -> file originale -> file criptato ->-> file criptato -> chiave pubblica -> file originale