![](attachments/Autori%202024-05-09%2010.25.20.excalidraw.svg)
%%[🖋 Edit in Excalidraw](attachments/Autori%202024-05-09%2010.25.20.excalidraw.md)%%



SQL rispetto db luca
1)
```SQL
SELECT Canzone.* FROM Canzone
WHERE Canzone.anno >= 1970 AND Canzone.anno <= 1980;
```

2)
```SQL
SELECT Canzone.* FROM Canzone
WHERE Canzone.mood = "upfeeling" AND Canzone.ID_Autori = IS NOT NULL
JOIN Scrive ON Canzone.ISRC = Scrive.ISRC;
```
3)
```SQL
SELECT COUNT(*) FROM Compone
WHERE Compone.genere = "dance"
JOIN Canzone ON Compone.ISRC = Canzone.ISRC;
```
4)
```SQL
SELECT Canzone.genere, COUNT(*)
FROM Canzone
GROUP BY Canzone.genere;
```
5)
```SQL

```
