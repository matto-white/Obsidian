# #TCP

[TCP.pdf](../_resources/TCP.pdf)

- ### Connection Oriented
    
- ### Affidabile
    
- ### Full Duplex
    
- ### Point to Point
    

Formato del segmento TCP: Header + Dati

### Header:

![[TCP Header.png]]

##### Ackhowledfement number (Numero di riscontro):
ha significato solo se il flag ack è impostato a 1.
conferma la ricezione

##### Header Lenght:
Indica la lunghezza dell'header del segmento TCP in word da 32bit

##### Syn:
Usato nella fase di instaurazione di una connessione se impostato a 1, significa che l'host mittente del segmento vuole aprire una connessione.

##### Fin:
Se imposato a 1 significa che l'host mittente non ha più dati da inviare e vuole chiudere la connessione.

##### Window size:
è usato dall'host ricevente per dire al mittente quanti dati può ricevere in quel momento (finestra di ricezione)

## Le fasi di una connessione TCP:

1.  Instaurazione (set-up) della connessione TCP: Avviene il colloquio iniziale tra mittente e destinatario
2.  Trasferimento dati: Avviene il traferimento dei dati. Poichè il TCP offre un meccanismo affidabile si attua una serie di meccanismi per il controllo.
3.  Abbattimento della connessione TCP: Disconnessione

Handshake a 3 vie:

![[Handshake.png]]

1) Syn.f = 1; Seq.n = x
2) Ack.f = 1; Ack.n = x+1; Syn.f = 1; Seq.n = y
3) Ack.f = 1; Ack.n = y+1


## Fase di trasferimento dati
![[_resources/tcp_data_transfer 1.png | 700]]

- Ogni volta che il ricevente invia un ACK, indica nel campo window size il numero di byte che può ricevere in quel momento.
- Il mittente non invia un numero di byte superiore a quello indicato nell'ultimo ACK
TCP:
	- il ricevente non può rifiutare di accettare il numero di byte che aveva indicato nella finestra
	- Assicura che i dati siano consegnati nella giusta sequenza
	- Attua un controllo di flusso (grazie al window size)
	- Nota Bene: Il tcp prevede un timeout di 3 secondi che evita l'attesa infinita del riscontro al segmento inviato