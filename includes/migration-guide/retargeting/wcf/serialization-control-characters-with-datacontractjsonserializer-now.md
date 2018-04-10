### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>Serializzazione dei caratteri di controllo con DataContractJsonSerializer è ora compatibile con ECMAScript V6 e V8

|   |   |
|---|---|
|Dettagli|In .NET framework 4.6.2 e versioni precedenti, il <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> non è stato serializzato alcuni caratteri di controllo speciali, ad esempio \b \f e \t, in modo compatibile con gli standard V8 ed ECMAScript V6. A partire dal 4.7 di .NET Framework, la serializzazione di questi caratteri di controllo è compatibile con ECMAScript V6 e V8.|
|Suggerimento|Per le app destinate 4.7 il Framework .NET, questa funzionalità è abilitata per impostazione predefinita. Se questo comportamento non è opportuno, è possibile rifiutare esplicitamente questa funzionalità aggiungendo la riga seguente alla sezione <code>&lt;runtime&gt;</code> del file app.config o web.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

