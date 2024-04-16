# Logico
Studente (==CodiceStud==, CognStud, NomeStud, DataNascita, Classe, *CodiceIstituto*)
Manifestazione (==CodiceManif==, Descrizione, Luogo, DataInizio)
Stud&Manif (==CodiceStud==, ==CodiceManif==)
Istituto (==CodiceIstituto==, Denominazione, Indirizzo, Telefono)
Professore (==CodiceProf==, CognProf, NomeProf, *CodiceIstituto*, *CodiceManif*)

# Query
1) 
```sql
SELECT COUNT(*) 
FROM Studente 
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud 
WHERE Stud&Manif.CodiceManif = codice_manifestazione
```

```sql
SELECT CognProf, NomeProf 
FROM Professore 
WHERE CodiceManif = codice_manifestazione
ORDER BY CognProf, NomeProf;
```

```sql
SELECT Istituto.Denominazione, COUNT(Studente.CodiceStud) 
FROM Istituto 
JOIN Studente ON Istituto.CodiceIstituto = Studente.CodiceIstituto  
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud 
GROUP BY Istituto.Denominazione;
```

```sql
SELECT Istituto.Denominazione, Istituto.Indirizzo, Istituto.Telefono 
FROM Istituto 
JOIN Studente ON Istituto.CodiceIstituto = Studente.CodiceIstituto 
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud 
WHERE Stud&Manif.CodiceManif = [desired manifestation
```

```sql
SELECT CognProf, NomeProf, Istituto.Denominazione 
FROM Professore 
JOIN Istituto ON Professore.CodiceIstituto = Istituto.CodiceIstituto;
```

```sql
SELECT Istituto.Denominazione, COUNT(Studente.CodiceStud) 
FROM Istituto 
JOIN Studente ON Istituto.CodiceIstituto = Studente.CodiceIstituto 
JOIN Stud&Manif ON Studente.CodiceStud = Stud&Manif.CodiceStud 
WHERE Istituto.CodiceIstituto = [desired school ID] 
GROUP BY Istituto.Denominazione, Stud&Manif.CodiceManif;
```

