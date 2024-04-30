# Logico
Studente (==CodiceStud==, CognStud, NomeStud, DataNascita, Classe, *CodiceIstituto*);
Manifestazione (==CodiceManif==, Descrizione, Luogo, DataInizio);
Stud&Manif (==CodiceStud==, ==CodiceManif==);
Istituto (==CodiceIstituto==, Denominazione, Indirizzo, Telefono);
Professore (==CodiceProf==, CognProf, NomeProf, *CodiceIstituto*, *CodiceManif*);

# Query

1) Numero degli studenti che partecipano a una determinata manifestazione sportiva
```sql
SELECT COUNT(*)
FROM Studente
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud
WHERE Stud&Manif.CodiceManif = codice_manifestazione;
```

2) Elenco alfabetico degli allenatori di un’attività o manifestazione sportiva
```sql
SELECT CognProf, NomeProf
FROM Professore
WHERE CodiceManif = codice_manifestazione
ORDER BY CognProf, NomeProf;
```

3) Elenco delle scuole (denominazione) con il numero di studenti che partecipano alle attività sportive
```sql
SELECT Istituto.Denominazione, COUNT(Studente.CodiceStud)
FROM Istituto
JOIN Studente ON Istituto.CodiceIstituto = Studente.CodiceIstituto
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud
GROUP BY Istituto.Denominazione;
```

4) Elenco delle scuole (con denominazione, indirizzo, telefono) con studenti che partecipano a una determinata manifestazione sportiva
```sql
SELECT Istituto.Denominazione, Istituto.Indirizzo, Istituto.Telefono
FROM Istituto
JOIN Studente ON Istituto.CodiceIstituto = Studente.CodiceIstituto
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud
WHERE Stud&Manif.CodiceManif = codice_istituto;
```

5) Elenco alfabetico dei professori (cognome e nome) e scuole (denominazione) di appartenenza
```sql
SELECT CognProf, NomeProf, Istituto.Denominazione
FROM Professore
JOIN Istituto ON Professore.CodiceIstituto = Istituto.CodiceIstituto;
```

6) Numero degli studenti partecipanti di una determinata scuola per ciascuna delle manifestazioni sportive
```sql
SELECT Istituto.Denominazione, COUNT(Studente.CodiceStud)
FROM Istituto
JOIN Studente ON Istituto.CodiceIstituto = Studente.CodiceIstituto
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud
WHERE Istituto.CodiceIstituto = codice_istituto
GROUP BY Istituto.Denominazione, Stud&Manif.CodiceManif;
```

