### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>Checksum del flusso di lavoro modificati da MD5 a SHA1

|   |   |
|---|---|
|Dettagli|Per supportare il debug con Visual Studio, il runtime del flusso di lavoro viene generato un checksum per un'istanza del flusso di lavoro usando un algoritmo di hash. In .NET Framework 4.6.2 e versioni precedenti, hashing checksum del flusso di lavoro utilizzato l'algoritmo MD5, che causa problemi nei sistemi abilitati per FIPS. A partire da 4.7 il Framework .NET, l'algoritmo è SHA1. Se il codice è resa persistente questi checksum, siano compatibili.|
|Suggerimento|Se il codice è in grado di caricare le istanze del flusso di lavoro a causa di un errore di checksum, provare a impostare il <code>AppContext</code> switch &quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; su true. Nel codice:<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>O nella configurazione:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.7|
|Tipo|Ridestinazione|

