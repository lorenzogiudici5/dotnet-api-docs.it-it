### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable&lt;TResult&gt; sempre restituisce memorizzate nella cache di istanza

|   |   |
|---|---|
|Dettagli|A partire da .NET 4.5 <xref:System.Linq.Enumerable.Empty%60%601> restituisce sempre un'istanza interna memorizzata nella cache <xref:System.Collections.Generic.IEnumerable%601>. In precedenza, <xref:System.Linq.Enumerable.Empty%60%601> verrebbe memorizzare nella cache vuota <xref:System.Collections.Generic.IEnumerable%601> al momento della chiamata API, vale a dire che in alcune condizioni in cui <xref:System.Linq.Enumerable.Empty%60%601> è stato chiamato in modo rapido e contemporaneamente, diverse istanze del tipo è stato possibile restituire per le diverse chiamate al API.|
|Suggerimento|Dato che il comportamento precedente è non deterministico, è improbabile che esista codice dipendente. Tuttavia, nel caso improbabile che i tipi enumerabili vuoti vengano usati per confronti prevedendo che talvolta possano essere diversi, è consigliabile creare matrici vuote esplicite (<code>new T[0]</code>) invece di usare <xref:System.Linq.Enumerable.Empty%60%601>.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

