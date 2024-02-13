do lnterface gi0/1# Firewall
Separa la LAN aziendale dalla WAN pubblica.
Filtra tutti i pacchetti entranti e uscenti da e verso una rete secondo regole prestabilite (Policy)
Un firewall può essere realizzato con 1 pc (con almeno due schede di rete) e il software opportuno
Nelle LAN aziendali viene realizzato attraverso un software incluso nel router oppure può essere implementato su un apparato hardware specifico

3 categorie:
- application level firewall
- packet filter firewall
- stateful packet inspection firewall

# ACL
## ACL Standard
Hanno numero da 1 a 99 e da 1300 a 1999
Filtra in base all'ip sorgente
## ACL Estese
hanno numero da 100 a 199 e da 2000 a 2699
Controllano l'ip e possono indicare anche protocolli L4-L7
Filtrano in base all'ip sorgente, destinazione, porta sorgente e porta destinazione

Sintassi acl router: ..# access-list numero {permit | deny} ip-sorgente \[wildcard mask]

## Wildcard Mask
32bit stabilisce se i bit dell'indirizzo il devono essere controllati o no

Es. voglio controllare l'indirizzo ip 169.12.5.0/24

voglio bloccare il traffico in arrivo dai seguenti indirizzi ip: da 169.12.5.4 fino a 169.12.5.7

.4    00000100
.5    00000101
.6    00000110
.7    00000111
00000011 = 0.0.0.3

# DMZ
(Demilitarized Zone)
La DMZ contiene ed espone dei servizi ad una rete ritenuta non sicura.
Lo scopo di una DMZ è proteggere la rete

# VPN
Esistono 2 tipi:
## 1) Remote access VPN
porta qualsiasi applicazione (Dati, voce, video...) al desktop remoto, emulando il desktop dell'ufficio principale
Consente ai singoli utenti di stabilire connessioni sicure con la lan aziendale remota. Sfrutta un sistema di autentificazione interno oppure un servizio esterno come un AAA (Authentication Authorization Accounting) server
![[Progettazione Reti Sicure 2024-02-12 12.01.45.excalidraw]]
### N.B. 2 componenti indispensabili
1) Server di accesso alla rete => NAS (Network Access Server). 
## 2) Site to site VPN
l'artenativa alle WAN. Consente alle aziende di ampliare le risorse di rete alle filiali
![[Progettazione Reti Sicure 2024-02-12 12.27.12.excalidraw]]
# IPsec
IPsec non è un singolo protocollo ma un architettura di sicurezza a livello network