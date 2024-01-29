# Firewall
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
Controllano solo l'ip sorgente
## ACL Estese
hanno numero da 100 a 199 e da 2000 a 2699
Controllano l'ip e possono indicare anche protocolli L4-L7

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