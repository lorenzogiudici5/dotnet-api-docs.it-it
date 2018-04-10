### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>Metodo System.Uri.IsWellFormedUriString restituisce false per gli URI relativi con un carattere due punti nel primo segmento

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.5 <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> tratterà gli URI relativo con un <code>:</code> nella loro primo segmento come non corretto. Si tratta di una modifica da <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> comportamento in .NET Framework 4.0 che è stata effettuata di conformarsi a RFC3986.|
|Suggerimento|Questa modifica (ad esempio, molte altre modifiche URI) influiranno solo applicazioni destinate a .NET Framework 4.5 (o versione successivo). Per continuare a usare il comportamento precedente, scegliere come destinazione l'app rispetto a .NET Framework 4.0. In alternativa, analizzare dell'URI prima di chiamare <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> cercando <code>:</code> caratteri che è possibile rimuovere ai fini della convalida, se è consigliabile che il comportamento precedente.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

