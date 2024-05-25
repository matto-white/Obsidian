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


**Città**(**ID**)
**Aeroporto**(**ID**, Luogo, Quantita_Piste, _CittaID_)
**Passeggero**(**N_Doc**, Nome, Cognome, Nazionalita, Motivo, Bagaglio_a_mano, _Controllo_ID_)
**Addetto**(**ID**, Nome, Cognome, _Controllo_ID_)
**Punto_di_Controllo**(**ID**)
**Funzionario**(**ID**, Nome, Cognome, _Controllo_ID_)
**Esito**(**ID**, Nome, Descrizione, _Controllo_ID_)
**Categoria**(**ID**, Nome, Descrizione)
**Merce**(**ID**, _CategoriaID_, Descrizione, Quantita, Ritirata)
**Controllo**(**ID**, Punto, Data_Inizio, Ora_Inizio, _EsitoID_, Dazio, _Passeggero_N_Doc_, _FunzionarioID_, _AddettoID_, _Merce_ID_)