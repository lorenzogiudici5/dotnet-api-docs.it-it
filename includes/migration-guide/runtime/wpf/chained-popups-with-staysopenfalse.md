### <a name="chained-popups-with-staysopenfalse"></a>Concatenare i popup con StaysOpen = False

|   |   |
|---|---|
|Dettagli|Una finestra Popup con StaysOpen = False deve per chiudere quando si fa clic all'esterno del Popup. Quando due o più tale popup autogestite, collegate (vale a dire uno contiene un altro), sono molti problemi, tra cui:<ul><li>Aprire due livelli, fare clic all'esterno di P2, ma all'interno di P1.  Non viene eseguita alcuna operazione.</li><li>Aprire due livelli, fare clic su P1 esterno.  Chiudere entrambi i popup.</li><li>Aprire e chiudere due livelli.  Quindi provare nuovamente ad aprire P2.  Non viene eseguita alcuna operazione.</li><li>Provare ad aprire tre livelli.  Non puoi.  (Non accade nulla o chiudono i primi due livelli, a seconda di dove si fa clic su.) Questi casi (e altre varianti) ora funzionano come previsto.</li></ul>|
|Ambito|Microsoft Edge|
|Versione|4.7.1|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

