### <a name="deadlock-may-result-when-using-reentrant-services"></a>Deadlock si verifichi quando si utilizza servizi rientranti

|   |   |
|---|---|
|Dettagli|Può causare un deadlock di un servizio rientrante, che limita le istanze del servizio a un solo thread di esecuzione alla volta. Servizi soggetti a verifica questo problema saranno necessario quanto segue <xref:System.ServiceModel.ServiceBehaviorAttribute> nel codice:<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|Suggerimento|Per risolvere questo problema, è possibile eseguire le operazioni seguenti:<ul><li>Impostare la modalità di concorrenza del servizio <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> oppure &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;. Ad esempio:</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>Installare l'aggiornamento più recente di .NET Framework 4.6.2 oppure eseguire l'aggiornamento a una versione successiva di .NET Framework. Disabilita il flusso dei <xref:System.Threading.ExecutionContext> in <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>. Questo comportamento è configurabile; è equivalente all'aggiunta la seguente impostazione dell'applicazione al file di configurazione:</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.6.2|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

