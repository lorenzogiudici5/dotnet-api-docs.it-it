### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF AddressHeaderCollection genera ora ArgumentException se un elemento addressHeader è null

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.7.1, il <xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})> costruttore genera un <xref:System.ArgumentException> se uno degli elementi è <code>null</code>. In .NET Framework 4.7 e versioni precedenti, viene generata alcuna eccezione.|
|Suggerimento|Se si verificano problemi di compatibilità con questa modifica in .NET Framework 4.7.1 o una versione successiva, è possibile rifiutare esplicitamente di esso aggiungendo la riga seguente al <code>&lt;runtime&gt;</code> sezione del file app. config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ambito|Secondario|
|Versione|4.7.1|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

