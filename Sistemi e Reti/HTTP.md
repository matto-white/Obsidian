è un protocollo stateless che regola lo scambio di messaggi tra il web server e il web client. è un protocollo basato sul modello client server

HTTP identifica le risorse del web mediante un indirizzo simbolico (URL(Uniform Resource Locator))

esempio di URL-> http://www.azienda.com/news/...
http -> indica il protocollo
www -> individua il nome di una specifica macchina

## Metodi HTTP
Dalla versione 1.0
Get -> richiede una risorsa al server
Head -> Richiede solo l'header, non la risorsa
Post -> invia informazioni al server

Versioni successive
Delete
Options
Trace
Connect

## Messaggi HTTP
2 tipi di messaggi:
	Http request
	Http response

### HTTP request
composto da 3 parti:
	Riga di richiesta
	Sezione header
	Body
### HTTP response
composto da 3 parti:
	Riga di stato
	Sezione header
	Body

1) Riga di stato contiene un codice a 3 cifre
	200 Ok
	404 Not found
	400 Wrong request
	500 Internal server error