![](Societ%C3%A0%20Aeroportuale%202024-05-23%2016.37.22.excalidraw.svg)
%%[🖋 Edit in Excalidraw](Societ%C3%A0%20Aeroportuale%202024-05-23%2016.37.22.excalidraw.md)%%


**Città**(**ID**)
**Aeroporto**(**ID**, Luogo, Quantità_Piste, *CittàID*)
**Passeggero**(**N_Doc**, Nome, Cognome, Nazionalità, Motivo, Bagaglio_a_mano)
**Funzionario**(**ID**, Nome, Cognome)
**Addetto**(**ID**, Nome, Cognome)
**Esito**(**ID**, Nome, Descrizione)
**Punto_di_Controllo**(**ID**)
**Categoria**(**ID**, Nome, Descrizione)
**Merce**(**ID**, *CategoriaID*, Descrizione, Quantità, Ritirata)
**Controllo**(**ID**, *Punto*, Data_Inizio, Ora_Inizio, *EsitoID*, Dazio, *Passeggero_N_Doc*, *FunzionarioID*, *AddettoID*)


