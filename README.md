# NetLogo-Agent-Based-Simulation
Bidding Market – Simulazione della Formazione del Prezzo con NetLogo

## Obiettivo

Questo progetto rappresenta un'esplorazione delle potenzialità di NetLogo, un programma per la simulazione ad agenti. Lo scopo dle progetto era quello di riadattare un modello esistente cercando di osservare come si forma e si adatta il prezzo in tre diversi tipi di mercato — monopolio, oligopolio e mercato competitivo.

L'idea di partenza è la teoria microeconomica classica, ma l'approccio utilizzato è quello dei modelli ad agenti: invece di risolvere equazioni e curve di domanda/offerta, ogni agente (compratore o venditore) segue regole comportamentali semplici, e il prezzo di equilibrio emerge dalle interazioni locali tra gli agenti stessi.


## Il Modello

Il progetto si basa su un modello NetLogo già esistente (Bidding Market), che è stato modificato e adattato per simulare i tre scenari di mercato ispirati alla teoria microeconomica.

La struttura del codice segue la logica tipica di NetLogo:

setup — inizializza il mercato: definisce il numero di venditori e compratori, assegna prezzi iniziali, quantità e disponibilità a pagare
go — fa evolvere la simulazione tick per tick, gestendo gli scambi tra agenti e l'aggiornamento adattivo dei comportamenti
do-commerce-with — cuore del modello: uno scambio avviene se il prezzo richiesto è minore o uguale alla disponibilità a pagare del compratore; in caso contrario la transazione non ha luogo

I tre scenari si differenziano principalmente per il numero di venditori:

Monopolio — un solo venditore, price maker, che controlla tutta l'offerta
Oligopolio — pochi venditori che competono adattando i propri prezzi
Mercato competitivo — molti venditori indipendenti, la concorrenza spinge i prezzi verso il basso

## Limitazioni e Differenze rispetto alla Teoria

Il modello non replica esattamente la microeconomia classica, e questo è un aspetto consapevole del progetto. Le principali differenze sono:

Nessun costo marginale né ricavo marginale — i venditori non risolvono la condizione MR = MC; i prezzi vengono aggiustati in modo adattivo (se vendo troppo poco, abbasso; se vendo tanto, aumento)
Nessuna curva di domanda formale — ogni compratore ha una propria disponibilità a pagare individuale, non esiste una funzione aggregata
Nessuna massimizzazione analitica del profitto — le decisioni degli agenti seguono regole reattive, non equazioni di ottimizzazione
Nessun equilibrio di Nash esplicito — i venditori non osservano strategicamente i concorrenti né anticipano le loro mosse
La quantità non è una variabile decisionale — i venditori vendono quanto richiesto se il prezzo è accettato; non scelgono una quantità ottima come nel modello di Cournot o Stackelberg

Ciò che il modello cattura correttamente rispetto alla teoria è la direzione dei risultati: nel monopolio il prezzo finale risulta più alto, nel mercato competitivo tende a stabilizzarsi verso il basso, nell'oligopolio si colloca in una posizione intermedia — in linea con le previsioni della microeconomia classica.

## Programma utilizzato
NetLogo — ambiente di modellazione agent-based
