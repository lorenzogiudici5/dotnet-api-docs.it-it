### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath genera un'eccezione NullReferenceException

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6.2, il runtime genera un <code>T:System.NullReferenceException</code> durante il recupero di un <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> valore che include caratteri null. In .NET Framework 4.6.1 e versioni precedenti, il runtime genera un <code>T:System.ArgumentNullException</code>.|
|Suggerimento|È possibile eseguire una delle seguenti per rispondere a questa modifica:<ul><li>Gestire il <code>T:System.NullReferenceException</code> se l'applicazione è in esecuzione in .NET Framework 4.6.2.</li><li>Eseguire l'aggiornamento a 4.7 il Framework .NET, che consente di ripristinare il comportamento precedente e genera un <code>T:System.ArgumentNullException</code>.</li></ul>|
|Ambito|Microsoft Edge|
|Versione|4.6.2|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

