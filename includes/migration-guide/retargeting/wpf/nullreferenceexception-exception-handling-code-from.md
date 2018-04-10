### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>Nel codice da ImageSourceConverter.ConvertFrom di gestione delle eccezioni NullReferenceException

|   |   |
|---|---|
|Dettagli|Un errore nel codice per le eccezioni <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> ha causato un'implementazione non corretta <xref:System.NullReferenceException?displayProperty=name> generazione dell'eccezione anziché l'eccezione previsto (ad esempio <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), questa modifica consente di correggere l'errore in modo che il metodo genera ora l'eccezione appropriata. Per impostazione predefinita tutte le applicazioni destinate a .NET Framework 4.6.2 e seguito continuerà a generare <xref:System.NullReferenceException?displayProperty=name> per garantire la compatibilità, gli sviluppatori di applicazioni .NET Framework 4.7 e versioni successive dovrebbe essere il destro exceptions.// sostituire lo spazio con una "x" se applicabile|
|Suggerimento|Gli sviluppatori che desiderano ripristinare recupero <xref:System.NullReferenceException?displayProperty=name> quando destinato a .NET Framework 4.7 può aggiungere/unione quanto segue al file app. config della propria applicazione:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Ambito|Microsoft Edge|
|Versione|4.7|
|Tipo|Ridestinazione|
|API interessate|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

