### <a name="serialport-background-thread-exceptions"></a>Eccezioni di thread in background SerialPort

|   |   |
|---|---|
|Dettagli|In background thread creati con <xref:System.IO.Ports.SerialPort> flussi non terminano il processo quando vengono generate eccezioni del sistema operativo. Nelle applicazioni destinate a .NET Framework 4.7 e versioni precedenti, un processo viene terminato quando viene generata un'eccezione di sistema operativo in un thread in background creato con una <xref:System.IO.Ports.SerialPort> flusso. Nelle applicazioni che destina .NET Framework 4.7.1 o versioni successive, i thread in background in attesa di eventi del sistema operativo relative alla porta seriale active e potrebbe arrestarsi in modo anomalo in alcuni casi, ad esempio la rimozione improvviso della porta seriale.|
|Suggerimento|Per le app destinate a .NET Framework 4.7.1, è possibile rifiutare esplicitamente la gestione delle eccezioni se non è consigliabile aggiungere il codice seguente per il <code>&lt;runtime&gt;</code> sezione il <code>app.config</code> file:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Per le app destinate a versioni precedenti di .NET Framework ma eseguite su .NET Framework 4.7.1 o versioni successive, è possibile acconsentire esplicitamente all'eccezione aggiungendo il comando seguente per il <code>&lt;runtime&gt;</code> sezione il <code>app.config</code> file:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.7.1|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

