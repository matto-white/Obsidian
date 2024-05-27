![](Societ%C3%A0%20Aeroportuale%202024-05-23%2016.37.22.excalidraw.svg)
%%[🖋 Edit in Excalidraw](Societ%C3%A0%20Aeroportuale%202024-05-23%2016.37.22.excalidraw.md)%%


**Citta**(**ID**)
**Aeroporto**(**ID**, Luogo, Quantita_Piste, *CittaID*)
**Passeggero**(**N_Doc**, Nome, Cognome, Nazionalita, Motivo, Bagaglio_a_mano, Stato)
**Aer_passeggero**(N.Doc, ID)
**Controllo**(**ID**, Data_Inizio, Ora_Inizio, Ora_Fine, EsitoID, Dazio, Passeggero_N_Doc, AddettoID, *Punto_di_Controllo_ID*, Funzionario_ID)
**Addetto**(**ID**, Nome, Cognome)
**Punto_di_Controllo**(**ID**, *Controllo_ID*)
**Funzionario**(**ID**, Nome, Cognome)
**Merce**(**ID**, CategoriaID, Descrizione, Quantita, Ritirata, *Controllo_ID*, Categoria_ID)
**Categoria**(**ID**, Nome, Descrizione)
**Esito**(**ID**, Nome, Descrizione, *Controllo_ID*)





1) visualizzare i dati di tutti i passeggeri che sono stati controllati in ciascuno dei punti di  dogana nell’arco della giornata
```SQL
SELECT *
FROM Passeggero
WHERE Passeggero.N_Doc IN (
    SELECT Controllo.Passeggero_N_Doc
    FROM Controllo
    WHERE DATE(Data_Inizio) = CURDATE()
)
ORDER BY Controllo.Punto_di_Controllo_ID;

```
2) visualizzare per ciascun punto di controllo l’ammontare dei dazi doganali registrati
```SQL
SELECT Controllo.Punto_di_Controllo_ID, SUM(Controllo.Dazio) AS Ammontare_Dazi
FROM Controllo
GROUP BY Controllo.Punto_di_Controllo_ID;

```
3) calcolare e visualizzare quante merci per ogni categoria sono state respinte dall’inizio  dell’anno
```SQL
SELECT Categoria.Nome AS Categoria, COUNT(*) AS Quantita_Respinte
FROM Merce
JOIN Categoria ON Merce.Categoria_ID = Categoria.ID
WHERE Merce.Ritirata = TRUE
AND YEAR(Merce.Data_Registrazione) = YEAR(CURDATE())
GROUP BY Categoria.Nome;

```
4) calcolare e visualizzare quante contestazioni sono state registrate da ciascun addetto
```SQL
SELECT Addetto.ID, Addetto.Nome, Addetto.Cognome, COUNT(*) AS Numero_Contestazioni
FROM Addetto
JOIN Controllo ON Addetto.ID = Controllo.AddettoID
WHERE Controllo.EsitoID IS NOT NULL
GROUP BY Addetto.ID, Addetto.Nome, Addetto.Cognome;

```
5) calcolare la durata media dei controlli per ogni punto di controllo nell’arco della giornata
```SQL
SELECT Controllo.Punto_di_Controllo_ID, AVG(TIMESTAMPDIFF(MINUTE, Controllo.Ora_Inizio, Controllo.Ora_Fine)) AS Durata_Media_Controllo
FROM Controllo
WHERE Controllo.Ora_Fine IS NOT NULL
GROUP BY Controllo.Punto_di_Controllo_ID;

```
6) visualizzare l’elenco, in ordine alfabetico, raggruppato per nazionalità, dei passeggeri in  stato di fermo, registrati dall’inizio dell’anno in tutti i punti di controllo
```SQL
SELECT Passeggero.Nazionalita, Passeggero.Nome, Passeggero.Cognome
FROM Passeggero
JOIN Controllo ON Passeggero.N_Doc = Controllo.Passeggero_N_Doc
WHERE Passeggero.Stato = 'Fermo'
AND YEAR(Controllo.Data_Inizio) = YEAR(CURDATE())
ORDER BY Passeggero.Nazionalita, Passeggero.Nome, Passeggero.Cognome;

```
7) visualizzare gli addetti in servizio nella giornata, suddivisi per nome del funzionario  incaricato
```SQL
SELECT Funzionario.Nome AS Nome_Funzionario, Addetto.Nome AS Nome_Addetto, Addetto.Cognome AS Cognome_Addetto
FROM Funzionario
JOIN Addetto ON Funzionario.ID = Addetto.Funzionario_ID
JOIN Controllo ON Addetto.ID = Controllo.AddettoID
WHERE DATE(Controllo.Data_Inizio) = CURDATE()
GROUP BY Funzionario.Nome, Addetto.Nome, Addetto.Cognome;

```