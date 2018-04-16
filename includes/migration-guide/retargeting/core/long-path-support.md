### <a name="long-path-support"></a>Supporto del percorso lungo

|   |   |
|---|---|
|Dettagli|Partire dalle App destinate a .NET Framework 4.6.2, percorsi lunghi (caratteri fino a 32 KB) sono supportati e i 260 caratteri (o <code>MAX_PATH</code>) limitazione nella lunghezza dei percorsi è stata eliminata. Per le app che vengono ricompilate per .NET Framework 4.6.2, il codice di percorsi che in precedenza ha generato un <xref:System.IO.PathTooLongException?displayProperty=name> perché ha superato un percorso di 260 caratteri ora genererà un <xref:System.IO.PathTooLongException?displayProperty=name> esclusivamente nelle condizioni seguenti:<ul><li>La lunghezza del percorso è maggiore di <xref:System.Int16.MaxValue> (32.767) caratteri.</li><li>Il sistema operativo restituisce <code>COR_E_PATHTOOLONG</code> o equivalente.</li></ul>Per le app destinate a .NET Framework 4.6.1 e versioni precedenti, il runtime genera automaticamente un <xref:System.IO.PathTooLongException?displayProperty=name> ogni volta che un percorso supera i 260 caratteri.|
|Suggerimento|Per le app destinate a .NET Framework 4.6.2, è possibile rifiutare esplicitamente il supporto di percorsi lunghi se non è consigliabile aggiungere il codice seguente per il <code>&lt;runtime&gt;</code> sezione il <code>app.config</code> file:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Per le app destinate a versioni precedenti di .NET Framework, ma eseguire in .NET Framework 4.6.2 o in un secondo momento, è possibile acconsentire esplicitamente al tempo percorso supporto aggiungendo il comando seguente per il <code>&lt;runtime&gt;</code> sezione il <code>app.config</code> file:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.6.2|
|Tipo|Ridestinazione|
