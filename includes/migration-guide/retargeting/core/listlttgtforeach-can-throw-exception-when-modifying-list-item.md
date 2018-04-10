### <a name="listlttgtforeach-can-throw-exception-when-modifying-list-item"></a>Elenco&lt;T&gt;. ForEach può generare eccezioni quando si modifica l'elemento elenco

|   |   |
|---|---|
|Dettagli|A partire da .NET 4.5, una <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> enumeratore genererà un <xref:System.InvalidOperationException?displayProperty=name> eccezione se un elemento nella raccolta chiamante viene modificato. Nelle versioni precedenti questa condizione non genera un'eccezione ma può causare situazioni di race condition.|
|Suggerimento|Idealmente, il codice dovrebbe essere corretto per evitare la modifica degli elenchi durante l'enumerazione dei relativi elementi, perché questa non è mai un'operazione sicura. Per ripristinare il comportamento precedente, tuttavia, un'app può essere destinata a .NET 4.0.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|

