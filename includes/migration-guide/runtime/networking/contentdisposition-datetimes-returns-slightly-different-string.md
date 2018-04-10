### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>ContentDisposition DateTimes restituisce stringa leggermente diversa

|   |   |
|---|---|
|Dettagli|Rappresentazioni di stringa di <xref:System.Net.Mime.ContentDisposition?displayProperty=name>del sono state aggiornate, a partire da 4.6, per rappresentare sempre il componente ora di un <xref:System.DateTime?displayProperty=name> con due cifre. Questo comportamento è conforme a [RFC822](http://www.ietf.org/rfc/rfc0822.txt) e [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). Ne consegue che <xref:System.Net.Mime.ContentDisposition.ToString> restituisce una stringa leggermente diversa nella versione 4.6 negli scenari in cui uno degli elementi di tempo della disposizione precede le 10.00. Si noti che ContentDispositions talvolta vengono serializzati tramite convertendoli in stringhe, pertanto, qualsiasi <xref:System.Net.Mime.ContentDisposition.ToString> operazioni, la serializzazione o chiamate GetHashCode dovrebbero essere rivisti.|
|Suggerimento|Non dare per scontato che le rappresentazioni di stringa di ContentDisposition da versioni diverse di .NET Framework vengano confrontate correttamente. Se possibile, riconvertire le stringhe in ContentDisposition prima di eseguire un confronto.|
|Ambito|Secondario|
|Versione|4.6|
|Tipo|Runtime|
|API interessate|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

