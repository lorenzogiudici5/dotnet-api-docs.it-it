### <a name="listsort-algorithm-changed"></a>List. Sort algoritmo modificato

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.5, <xref:System.Collections.Generic.List%601?displayProperty=name>dell'algoritmo di ordinamento è stata modificata (per un ordinamento interiorizzato anziché un ordinamento rapido). <xref:System.Collections.Generic.List%601?displayProperty=name>del tipo di ordinamento non è mai stato stabile, ma questa modifica potrebbe causare diversi scenari di eseguire l'ordinamento in modi instabili. Questo significa semplicemente che gli elementi equivalenti ordinamento può essere eseguito in un ordine diverso nelle successive chiamate dell'API.|
|Suggerimento|Poiché l'algoritmo di ordinamento precedente è stata inoltre instabile (anche se in modi leggermente differenti), non deve esserci alcun codice che dipende da elementi equivalenti sempre l'ordinamento in un ordine particolare. Se sono presenti istanze di codice che a seconda che in corso dei con il comportamento precedente, che il codice deve essere aggiornato per usare un operatore di confronto che verrà in modo deterministico ordinare gli elementi nell'ordine desiderato.|
|Ambito|Trasparente|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

