### <a name="httputilityjavascriptstringencode-escapes-ampersand"></a>HttpUtility.JavaScriptStringEncode escapes ampersand

|   |   |
|---|---|
|Dettagli|A partire da .NET Framework 4.5 <xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name> Usa sequenze di escape e commerciale (&amp;) caratteri.|
|Suggerimento|Se l'app dipende dal comportamento precedente di questo metodo, è possibile aggiungere un'impostazione aspnet:JavaScriptDoNotEncodeAmpersand all'[elemento appSettings di ASP.NET](https://msdn.microsoft.com/library/hh975440.aspx) nel file di configurazione.|
|Ambito|Secondario|
|Versione|4.5|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

