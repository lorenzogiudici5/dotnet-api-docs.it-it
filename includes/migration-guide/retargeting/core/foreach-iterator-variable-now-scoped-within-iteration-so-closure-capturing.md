### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Variabile di iteratore foreach ambita all'interno dell'iterazione, pertanto la semantica di acquisizione di chiusura è diversa (in C n. 5)

|   |   |
|---|---|
|Dettagli|A partire da c# 5 (Visual Studio 2012), <code>foreach</code> variabili iteratore incluse nell'ambito di iterazione. Ciò può provocare interruzioni se codice è stato in precedenza dipende le variabili a non essere presenti il <code>foreach</code>della chiusura. Il sintomo di questa modifica è che una variabile di iteratore passata a un delegato viene considerata come il valore è al momento il delegato viene creato, anziché il valore che è al momento che il delegato viene richiamato.|
|Suggerimento|Idealmente, è consigliabile aggiornare il codice in modo che tenga conto del nuovo comportamento del compilatore. Se è richiesta la semantica precedente, la variabile iteratore può essere sostituita con una variabile separata che viene inserita in modo esplicito all'esterno dell'ambito del ciclo.|
|Ambito|Principale|
|Versione|4.5|
|Tipo|Ridestinazione|

