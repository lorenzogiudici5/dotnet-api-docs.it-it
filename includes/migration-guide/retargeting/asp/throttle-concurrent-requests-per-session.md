### <a name="throttle-concurrent-requests-per-session"></a>Limitazione delle richieste simultanee per sessione

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.6.2 in precedenza, ASP.NET esegue in modo sequenziale le richieste con l'ID di sessione stesso e ASP.NET esegue sempre Sessionid tramite i cookie per impostazione predefinita. Se una pagina richiede molto tempo a rispondere, riducono significativamente le prestazioni del server appena premendo F5 nel browser. La correzione è aggiunto un contatore per tenere traccia delle richieste in coda e terminano le richieste quando si supera il limite massimo specificato. Il valore predefinito è 50. Se viene raggiunto il limite, verrà registrato un avviso nel caso in cui log e una risposta HTTP 500 possono essere registrati nel Registro di IIS.|
|Suggerimento|Per ripristinare il comportamento precedente, è possibile aggiungere l'impostazione seguente al file web. config per rifiutare esplicitamente il nuovo comportamento.<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Ridestinazione|

