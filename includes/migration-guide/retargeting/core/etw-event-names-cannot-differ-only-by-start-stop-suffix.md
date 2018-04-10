### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>I nomi degli eventi ETW non possono distinguersi solo per un suffisso "Start" o "Stop"

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6 e 4.6.1, il runtime genera un' <xref:System.ArgumentException> quando i nomi degli eventi di Event Tracing for Windows (ETW) due differiscono solo per un &quot;avviare&quot; o &quot;arrestare&quot; suffisso (come quando un evento denominato <code>LogUser</code>e un altro denominato <code>LogUserStart</code>). In questo caso, il runtime non può creare l'origine dell'evento, quindi non viene generata alcuna registrazione.|
|Suggerimento|Per evitare l'eccezione, assicurarsi che nessun nome di due evento differiscono solo per un &quot;avviare&quot; oppure &quot;arrestare&quot; suffisso. Questo requisito viene rimosso a partire da .NET Framework 4.6.2; il runtime può risolvere l'ambiguità di nomi di evento che differiscono solo per il &quot;avviare&quot; e &quot;arrestare&quot; suffisso.|
|Ambito|Microsoft Edge|
|Versione|4.6|
|Tipo|Ridestinazione|

