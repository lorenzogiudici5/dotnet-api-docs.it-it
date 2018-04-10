### <a name="path-colon-checks-are-stricter"></a>Controlli del percorso i due punti sono più severi

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6.2, un numero di modifiche sono stato apportato per supportare i percorsi in precedenza non supportati (sia di lunghezza e il formato). Controlli per la sintassi di unità appropriata separatore (due punti) sono stati apportati più corretti, che ha l'effetto collaterale di alcuni percorsi URI in alcune API percorso selezionare quale usati per essere espresso di blocco.|
|Suggerimento|Se si passa un URI alle API interessate, modificare la stringa per essere innanzitutto un percorso valido.<ul><li>Rimuovere manualmente la combinazione di dagli URL (ad esempio rimuovere <code>file://</code> dagli URL)</li><li>Passare l'URI per il <xref:System.Uri> classe e usare <xref:System.Uri.LocalPath></li></ul>In alternativa, è possibile rifiutare esplicitamente la normalizzazione di percorso nuovo impostando il <code>Switch.System.IO.UseLegacyPathHandling</code> commutatore AppContext su true.|
|Ambito|Microsoft Edge|
|Versione|4.6.2|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

