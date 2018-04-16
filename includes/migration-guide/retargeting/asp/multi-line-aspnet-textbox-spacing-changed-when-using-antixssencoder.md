### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>Spaziatura ASP.Net casella di testo multilinea modificata quando si utilizza AntiXSSEncoder

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.0 vengono inserite righe aggiuntive tra le righe di una casella di testo a più righe durante il postback, se si usa <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>. In .NET Framework 4.5 queste interruzioni di riga aggiuntive non vengono incluse, ma solo se l'app Web è destinata a .NET 4.5|
|Suggerimento|Tenere presente che nelle app Web 4.0 ridestinate a .NET 4.5, le caselle di testo a più righe possono essere migliorate in modo che non vengano più inserite interruzioni di riga aggiuntive. Se ciò non è opportuno, l'app può avere il comportamento precedente durante l'esecuzione in .NET Framework 4.5 specificando come destinazione di .NET Framework 4.0.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Ridestinazione|
