### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>ETW EventListeners non acquisire gli eventi dai provider con parole chiave esplicite (ad esempio, il provider TPL)

|   |   |
|---|---|
|Dettagli|Gli EventListener ETW con una maschera di parole chiave vuota non acquisiscono correttamente gli eventi dai provider con parole chiave esplicite. In .NET Framework 4.5, il provider TPL ha iniziato a fornire parole chiave esplicite e ha causato questo problema. In .NET Framework 4.6, gli EventListener sono stati aggiornati e non presentano più questo problema.|
|Suggerimento|Per risolvere questo problema, sostituire le chiamate a <xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)> con le chiamate all'overload EnableEvents che specifichi esplicitamente il &quot;parole&quot; mask da utilizzare: <code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>. In alternativa, questo problema è stato risolto in .NET Framework 4.6 e potrebbe essere risolto eseguendo l'aggiornamento a tale versione di .NET Framework.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|

