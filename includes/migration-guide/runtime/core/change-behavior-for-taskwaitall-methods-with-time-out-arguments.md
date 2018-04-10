### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Modifica del comportamento per i metodi Task.WaitAll con argomenti di timeout

|   |   |
|---|---|
|Dettagli|Task.WaitAll comportamento è stato reso più coerente in 4.5.In .NET di .NET Framework 4, questi metodi è incoerente. Alla scadenza del timeout, se una o più attività sono state completate o annullate prima della chiamata al metodo, il metodo genera un'eccezione <xref:System.AggregateException?displayProperty=name>. Alla scadenza del timeout, se nessuna attività è stata completata o annullata prima della chiamata al metodo, ma una o più attività sono entrate in questi stati dopo la chiamata al metodo, il metodo restituisce false.<br/><br/>In .NET Framework 4.5, questi overload del metodo ora restituire false se tutte le attività sono ancora in esecuzione quando l'intervallo di timeout è scaduto e generano un <xref:System.AggregateException?displayProperty=name> eccezione solo se è stata annullata un'attività di input (indipendentemente dal fatto se era prima o dopo il metodo chiamare) e altre attività non sono ancora in esecuzione.|
|Suggerimento|Se un <xref:System.AggregateException?displayProperty=name> è stata rilevata come mezzo per rilevare un'attività che è stata annullata prima della chiamata di metodo WaitAll richiamata, il codice deve invece eseguire operazioni di rilevamento stesso tramite la proprietà IsCanceled (ad esempio:. Any(t =&gt; t.IsCanceled)) poiché .NET 4.6 verrà semplicemente generata in questo caso se vengono completate tutte le attività di attese prima del timeout.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

