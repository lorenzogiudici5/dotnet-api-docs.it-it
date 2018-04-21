### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException nel codice di gestione delle eccezioni da ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Dettagli|A causa di un errore nel codice di gestione delle eccezioni per <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> veniva generata una <xref:System.NullReferenceException?displayProperty=name> non corretta invece dell'eccezione prevista (ad esempio <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>). Questa modifica consente di correggere l'errore in modo che il metodo generi ora l'eccezione appropriata. Per impostazione predefinita tutte le applicazioni destinate a .NET Framework 4.6.2 e versioni precedenti continueranno a generare <xref:System.NullReferenceException?displayProperty=name> per garantire la compatibilità. Gli sviluppatori di applicazioni .NET Framework 4.7 e versioni successive dovrebbe vedere le eccezioni corrette. // Sostituire lo spazio con una "x" se applicabile|
|Suggerimento|Gli sviluppatori che desiderano tornare al recupero di <xref:System.NullReferenceException?displayProperty=name> quando usano .NET Framework 4.7 come destinazione possono aggiungere/unire il codice seguente nel file App.config della propria applicazione:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

