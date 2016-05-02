#Road to ES6
###Speaker: WeLaika (Filippo Gangelino)
###Date: 02/05/2016
###Conference event: Torino Coding Society 

Here I will copy&paste the synopsys of the keynote.

######My Actual Notes

Here we are, live @TAG.

Un incontro di base su ES6: intanto... perchè?
Nonostante qualcuno flami e dica che Javascript sia morto, loro han deciso di andare in questa direzione.

Han scelto Javascript perchè è *universale*. Dobbiamo averne a che fare, e con piacere.
Dopo 15-20 anni di evoluzione del linguaggio finalmente si è deciso di dare uno "standard".

Partiamo subito:

* **Let** 
    = ci permette di definire una variabile all'interno di un blocco preciso.
    Con ES5 il problema era che lo scope viene definito al di fuori del nostro codice.
    
* **const** 
    = è in qualche modo la definizione di una costante. Nel senso che non la definisci "per davvero" come read-only; in questo caso infatti si può variare il suo valore, ma la variabile non può essere riassegnata.
    Le costanti valgono anche per gli oggetti... ed è qua che è facile accorgersi di immutabilità, è la referenza che non può essere sovrascritta.
    
* **arrow function**
    = sono un modo più compatto per scrivere delle funzioni... è un sintactic sugar per definire le funzioni alla fine: => è equivalente a function()
    E preservano lo scope.
    Quando c'è una sola riga c'è l'implicit return.
    
* **Destructuring**
    In ES6 hanno introdotto alcune cose un po' più "agili", tra cui:
    * Array matching
    * Object matching (permette anche assegnazioni anche abbastanza "complesse" da fare senza passaggi più espliciti)
 
* **Parameter handling**
    Anche in questo ambito ES6 permette cose simpatiche:
    * Default values
    * Rest parameters (the ... value)
    * Spread operator (sempre legato al ... )
    
* **String interpolation**
    Finalmente anche JS si aggiorna a livelli umani di gestione delle stringhe.

* **Iterators**
    ES6 da un nuovo giochino, praticamente un iteratore di alto livello, richiamato da Symbol.iterator(). Ha un paio di proprietà, e una funzione next() che è tipo il ++.
    Inoltre ES6 da' una nuova versione di un ciclo while, chiamato for...of.
    Ovviamente se non viene settato in maniera appropriata si va in loop infinito.
    
* **Classes**
    ES6 si muove anche verso la programmazione ad oggetti.
    ...in maniera molto simile al coffeescript.
    * Class inheritance

* **Modules**
    "Questa roba è ES6", ma a volerla implementare... non se ne esce.
    Di base dovrebbe essere molto più di un banale transpiring: stiamo parlando di isolare porzioni di logica da importare/esportare.

* **Promises**
    Oggetti usati per deferring e asynchrounous computation. Niente di nuovo, ma integrazione di uno standard già adottato.
    Però essere in uno di 3 stati:
    * Pending
    * Fulfilled
    * Rjected
    
    
// *sono dovuto andare via per questioni logistiche, non so quanto abbia ancora spiegato* //

######The speaker bio

As title, the speaker short bio. Or infos. Or whatever.

######The conference description

Small text about the conference.
