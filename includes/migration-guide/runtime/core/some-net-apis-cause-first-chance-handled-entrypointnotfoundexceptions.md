### <a name="some-net-apis-cause-first-chance-handled-entrypointnotfoundexceptions"></a>Alcune API .NET causa prima opportunità di EntryPointNotFoundExceptions (gestito)

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.5, un numero ridotto di metodi .NET è iniziata la generazione prima opportunità di gestire <xref:System.EntryPointNotFoundException?displayProperty=name>s. Queste eccezioni sono gestite all'interno di .NET Framework, ma possono interrompere l'automazione dei test che non si aspettano eccezioni first-chance. Queste stesse API causano errori in alcuni scenari di ApiVerifier con HighVersionLie abilitato.|
|Suggerimento|È possibile evitare questo bug eseguendo l'aggiornamento a .NET Framework 4.5.1. In alternativa, automazione dei test può essere aggiornata per non interrompere l'esecuzione in first-chance <xref:System.EntryPointNotFoundException?displayProperty=name>s.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Diagnostics.Debug.Assert(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Debug.Assert(System.Boolean,System.String,System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Xml.Serialization.XmlSerializer.%23ctor(System.Type)?displayProperty=nameWithType></li></ul>|

