### <a name="xslt-style-sheet-exception-message-changed"></a>Messaggio eccezione foglio stile XSLT modificato

|   |   |
|---|---|
|Dettagli|In .NET Framework 4.5, il testo del messaggio di errore quando un file XSLT è troppo complesso è &quot;il foglio di stile è troppo complesso.&quot; Nelle versioni precedenti, il messaggio di errore era &quot;errore di compilazione XSLT.&quot; Il codice di applicazione che dipende dal testo del messaggio di errore non funzionerà più. Tuttavia, i tipi di eccezione rimangono gli stessi e pertanto questa modifica non dovrebbe avere un impatto reale.|
|Suggerimento|Aggiornare qualsiasi codice di app a seconda del messaggio di eccezione da questa condizione di errore per prevedere il nuovo messaggio, oppure (ancor meglio) aggiornare il codice per dipendere solo il tipo di eccezione (<xref:System.Xml.Xsl.XsltException?displayProperty=name>), che non è stato modificato.|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

