# DB-FIRST-USED-CARS

## Descrizione

Creazione delle colonne di una tabella per un database che raccoglie dati relativi ad auto usate messe in vendita da un concessionario, nelle colonne vengono indicati:

- Nome della colonna
- Tipo e rappresentazione del dato
- Attributi aggiuntivi come NULL/NOT NULL, DEFAULT, AUTO_INCREMENTE, UNIQUE.

### Considerazioni

Per progettare i vari dati delle colonne son state fatte le seguenti considerazioni:

- Solo i dati che potrebbero non essere necessari fin da subito o quelli che potrebbero non essere presenti su auto elettriche(Cilindri, Cilindrata) accetteranno valori NULL
- Per i dati di tipo stringa è stato impostato un VARCHAR(30) cautelativamente, ad eccezione della DESCRIZIONE_VEICOLO a cui è stato dato TEXT presupponendo un numero maggiore di caratteri.
- Per molto accessori tipo sensori parcheggio, autoradio, bluetooth etc.. sono stati assegnati TINYINT come dato che poi verrà considerato un true false booleano
- Per i dati numerici con unità di misura e valuta((pesi, prezzi, cilindrata, etc..) si è scelto di non usare stringhe numeriche ma numeri, avendo già in mente in che unità o valuta saranno.
  La scelta tra TINYINT, SMALLINT e MEDIUMINT è stata effettuata basandosi sui valori massimi tipici del dato di volta in volta.
- Per il codice alfanumerico del numero di immatricolazione è stato scelto CHAR al posto di VARCHAR poichè il numero di caratteri è noto a priori e così la leggibilità del dato dal database sarà più veloce
