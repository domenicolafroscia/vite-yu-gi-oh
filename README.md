### ESERCIZIO
####Prima parte
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Al caricamento della pagina, effettuate una chiama ajax all'API di Yu-Gi-Oh.
Per prendere le prime 20 cards potete usare questo link:
https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0

**Bonus:**
Creare un componente loader da visualizzare fintantoché i risultati non sono pronti.

#### Seconda parte
Continuate a lavorare nella stessa repo di ieri e aggiungete una select per filtrare i risultati in base all'archetipo:  Alien, Ally of Justice o Ancient Gear.
Quando l'utente seleziona un valore dalla lista, viene effettuata una chiamata alle API con le cards corrispondenti.

**Bonus:**
Creare un componente che mostri il numero totale di risultati ottenuti.

**Nota:**
Per capire come comunicare alle API l'archetipo, è necessario fare riferimento alla documentazione che trovate qui: https://ygoprodeck.com/api-guide/
