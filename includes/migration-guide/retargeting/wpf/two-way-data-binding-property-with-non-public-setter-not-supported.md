### <a name="two-way-data-binding-to-a-property-with-a-non-public-setter-is-not-supported"></a>Associazione dati bidirezionale a una proprietà con un setter non pubblico non è supportata

|   |   |
|---|---|
|Dettagli|Il data binding per una proprietà senza un setter pubblico non è mai stata uno scenario supportato. A partire da .NET Framework 4.5.1, questo scenario, verrà generata un' <xref:System.InvalidOperationException?displayProperty=name>. Si noti che la nuova eccezione verrà generata soltanto per le app destinate specificamente a .NET Framework 4.5.1. Per le app destinate a .NET Framework 4.5, la chiamata sarà consentita. Se l'app non è destinata a una versione specifica di .NET Framework, l'associazione verrà considerata unidirezionale.|
|Suggerimento|È consigliabile aggiornare l'app per usare l'associazione unidirezionale o esporre pubblicamente il setter della proprietà. In alternativa, è possibile destinare l'app a .NET Framework 4.5 per ottenere il comportamento precedente.|
|Ambito|Secondario|
|Versione|4.5.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType></li></ul>|

