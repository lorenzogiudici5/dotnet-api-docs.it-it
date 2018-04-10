### <a name="httprequestcontentencoding-property-prohibits-utf7"></a>Proprietà ContentEncoding impedisce UTF7

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.5, la codifica UTF-7 non è consentita in <xref:System.Web.HttpRequest?displayProperty=name>s' corpi. In alcuni casi i dati per le applicazioni che dipendono dai dati UTF-7 in ingresso non verranno decodificati correttamente.|
|Suggerimento|In teoria, le applicazioni devono essere aggiornate per non utilizzare la codifica UTF-7 <xref:System.Web.HttpRequest?displayProperty=name>s. In alternativa, è possibile ripristinare il comportamento legacy usando l'attributo <code>aspnet:AllowUtf7RequestContentEncoding</code> dell'elemento [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx).|
|Ambito|Microsoft Edge|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|

