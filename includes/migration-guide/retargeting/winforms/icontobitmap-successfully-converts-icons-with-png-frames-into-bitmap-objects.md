### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap converte correttamente le icone con i frame PNG in oggetti di Bitmap

|   |   |
|---|---|
|Dettagli|Partire dalle App destinate a .NET Framework 4.6, il <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> metodo converte correttamente le icone con i frame PNG in oggetti Bitmap. Nelle App destinate a .NET Framework 4.5.2 e versioni precedenti, il <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> metodo genera un <xref:System.ArgumentOutOfRangeException> eccezione se l'oggetto icona presenta frame PNG. Questa modifica influisce sulle App che vengono ricompilate per essere destinate a .NET Framework 4.6 e che implementano una gestione speciale per il <xref:System.ArgumentOutOfRangeException> che viene generata quando un oggetto icona presenta frame PNG. Quando è in esecuzione su .NET Framework 4.6, la conversione viene completata correttamente, non viene più generata un'eccezione <xref:System.ArgumentOutOfRangeException> e quindi non viene più richiamato il gestore di eccezioni.|
|Suggerimento|Se questo comportamento è indesiderato, è possibile mantenere il comportamento precedente aggiungendo l'elemento seguente al <code>&lt;runtime&gt;</code> sezione del file app. config:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>Se il file app. config contiene già il <code>AppContextSwitchOverrides</code> elemento, il nuovo valore deve essere unito con l'attributo value simile al seguente:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

