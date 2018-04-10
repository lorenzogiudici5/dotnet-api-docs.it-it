### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>La condivisione dello stato della sessione con Asp.Net StateServer richiede tutti i server nella web farm per usare la stessa versione di .NET Framework

|   |   |
|---|---|
|Dettagli|Quando si abilita <xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name> sullo stato della sessione, tutti i server nella farm web specificato deve utilizzare la stessa versione di .NET Framework affinché lo stato per essere condivisi correttamente.|
|Suggerimento|Assicurarsi di aggiornare le versioni di .NET Framework nei server web che condividono lo stato nello stesso momento.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

