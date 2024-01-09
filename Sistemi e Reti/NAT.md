Network Address Translation

Provvede alla mappatura degli indirizzi IP privati in una coppia costituita dall'indirizzo pubblico e dal numero porta

Il router costruisce la NAT table, che è una tabella di tracciamento delle connessioni

NAT Table
![[NAT 2024-01-09 08.33.28.excalidraw|50%]]

1)
S: 10.0.0.1:3335
D: 128.5.7.4:80

2)
S: 138.29.7.4:5000
D: 128.5.7.4:80

3)
S: 128.5.7.4:80
D: 138.29.7.4:5000

4)
S: 138.29.7.4:80
D: 10.0.0.1:3335