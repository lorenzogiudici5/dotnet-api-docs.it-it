### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase non propaga le eccezioni di OnStart

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.7 e versioni precedenti, le eccezioni generate all'avvio del servizio non vengono propagate al chiamante di <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>. A partire da applicazioni destinate a .NET Framework 4.7.1, il runtime propaga le eccezioni a <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType> per i servizi che non vengono avviati.|
|Suggerimento|Avvio del servizio, se si verifica un'eccezione, tale eccezione verrà propagata. Questo dovrebbe aiutare a diagnosticare casi in cui servizi non avviati. Se questo comportamento è indesiderato, è possibile rifiutare esplicitamente aggiungendo quanto segue <AppContextSwitchOverrides> elemento per il <runtime> sezione del file di configurazione dell'applicazione:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>Se l'applicazione è destinata a una versione precedente a 4.7.1 ma si desidera che questo comportamento, aggiungere il seguente <AppContextSwitchOverrides> elemento per il <runtime> sezione del file di configurazione dell'applicazione:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.7.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

