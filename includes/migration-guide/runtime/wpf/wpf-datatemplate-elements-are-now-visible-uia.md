### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>Elementi DataTemplate WPF sono ora visibili per automazione

|   |   |
|---|---|
|Dettagli|In precedenza, <xref:System.Windows.DataTemplate?displayProperty=name> elementi sono invisibili per automazione interfaccia utente. A partire dalla versione 4.5, Automazione interfaccia utente rileva questi elementi. Ciò è utile in molti casi, ma può interrompere i test che dipendono da strutture ad albero di automazione non contenente <xref:System.Windows.DataTemplate?displayProperty=name> elementi.|
|Suggerimento|I test di automazione interfaccia utente per questa app potrebbe essere aggiornato per tenere conto dell'albero di automazione, ora inclusi in precedenza invisibile <xref:System.Windows.DataTemplate?displayProperty=name> elementi. Ad esempio, nei test che prevedono che alcuni elementi siano adiacenti può essere ora necessario prevedere che possono infrapporsi elementi di Automazione interfaccia utente precedentemente invisibili. Oppure, potrebbe essere necessario aggiornare con nuovi valori i test che si basano su conteggi o indici specifici per gli elementi di Automazione interfaccia utente.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

